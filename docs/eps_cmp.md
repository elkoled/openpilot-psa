# CMP EPS — practical insights for openpilot

Practical findings about the CMP electric power steering ECU, validated where possible on the opendbc
`PSA_PEUGEOT_208` test route `6a7075a4fdd765ee/0000004e--1f612006dd`.

**Confidence tags**
- **[route]**: confirmed on real CAN data from a 208.
- **[ECU]**: confirmed in the ECU's logic.
- **[CAL]**: the logic exists, but the number comes from a development calibration and must be confirmed on a car.

Applies to: CMP / e-CMP cars with this EPS (208/2008 II, Corsa F, Mokka B, DS3 Crossback, C4 III and likely
Avenger/600/Junior/Ypsilon; the model list is a hypothesis).
**Does not apply to EMP2 V3 cars**: they use an EPS from a different supplier with different software.

---

## 1. TL;DR for openpilot

1. **0x3F2 has no checksum/counter check in this EPS** [ECU]. It only checks: DLC = 8, `TORQUE_FACTOR` 0..100 (126 = "unavailable"), `STATUS` ≠ 7, |`SET_ANGLE`| ≤ 780° (then clipped to ±500°).
2. **Stock 0x3F2 period is 50 ms** [route]. A missing frame for **200 ms** → LKA Defect. Recovery needs **10 consecutive good frames** (500 ms at 20 Hz) [ECU].
3. **2→3→4 `STATUS` sequence is mandatory**, but there is no minimum time per step: one frame each is enough. Active also needs `TORQUE_FACTOR` > 0 [ECU].
4. **Driver override can latch LKA off until the next ignition cycle.** The EPS hands back at ~3–5 Nm, but a separate safety monitor latches a fault if the driver applies more than about 5 Nm for 240 ms while the LKA torque is non-zero [CAL]. openpilot should release (move the target to the measured angle or ramp `TORQUE_FACTOR`) **well before 3 Nm**.
5. **After an override the EPS refuses to re-arm for 10–20 s** (longer at low speed) [CAL]. Cycling 2/3/4 won't help, so show "steering unavailable".
6. **The EPS drops LKA if the measured wheel angle stays above a speed-dependent limit for 200 ms** (dev calibration: ~25° at standstill, ~20° at 100 km/h) [CAL]. This is a likely cause of drop-outs in tight turns and roundabouts. openpilot's 390° limit is irrelevant in practice.
7. **Keep `LXA_ACTIVATION = 1`** (LPA mode). The hands-off timeout is then speed-dependent, from about 60 s at 0 km/h to 10 s at 100 km/h, + 3 s. In LKA mode it is a fixed 10–13 s [ECU].
8. **Never set 0x3F2 byte 0 bit 2 (`DMD_DELEST_DA`)**: on Stop&Start cars it is a power-cut request that removes steering assist at low speed [ECU].
9. **Never send 0x092 with 0xC0**: three of them put the EPS into a silent "electronic integration" mode (no TX, no DTCs), which is persisted [ECU].
10. **Variant coding:** an EPS from a car without factory LKA is not coded for it and will stay `Unauthorised` forever [ECU].

---

## 2. CAN interface

Single bus (DCAN1, 500 kbit/s). Byte order Motorola. The DBC fragment with all EPS-relevant frames is in
[`dbc/psa_cmp_eps.dbc`](../dbc/psa_cmp_eps.dbc).

### 2.1 EPS receives

| ID | Name | Use in EPS | Notes |
|---|---|---|---|
| 0x3F2 | IS_DAT_BSI_3F2 (opendbc `LANE_KEEP_ASSIST`) | LKA/LXA command | see 2.3 |
| 0x38D | IS_DYN_ABR (vehicle speed) | speed, LKA validity | nibble checksum chk_ini 0x7 [route]. Bad for ≥ 5 frames → EPS assumes **100 km/h** and LKA becomes invalid [ECU] |
| 0x388 / 0x208 / 0x348 | engine data | engine running state, speed fallback | assist needs engine state in {3,4,5,6,13} for 3 frames, or speed ≥ 8 km/h |
| 0x34D | IS_DYN_CDS_34D | ESP off / ESP regulating | LKA needs ESP on and not regulating |
| 0x50D | IS_DAT_ABR_50D | — | required for LKA validity |
| 0x3CD | IS_DYN2_FRE_3CD | lateral acceleration (bytes 0–1, 0.05 m/s²) | opendbc layout differs, verify |
| 0x412 | IS_DAT_BSI_412 | drive mode request `REQ_MODE_DA` (bits 30–31) | selects steering personality (normal/sport) |
| 0x2EB | IS_DYN_AAS | park assist (CityPark) angle command | checksum chk_ini 0x4 + counter, ≤ 2–10 km/h only. **Not usable for openpilot** |
| 0x5CD | PROTO_HS1_DYN_UCF_5CD | ESC steering-angle offset | checksum chk_ini 0x1 |
| 0x092 | IS_INTE_ELECTRON_BSI | silent mode / clear DTC | **never send** |

