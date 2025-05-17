# ECU Firmware Query

## Summary

| ECU Name  | CAN Tx Addr | CAN Rx Addr | Bus | ECU Serial Number        | Manufacturing Date | Notes                  |
|-----------|-------------|-------------|-----|---------------------------|---------------------|----------------------|
| ARTIV     | 0x6B6       | 0x696       | 1   | 212053276                | 0x180521 (21.05.18) | Radar                |
| DIRECTN   | 0x6B5       | 0x695       | 0   | 6077GC0817309            | 0x070615 (15.06.07) |              |
| CMM_E/HCU2| 0x6A6       | 0x686       | 0   | 210306062100             | 0x060321 (21.03.06) |              |
| MSB       | 0x6B4       | 0x694       | 0   | 521021900860             | 0x110121 (21.01.11) |              |
| VCU       | 0x6A2       | 0x682       | 0   | 9210126909               | 0x170521 (21.05.17) |              |
| ABRASR    | 0x6AD       | 0x68D       | 0   | 085095700857210527       | 0x270521 (21.05.27) |              |


## ARTIV (Radar ECU)

python panda/examples/query_fw_versions.py --addr 6b6 --bus 1 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b6, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b6 0x3e00
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x023e000000000000
CAN-RX: 0x696 - 0x027e00
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7e00
ISO-TP: REQUEST - 0x6b6 0x1001
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0210010000000000
CAN-RX: 0x696 - 0x06500100c80014
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x500100c80014
ISO-TP: REQUEST - 0x6b6 0x1003
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0210030000000000
CAN-RX: 0x696 - 0x06500300c80014
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x500300c80014
ISO-TP: REQUEST - 0x6b6 0x22f180
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18000000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f181
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18100000000
ISO-TP: REQUEST - 0x6b6 0x22f182
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18200000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f183
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18300000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f184
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18400000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f185
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18500000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f186
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18600000000
ISO-TP: REQUEST - 0x6b6 0x22f187
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18700000000
ISO-TP: REQUEST - 0x6b6 0x22f188
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18800000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f189
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18900000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18a
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18a00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18b
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18b00000000
CAN-RX: 0x696 - 0x0662f18b180521
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x62f18b180521
ISO-TP: REQUEST - 0x6b6 0x22f18c
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18c00000000
CAN-RX: 0x696 - 0x100c62f18c323132
ISO-TP: RX - first frame - 0x696 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b6
CAN-TX: 0x6b6 - 0x3000000000000000
CAN-RX: 0x696 - 0x21303533323736
ISO-TP: RX - consecutive frame - 0x696 idx=1 done=True
ISO-TP: RESPONSE - 0x696 0x62f18c323132303533323736
ISO-TP: REQUEST - 0x6b6 0x22f18d
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18d00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f18e
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f18e00000000
ISO-TP: REQUEST - 0x6b6 0x22f190
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19000000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f191
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19100000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f192
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19200000000
ISO-TP: REQUEST - 0x6b6 0x22f193
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19300000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f194
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19400000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f195
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19500000000
ISO-TP: REQUEST - 0x6b6 0x22f196
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19600000000
ISO-TP: REQUEST - 0x6b6 0x22f197
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19700000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f198
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19800000000
ISO-TP: REQUEST - 0x6b6 0x22f199
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19900000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19a
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19a00000000
ISO-TP: REQUEST - 0x6b6 0x22f19b
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19b00000000
ISO-TP: REQUEST - 0x6b6 0x22f19c
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19c00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19d
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19d00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19e
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19e00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
ISO-TP: REQUEST - 0x6b6 0x22f19f
ISO-TP: TX - single frame - 0x6b6
CAN-TX: 0x6b6 - 0x0322f19f00000000
CAN-RX: 0x696 - 0x037f2231
ISO-TP: RX - single frame - 0x696 idx=0 done=True
ISO-TP: RESPONSE - 0x696 0x7f2231
0x6b6, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:02<00:00,  2.84s/it]


*** Results for address 0x6B6 ***


0xF18B ECU_MANUFACTURING_DATE: b'\x18\x05!'
0xF18C ECU_SERIAL_NUMBER: b'212053276'


## DIRECTN

