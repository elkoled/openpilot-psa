# PSA test routes

Routes worth keeping for porting, tuning and regression checks. Checked in November 2026.

- **rlog**: full logs available (every CAN frame). Needed for counter, timing and safety replay.
- **qlog**: decimated logs only. Fine for states and signals, not for counters.
- **preserved**: kept on comma connect indefinitely.
- **lat %**: share of the route with openpilot steering.

Every route below was replayed against the 0x432 CAN ignition rule (see [eps_cmp.md](eps_cmp.md) §4.1).
On all of them ignition comes on with the first valid frame, stays on while driving and only goes off at key off.

## Full logs (rlog)

| Route | Car | Branch | Segs | lat % | Max km/h | Notes |
|---|---|---|---|---|---|---|
| `4cef1f7eba322b25/00000000--dee7de3f20` | 508 (MOCK) | psa | 63 | 0 | 73 | **preserved**. 40 min ignition on with engine off, cranking, a key off while rolling, key off with the network awake, restart |
| `378c9bf47606eb28/0000000a--decc68d4d9` | 208 | psa-torque-2 | 22 | 38 | 121 | **preserved**. Good autobahn lateral tuning route |
| `378c9bf47606eb28/00000019--12b72fae5c` | Berlingo | psa-berlingo | 37 | 25 | 127 | **preserved** |
| `378c9bf47606eb28/00000002--5b692350f3` | Berlingo (MOCK) | psa | 31 | 0 | 130 | **preserved**. Stock behaviour, ends with key off |
| `378c9bf47606eb28/00000001--b85eed4b91` | C4 SpaceTourer | psa-torque-sunny | 26 | 66 | 122 | key off at the end |
| `378c9bf47606eb28/00000008--139b4c1f90` | C4 SpaceTourer | psa-torque-sunny | 28 | 3 | 128 | mostly stock driving |
| `3572c628f9c5a0ef/0000046e--47f9807b24` | 508 (China-built) | psa-sunny | 99 | 81 | 114 | longest engaged rlog route |
| `3572c628f9c5a0ef/00000474--b93ce95a43` | 508 (China-built) | psa-sunny | 56 | 92 | 130 | highest engagement |
| `3572c628f9c5a0ef/00000472--1b11fc5ae3` | 508 (China-built) | psa-sunny | 87 | 57 | 136 | key off at the end |
| `3572c628f9c5a0ef/00000471--f69ce3e7d7` | 508 (China-built) | psa-sunny | 39 | 87 | 148 | highway |
| `3572c628f9c5a0ef/00000470--f5e5de6f58` | 508 (China-built) | psa-sunny | 10 | 85 | 118 | |
| `3572c628f9c5a0ef/00000475--d95b0702e6` | 508 (China-built) | psa-sunny | 24 | 57 | 122 | |
| `3572c628f9c5a0ef/0000046f--29bfe02683` | 508 (China-built) | psa-sunny | 27 | 45 | 132 | key off at the end |
| `3572c628f9c5a0ef/00000473--8729a0e34f` | 508 (China-built) | psa-sunny | 27 | 37 | 96 | |
| `3572c628f9c5a0ef/0000047c--57db4f27ab` | 508 (China-built) | psa-sunny | 24 | 0 | 62 | city, not engaged |
| `3572c628f9c5a0ef/0000047d--d492fe0cb1` | 508 (China-built) | psa-sunny | 11 | 0 | 60 | key off at the end |
| `3572c628f9c5a0ef/0000047e--54fcf8c16b` | 508 (China-built) | psa-sunny | 8 | 0 | 63 | rlogs missing for some segments |
| `0f66637e79696096/000000cf--c60c650fea` | 508 | psa-sunny-deviation | 35 | 77 | 126 | on konik connect. Key off at the end |

The China-built 508 (`3572c628f9c5a0ef`) is the only non-European car with full logs. Its rlogs are not preserved
and will expire, so preserve or download them soon.

## qlog only

| Route | Car | Branch | Segs | lat % | Max km/h | Notes |
|---|---|---|---|---|---|---|
| `a6df478182b4025c/000001cd--18fd03fe05` | 508 | psa-sunny | 179 | 73 | 107 | longest route, 3 h |
| `782c88bd80dc1512/0000011e--a741b3bb34` | Corsa F (as 208) | psa | 106 | 26 | 109 | |
| `3ae5e3d7179aa92c/000001c1--6894aa2158` | Corsa F (as 208) | psa | 74 | 87 | 98 | |
| `3ae5e3d7179aa92c/0000000a--4da2d0bc6b` | Corsa F (as 208) | psa | 71 | 73 | 120 | **preserved** |
| `3ae5e3d7179aa92c/000001b0--5e40c8812a` | Corsa F (MOCK) | psa | 80 | 0 | 116 | **preserved**. Relay open the whole drive |
| `3ae5e3d7179aa92c/000001a9--acc55785fe` | Corsa F (MOCK) | psa | 69 | 0 | 119 | relay open the whole drive |
| `378c9bf47606eb28/00000001--9be9d45f9f` | C4 SpaceTourer | psa-torque-sunny | 72 | 69 | 160 | fastest route |
| `3572c628f9c5a0ef/000003eb--40523f7941` | 508 (China-built) | psa-sunny | 47 | 0 | 139 | |
| `4cef1f7eba322b25/00000073--1dd49d2543` | 508 | psa-sunny | 19 | 63 | 115 | |
| `df4becc685028a3f/0000001d--09b7bf54b9` | 208 | psa-sunny-high | 54 | 80 | 126 | on konik connect |

## Gaps

- No full logs at all for the 308 T9, 5008, 3008 II, DS7 and Corsa F.
- No files left for `564853d6b754a8fe` and the older routes of `782c88bd80dc1512`, `a6df478182b4025c`,
  `3572c628f9c5a0ef` (before October 2026).
- konik connect devices can't be listed without a login, so only the two konik routes above are included.