### 2.2 EPS transmits

| ID | Name | Rate | Content |
|---|---|---|---|
| 0x2F5 | IS_DYN_DAE (opendbc `STEERING`) | 100 Hz | driver torque `CPLE_VOLANT_OPTMSE` **0.1 Nm/bit**, ±10 Nm, 127 = invalid; relative column angle (zero at power-on); column rate; park-assist state. Checksum: high nibble of byte 0, nibble-sum, chk_ini 0xB; counter: low nibble of byte 0 [route] |
| 0x305 | IS_DYN_VOL (opendbc `STEERING_ALT`) | 100 Hz | absolute steering angle 0.1°, **rate 4 °/s per bit** [route], angle-source and validity flags. **XOR checksum**: high nibble of byte 4; counter: low nibble of byte 4 [route] |
| 0x495 | IS_DAT_DIRA | 10 Hz | `CPLE_VOLANT` (driver torque 0.25 Nm, **not EPS torque**), `EPS_STATE_LKA`, `STEERWHL_HOLD_BY_DRV`, `TRQ_LIMIT_STATE`, `DDE_REDEM_DA` (**Stop&Start engine restart request, not an EPS reboot**) |
| 0x795 | IS_SUPV_DIRA | ~1 Hz [route] | `ETAT_ASSIST_DA`: 0 off, 1 nominal, 2 **degraded** (thermal etc.), 3/4 Stop&Start |
| 0x115 | IS_VERS_DIRA_115 | event | SW version broadcast; **not seen on the 208 route** |
| 0x695 / 0x6B5 | diag response / request | — | UDS, see §5 |

**0x305 checksum** [ECU][route: 18,147/18,147 frames]:
```python
x = d[0] ^ d[1] ^ d[2] ^ d[3] ^ (d[4] & 0x0F)   # checksum nibble (high nibble of byte 4) zeroed
chk = (x ^ (x >> 4)) & 0xF
```
Note: this frame does not use the usual PSA nibble sum.

**PSA nibble checksum** (other frames): a frame is valid when `(sum of all nibbles + CHKINI) & 0xF == 0xF`, so opendbc's
`chk_ini = 0xF − CHKINI`. Confirmed values: 0x2F5 = 0xB, 0x38D = 0x7 [route]; 0x2EB = 0x4, 0x5CD = 0x1 [ECU].

### 2.3 0x3F2 (LANE_KEEP_ASSIST), what the EPS actually reads

| Signal | Bits | Meaning |
|---|---|---|
| `DMD_DELEST_DA` | 2\|1 | Stop&Start power-cut request. **Must be 0** |
| `LKA_STATE` / opendbc `STATUS` | 36\|3 | 0 unavailable, 1 unselected, 2 selected, 3 authorized, 4 active, 5 defect, 6 collision, 7 invalid |
| `LXA_ACTIVATION` | 40\|1 | 0 = LKA, 1 = LPA (speed-dependent hands-off time) |
| `LKA_TRQ_FACT_REQ` / `TORQUE_FACTOR` | 47\|7 | 0.01/bit, 0..100 = 0..1.0; 126 = unavailable (treated as 0); others invalid (fault after 4 frames) |
| `COLUMN_ANGLE_SETPOINT` / `SET_ANGLE` | 55\|14 signed | 0.1°/bit, same sign as the measured angle; valid ±780°, clipped to ±500° |

Everything else in the frame (opendbc `DRIVE`, `COUNTER`, `CHECKSUM`, `TORQUE`, `LANE_DEPARTURE`, `unknown*`) is
ignored by this EPS [ECU]. Other EPS generations may check counter/checksum, so keep sending valid values.

---

## 3. LKA behaviour inside the EPS

### 3.1 `EPS_STATE_LKA` (0x495)
0 Unauthorised, 1 Authorised, 2 Available, 3 Active, 4 Defect.

Entry conditions (all required) [ECU]:
- LXA coded in the variant coding.
- ESP on and not regulating.
- Full assist (no thermal/voltage derating).
- Driver torque below the override threshold.
- Valid 0x38D / 0x34D / 0x50D / 0x305 / 0x3F2.
- EPS in its normal operating mode.
- The driver has held the wheel at least once (≥ 0.7 Nm). Hands-on detection is disabled below 10 km/h, so after power-up LKA may not arm until hands are detected above 10 km/h [ECU].
- There is no minimum speed [CAL].