python panda/examples/query_fw_versions.py --addr 6b5 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b5, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b5 0x3e00
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x023e000000000000
CAN-RX: 0x695 - 0x027e00
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7e00
ISO-TP: REQUEST - 0x6b5 0x1001
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0210010000000000
CAN-RX: 0x695 - 0x06500100c80014
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x500100c80014
ISO-TP: REQUEST - 0x6b5 0x1003
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0210030000000000
CAN-RX: 0x695 - 0x06500300c80014
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x500300c80014
ISO-TP: REQUEST - 0x6b5 0x22f180
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18000000000
CAN-RX: 0x695 - 0x101062f180010906
ISO-TP: RX - first frame - 0x695 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b5
CAN-TX: 0x6b5 - 0x3000000000000000
CAN-RX: 0x695 - 0x210f0f0f0f0f0f08
ISO-TP: RX - consecutive frame - 0x695 idx=1 done=False
CAN-RX: 0x695 - 0x22000201
ISO-TP: RX - consecutive frame - 0x695 idx=2 done=True
ISO-TP: RESPONSE - 0x695 0x62f1800109060f0f0f0f0f0f08000201
ISO-TP: REQUEST - 0x6b5 0x22f181
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18100000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f182
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18200000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f183
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18300000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f184
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18400000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f185
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18500000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f186
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18600000000
CAN-RX: 0x695 - 0x0462f18603
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x62f18603
ISO-TP: REQUEST - 0x6b5 0x22f187
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18700000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f188
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18800000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f189
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18900000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18a
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18a00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18b
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18b00000000
CAN-RX: 0x695 - 0x0662f18b070615
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x62f18b070615
ISO-TP: REQUEST - 0x6b5 0x22f18c
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18c00000000
CAN-RX: 0x695 - 0x101062f18c363037
ISO-TP: RX - first frame - 0x695 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b5
CAN-TX: 0x6b5 - 0x3000000000000000
CAN-RX: 0x695 - 0x2137474330383137
ISO-TP: RX - consecutive frame - 0x695 idx=1 done=False
CAN-RX: 0x695 - 0x22333039
ISO-TP: RX - consecutive frame - 0x695 idx=2 done=True
ISO-TP: RESPONSE - 0x695 0x62f18c36303737474330383137333039
ISO-TP: REQUEST - 0x6b5 0x22f18d
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18d00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f18e
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f18e00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f190
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19000000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f191
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19100000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f192
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19200000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f193
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19300000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f194
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19400000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f195
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19500000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f196
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19600000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f197
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19700000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f198
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19800000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f199
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19900000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19a
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19a00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19b
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19b00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19c
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19c00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19d
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19d00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19e
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19e00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
ISO-TP: REQUEST - 0x6b5 0x22f19f
ISO-TP: TX - single frame - 0x6b5
CAN-TX: 0x6b5 - 0x0322f19f00000000
CAN-RX: 0x695 - 0x037f2231
ISO-TP: RX - single frame - 0x695 idx=0 done=True
ISO-TP: RESPONSE - 0x695 0x7f2231
0x6b5, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.44s/it]


*** Results for address 0x6B5 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'\x01\t\x06\x0f\x0f\x0f\x0f\x0f\x0f\x08\x00\x02\x01'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x07\x06\x15'
0xF18C ECU_SERIAL_NUMBER: b'6077GC0817309'


## CMM_E/HCU2