Defect causes:
- Recoverable: CAN validity problems, cleared after 10 good frames.
- **Latched until ignition cycle:** the safety monitor faults in 3.3, and overlap of LKA with park assist [ECU].

### 3.2 Angle → torque
`SET_ANGLE` → clip ±500° → speed-dependent saturation and setpoint rate limit → 2 Hz low-pass → PD/PID servo
(≈0.5 Nm/°) × `TORQUE_FACTOR` (smoothed over 50 ms, slew-limited to ~1.1/s) → clip to **±3 motor-Nm (~60 Nm at the
wheel) at every speed** [CAL]. This torque is **added** to normal assist:
assist, damping, friction compensation and active pull stay on, and only return-to-centre fades out.
- Ramp-in to full authority takes 1–2 s; ramp-out takes 0.2 s.
- EPS-side setpoint rate limit is about 100 °/s at standstill down to about 8 °/s at 200 km/h. openpilot's current limits
  (50 / 30 / 4 °/s at 0 / 18 / 90 km/h, sent at 20 Hz) are well inside this. The 90 km/h value is very conservative.
- Response: roughly a 100 ms first-order lag, plus the 2 Hz filter.

### 3.3 Override, hands-on, latches

| Mechanism | Threshold | Effect |
|---|---|---|
| openpilot `steeringPressed` | 0.5 Nm on 0x2F5 | correct scale |
| Override | ≥ 3 Nm, or fast wheel motion (~35 °/s) | inhibit 10 s |
| Ramp-out | > 2.8 Nm for 20 ms | ramp to zero |
| EPS state handler | filtered 5 Nm, immediate | exit + 200 ms fade, re-arm blocked 10 s (≥ 20 km/h) … 20 s (0 km/h) [CAL] |
| Safety monitor | raw > 5 Nm for 240 ms while LKA torque ≠ 0 | **latched Defect** [CAL] |
| Safety monitor | torque change > 5 Nm within 0.5 s while LKA torque ≠ 0 | **latched Defect** [CAL] |
| Safety monitor | wheel speed above ~25 rad/s (≤ 70 km/h) … 9 rad/s (200 km/h) | **latched Defect** [CAL] |
| Safety monitor | LKA torque > clamp | **latched Defect** [CAL] |
| Actual-angle monitor | \|angle\| ≥ limit(speed) for 200 ms | LKA off, re-arm blocked [CAL] |

Hands-on is detected from torque only and is reported only as `STEERWHL_HOLD_BY_DRV`. The 0x495 frame comes at 10 Hz,
so openpilot sees state changes up to 100 ms late.

### 3.4 Thermal
The motor torque cap is lowered by thermal models with time constants from seconds to over an hour [CAL]:
- holding a large torque derates within minutes;
- light continuous steering derates after tens of minutes;
- thermal state resets at power-up.

Derating blocks LKA entry. It is visible as `0x795 ETAT_ASSIST_DA = 2`.

### 3.5 Stop & Start
- At standstill the EPS asks for an engine restart (`DDE_REDEM_DA`) if driver torque exceeds 4.5 Nm, wheel speed exceeds 300 °/s, or angle exceeds 100°.
- Steering at a stop can restart the engine.
- Avoid a non-zero `TORQUE_FACTOR` at standstill: the EPS's own fade factor is 0 at 0 km/h, so the overlay freezes instead of fading [CAL].

### 3.6 Steering angle source
CMP cars may have:
- a physical sensor;
- a "virtual" sensor: the EPS measures the column angle (even key-off) and adds an offset from the ESC (0x5CD), adopted only below 3 km/h, 3 °/s and 0.3 Nm.

0x305 `ANGLE` is 0x7FFF until the absolute position is known. `FLG_INIT_AVOL`, `FLG_AVOL_ICN` and `ANGLE_VOLANT_ORIGINE` tell
the state; openpilot could gate engagement on them [ECU].

---

## 4. EPS hardware and calibration facts
- Column EPS with a brushless motor. Motor-to-handwheel ratio 22:1 (torque ratio 20), torsion bar 2.5 Nm/°.
- Motor torque limit 4.6 Nm (~93 Nm at the column); thermal cap 2.7 Nm [CAL].
- One software covers several bodies, engines and gearboxes: 5 tuning sets selected by variant coding, × 3 drive-mode personalities.
  Per car, the following vary: LKA coded or not, angle source, LKA limits and servo gains, lock-to-lock angle, steer ratio.
- `steerRatio` is not available from the EPS. Keep the learned value.
- Known EPS HW part numbers: 9828309580, 9828309680, 9828404980.

---

## 5. Diagnostics and fingerprinting
- Physical UDS: request **0x6B5**, response **0x695** (rx offset −0x20, same scheme as the ARTIV radar); functional 0x7FF.
- ISO-TP: normal 11-bit addressing, **unpadded** (padded frames are accepted), BS 0, STmin 10 ms.
- Readable in the **default session without security**, also while driving:
  - **F0FE**: identification zone, 24 B. supplier code 0x13, system code 0x6A = EPS, SW version/edition, download date, cal file number.
  - **F080**: authentication zone, 22 B. Functional part number (BCD), supplier, SW/cal versions, HW version.
  - **F180** (boot SW), **F18C** (serial).
- **opendbc's current placeholder query (DID F181) is not supported by this EPS** and will get a negative response.
- Proposed opendbc request:
  ```python
  Request([b'\x22\xf0\xfe'], [b'\x62\xf0\xfe'], whitelist_ecus=[Ecu.eps], rx_offset=-0x20, bus=0)
  # FW_VERSIONS address for the EPS: (0x6B5, None)
  ```
  The responses are binary, so the `\d{9}` version regex needs a PSA-specific parser.
- Useful live-data DIDs:

  | DID | Content |
  |---|---|
  | D40D | absolute handwheel angle (0.1°) |
  | D40F | handwheel torque (0.1 Nm) |
  | D417 | LKA/park angle setpoint |
  | D419 | LKA function request |
  | D41A | LKA factor |
  | D41B / D41C | LKA state and active tuning set (order unconfirmed) |
  | D403 / D404 / D405 | speed / battery / temperature |

- Variant coding: **DID 2101**. Byte 1 bit 5 = LXA (LKA), bit 4 = multimode, bit 2 = Stop&Start, bit 0 = CityPark; byte 2 = angle-source variant.
  Reading it shows whether a car's EPS is coded for LKA. Writing it needs an extended session and security access.
- DTCs related to 0x3F2 on other EPS generations: U1118-87 (missing), U1218-81 (invalid signal), U1318-08 (frame error).
- XCP (0x7AE/0x7B0) exists but is **disabled at startup on production ECUs**.

---

## 6. opendbc status

An opendbc branch implements:
- **DBC (`0x305`):** rate ×4; checksum and counter named so they are checked; angle validity flags.
- **DBC (`0x2F5`):** driver torque in Nm; new status signals.
- **DBC (`0x3F2`):** `DMD_DELEST_DA`.
- **DBC (`0x495`):** renames to `DRIVER_TORQUE` and `DDE_REDEM_DA`.
- **DBC (`0x795`):** new message.
- **Car code:** 0x305 XOR checksum in `psa_checksum`.
- **Safety:** checksum and counter checks for 0x2F5 and 0x305; TX blocked when `DMD_DELEST_DA` = 1.
- **Validation:** all of it was checked on the 208 route; panda accepts 100% of frames and the parser stays valid.

Still to do:
1. Carcontroller override handling: release before 3 Nm; consider `STATUS = 1` on disengage.
2. Alerts for persistent `EPS_STATE_LKA = 4` ("restart car"), the 10–20 s post-override hold-off, and `ETAT_ASSIST_DA = 2`.
3. Revisit the highway angle-rate limits toward the EPS envelope. Optionally send 0x3F2 at 50 Hz with per-frame limits rescaled.
4. FW query as in §5, once a real F0FE/F080 response is captured.
5. Gate engagement on the 0x305 angle validity flags.

---

## 7. On-car experiments that would settle the open questions
1. Read F0FE, F080, 2101 and D41B/D41C on several CMP models to build a variant table.
2. Ramp the angle slowly at 10/50/100 km/h and note where `EPS_STATE_LKA` leaves 3. This gives the real actual-angle limit and setpoint rate limit.
3. Grab test: log the torque profile against `EPS_STATE_LKA` to confirm the latch window.
4. Gaps in 0x3F2 (60/150/250 ms): confirm the 200 ms fault and 10-frame requalification.
5. Log 0x115 and 0x795, and check the driver-torque sign against the angle sign.
6. Verify the 0x3CD and 0x412 bits 30–31 layouts against opendbc.

## 8. Open questions
- Production values of all [CAL] numbers.
- Which CMP models have LKA coded, and their angle source.
- Whether other EPS software versions check the 0x3F2 counter/checksum.