python panda/examples/query_fw_versions.py --addr 6a6 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6a6, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6a6 0x3e00
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x023e000000000000
CAN-RX: 0x686 - 0x027e00
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7e00
ISO-TP: REQUEST - 0x6a6 0x1001
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0210010000000000
CAN-RX: 0x686 - 0x06500100c80014
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x500100c80014
ISO-TP: REQUEST - 0x6a6 0x1003
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0210030000000000
CAN-RX: 0x686 - 0x06500300c80014
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x500300c80014
ISO-TP: REQUEST - 0x6a6 0x22f180
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18000000000
CAN-RX: 0x686 - 0x100d62f180000000
ISO-TP: RX - first frame - 0x686 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a6
CAN-TX: 0x6a6 - 0x3000000000000000
CAN-RX: 0x686 - 0x2100000000000000
ISO-TP: RX - consecutive frame - 0x686 idx=1 done=True
ISO-TP: RESPONSE - 0x686 0x62f18000000000000000000000
ISO-TP: REQUEST - 0x6a6 0x22f181
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18100000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f182
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18200000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f183
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18300000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f184
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18400000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f185
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18500000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f186
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18600000000
CAN-RX: 0x686 - 0x0462f18603
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x62f18603
ISO-TP: REQUEST - 0x6a6 0x22f187
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18700000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f188
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18800000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f189
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18900000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18a
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18a00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18b
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18b00000000
CAN-RX: 0x686 - 0x0662f18b060321
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x62f18b060321
ISO-TP: REQUEST - 0x6a6 0x22f18c
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18c00000000
CAN-RX: 0x686 - 0x100f62f18c323130
ISO-TP: RX - first frame - 0x686 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a6
CAN-TX: 0x6a6 - 0x3000000000000000
CAN-RX: 0x686 - 0x2133303630363231
CAN-RX: 0x686 - 0x223030
ISO-TP: RX - consecutive frame - 0x686 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x686 idx=2 done=True
ISO-TP: RESPONSE - 0x686 0x62f18c323130333036303632313030
ISO-TP: REQUEST - 0x6a6 0x22f18d
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18d00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f18e
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f18e00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f190
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19000000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f191
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19100000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f192
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19200000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f193
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19300000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f194
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19400000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f195
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19500000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f196
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19600000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f197
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19700000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f198
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19800000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f199
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19900000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19a
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19a00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19b
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19b00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19c
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19c00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19d
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19d00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19e
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19e00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
ISO-TP: REQUEST - 0x6a6 0x22f19f
ISO-TP: TX - single frame - 0x6a6
CAN-TX: 0x6a6 - 0x0322f19f00000000
CAN-RX: 0x686 - 0x037f2231
ISO-TP: RX - single frame - 0x686 idx=0 done=True
ISO-TP: RESPONSE - 0x686 0x7f2231
0x6a6, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.34s/it]


*** Results for address 0x6A6 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'\x00\x00\x00\x00\x00\x00\x00\x00\x00\x00'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x06\x03!'
0xF18C ECU_SERIAL_NUMBER: b'210306062100'


## MSB

python panda/examples/query_fw_versions.py --addr 6b4 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6b4, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6b4 0x3e00
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x023e000000000000
CAN-RX: 0x694 - 0x027e00
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7e00
ISO-TP: REQUEST - 0x6b4 0x1001
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0210010000000000
CAN-RX: 0x694 - 0x06500100c80014
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x500100c80014
ISO-TP: REQUEST - 0x6b4 0x1003
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0210030000000000
CAN-RX: 0x694 - 0x06500300c80014
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x500300c80014
ISO-TP: REQUEST - 0x6b4 0x22f180
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18000000000
CAN-RX: 0x694 - 0x101062f180533930
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x2143303539323031
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
CAN-RX: 0x694 - 0x22303236
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f18053393043303539323031303236
ISO-TP: REQUEST - 0x6b4 0x22f181
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18100000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f182
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18200000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f183
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18300000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f184
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18400000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f185
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18500000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f186
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18600000000
CAN-RX: 0x694 - 0x0462f18603
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x62f18603
ISO-TP: REQUEST - 0x6b4 0x22f187
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18700000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f188
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18800000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f189
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18900000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18a
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18a00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18b
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18b00000000
CAN-RX: 0x694 - 0x0662f18b110121
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x62f18b110121
ISO-TP: REQUEST - 0x6b4 0x22f18c
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18c00000000
CAN-RX: 0x694 - 0x100f62f18c353231
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x2130323139303038
CAN-RX: 0x694 - 0x223630
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f18c353231303231393030383630
ISO-TP: REQUEST - 0x6b4 0x22f18d
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18d00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f18e
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f18e00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f190
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19000000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f191
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19100000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f192
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19200000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f193
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19300000000
CAN-RX: 0x694 - 0x101462f193383130
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x213232312d303030
CAN-RX: 0x694 - 0x22383056312e3120
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f1933831303232312d303030383056312e3120
ISO-TP: REQUEST - 0x6b4 0x22f194
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19400000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f195
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19500000000
CAN-RX: 0x694 - 0x101462f195413042
ISO-TP: RX - first frame - 0x694 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6b4
CAN-TX: 0x6b4 - 0x3000000000000000
CAN-RX: 0x694 - 0x214d55433035394b
CAN-RX: 0x694 - 0x2233364356323000
ISO-TP: RX - consecutive frame - 0x694 idx=1 done=False
ISO-TP: RX - consecutive frame - 0x694 idx=2 done=True
ISO-TP: RESPONSE - 0x694 0x62f1954130424d55433035394b33364356323000
ISO-TP: REQUEST - 0x6b4 0x22f196
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19600000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f197
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19700000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f198
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19800000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f199
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19900000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19a
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19a00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19b
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19b00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19c
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19c00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19d
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19d00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19e
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19e00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
ISO-TP: REQUEST - 0x6b4 0x22f19f
ISO-TP: TX - single frame - 0x6b4
CAN-TX: 0x6b4 - 0x0322f19f00000000
CAN-RX: 0x694 - 0x037f2231
ISO-TP: RX - single frame - 0x694 idx=0 done=True
ISO-TP: RESPONSE - 0x694 0x7f2231
0x6b4, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.58s/it]


*** Results for address 0x6B4 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'S90C059201026'
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x11\x01!'
0xF18C ECU_SERIAL_NUMBER: b'521021900860'
0xF193 SYSTEM_SUPPLIER_ECU_HARDWARE_VERSION_NUMBER: b'810221-00080V1.1 '
0xF195 SYSTEM_SUPPLIER_ECU_SOFTWARE_VERSION_NUMBER: b'A0BMUC059K36CV20\x00'

## VCU

python panda/examples/query_fw_versions.py --addr 6a2 --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6a2, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6a2 0x3e00
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x023e000000000000
CAN-RX: 0x682 - 0x027e00
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7e00
ISO-TP: REQUEST - 0x6a2 0x1001
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0210010000000000
CAN-RX: 0x682 - 0x06500100c80014
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x500100c80014
ISO-TP: REQUEST - 0x6a2 0x1003
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0210030000000000
CAN-RX: 0x682 - 0x06500300c80014
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x500300c80014
ISO-TP: REQUEST - 0x6a2 0x22f180
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18000000000
CAN-RX: 0x682 - 0x102762f180564538
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x21305f4c5f32375f
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=False
CAN-RX: 0x682 - 0x2230392d344d2020
ISO-TP: RX - consecutive frame - 0x682 idx=2 done=False
CAN-RX: 0x682 - 0x2320202056453830
ISO-TP: RX - consecutive frame - 0x682 idx=3 done=False
CAN-RX: 0x682 - 0x242d534552202020
ISO-TP: RX - consecutive frame - 0x682 idx=4 done=False
CAN-RX: 0x682 - 0x252020202020
ISO-TP: RX - consecutive frame - 0x682 idx=5 done=True
ISO-TP: RESPONSE - 0x682 0x62f180564538305f4c5f32375f30392d344d2020202020564538302d5345522020202020202020
ISO-TP: REQUEST - 0x6a2 0x22f181
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18100000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f182
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18200000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f183
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18300000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f184
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18400000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f185
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18500000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f186
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18600000000
CAN-RX: 0x682 - 0x0462f18603
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x62f18603
ISO-TP: REQUEST - 0x6a2 0x22f187
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18700000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f188
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18800000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f189
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18900000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18a
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18a00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18b
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18b00000000
CAN-RX: 0x682 - 0x0662f18b170521
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x62f18b170521
ISO-TP: REQUEST - 0x6a2 0x22f18c
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18c00000000
CAN-RX: 0x682 - 0x100d62f18c393231
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x2130313236393039
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=True
ISO-TP: RESPONSE - 0x682 0x62f18c39323130313236393039
ISO-TP: REQUEST - 0x6a2 0x22f18d
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18d00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f18e
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f18e00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f190
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19000000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f191
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19100000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f192
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19200000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f193
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19300000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f194
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19400000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f195
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19500000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f196
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19600000000
CAN-RX: 0x682 - 0x101362f196484f4d
ISO-TP: RX - first frame - 0x682 idx=0 done=False
ISO-TP: TX - flow control continue - 0x6a2
CAN-TX: 0x6a2 - 0x3000000000000000
CAN-RX: 0x682 - 0x212d303030343532
ISO-TP: RX - consecutive frame - 0x682 idx=1 done=False
CAN-RX: 0x682 - 0x22000000000000
ISO-TP: RX - consecutive frame - 0x682 idx=2 done=True
ISO-TP: RESPONSE - 0x682 0x62f196484f4d2d303030343532000000000000
ISO-TP: REQUEST - 0x6a2 0x22f197
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19700000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f198
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19800000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f199
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19900000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19a
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19a00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19b
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19b00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19c
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19c00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19d
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19d00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19e
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19e00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
ISO-TP: REQUEST - 0x6a2 0x22f19f
ISO-TP: TX - single frame - 0x6a2
CAN-TX: 0x6a2 - 0x0322f19f00000000
CAN-RX: 0x682 - 0x037f2231
ISO-TP: RX - single frame - 0x682 idx=0 done=True
ISO-TP: RESPONSE - 0x682 0x7f2231
0x6a2, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.32s/it]


*** Results for address 0x6A2 ***


0xF180 BOOT_SOFTWARE_IDENTIFICATION: b'VE80_L_27_09-4M     VE80-SER        '
0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b'\x17\x05!'
0xF18C ECU_SERIAL_NUMBER: b'9210126909'
0xF196 EXHAUST_REGULATION_OR_TYPE_APPROVAL_NUMBER: b'HOM-000452\x00\x00\x00\x00\x00\x00'

## ABRASR (Dash error on query)

python panda/examples/query_fw_versions.py --addr 6ad --bus 0 --rxoffset -20 --no-obd --debug
INFO: connecting to panda 020026000151323431333839
querying addresses ...
0x6ad, None:   0%|                                                                                                               | 0/1 [00:00<?, ?it/s]ISO-TP: REQUEST - 0x6ad 0x3e00
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x023e000000000000
CAN-RX: 0x68d - 0x027e00
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7e00
ISO-TP: REQUEST - 0x6ad 0x1001
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0210010000000000
CAN-RX: 0x68d - 0x06500100c80014
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x500100c80014
ISO-TP: REQUEST - 0x6ad 0x1003
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0210030000000000
CAN-RX: 0x68d - 0x037f1078
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f1078
UDS-RX: response pending
CAN-RX: 0x68d - 0x06500300c80014
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x500300c80014
ISO-TP: REQUEST - 0x6ad 0x22f180
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18000000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f181
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18100000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f182
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18200000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f183
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18300000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f184
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18400000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f185
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18500000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f186
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18600000000
CAN-RX: 0x68d - 0x0462f18603
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18603
ISO-TP: REQUEST - 0x6ad 0x22f187
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18700000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f188
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18800000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f189
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18900000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18a
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18a00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18b
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18b00000000
CAN-RX: 0x68d - 0x0662f18b270521
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18b270521
ISO-TP: REQUEST - 0x6ad 0x22f18c
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18c00000000
CAN-RX: 0x68d - 0x101562f18c303835
ISO-TP: RX - first frame - 0x68d idx=0 done=False
ISO-TP: TX - flow control continue - 0x6ad
CAN-TX: 0x6ad - 0x3000000000000000
CAN-RX: 0x68d - 0x2130393537303038
CAN-RX: 0x68d - 0x2235373231303532
ISO-TP: RX - consecutive frame - 0x68d idx=1 done=False
ISO-TP: RX - consecutive frame - 0x68d idx=2 done=False
CAN-RX: 0x68d - 0x2337
ISO-TP: RX - consecutive frame - 0x68d idx=3 done=True
ISO-TP: RESPONSE - 0x68d 0x62f18c303835303935373030383537323130353237
ISO-TP: REQUEST - 0x6ad 0x22f18d
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18d00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f18e
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f18e00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f190
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19000000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f191
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19100000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f192
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19200000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f193
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19300000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f194
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19400000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f195
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19500000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f196
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19600000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f197
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19700000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f198
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19800000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f199
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19900000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19a
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19a00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19b
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19b00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19c
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19c00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19d
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19d00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19e
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19e00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
ISO-TP: REQUEST - 0x6ad 0x22f19f
ISO-TP: TX - single frame - 0x6ad
CAN-TX: 0x6ad - 0x0322f19f00000000
CAN-RX: 0x68d - 0x037f2231
ISO-TP: RX - single frame - 0x68d idx=0 done=True
ISO-TP: RESPONSE - 0x68d 0x7f2231
0x6ad, None: 100%|███████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:01<00:00,  1.46s/it]


*** Results for address 0x6AD ***


0xF186 ACTIVE_DIAGNOSTIC_SESSION: b'\x03'
0xF18B ECU_MANUFACTURING_DATE: b"'\x05!"
0xF18C ECU_SERIAL_NUMBER: b'085095700857210527'

