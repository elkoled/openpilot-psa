# Openpilot-PSA
Information collection for porting PSA vehicles to Openpilot

# Links
- [Arduino PSA Diag Sketch](https://github.com/ludwig-v/arduino-psa-diag)
- [Diagnostique Tool](https://bitbucket.org/thoste5/diagnostique/src/master/)


# Control Units (BSI)
| Model        | Platform | Name          | HW | SW   | Part          | Year     |
| ------------ | -------- |------------- | -- | ---- | ------------- | -------- |
| DS DS3 Crossback<br> Opel Corsa F | CMP | BSI-EL4-CEM00 | D6 | 6.05 | 9830707780-00 | 2019 - ? |
| Peugeot (e)208<br>Peugeot (e)2008<br>Opel Corsa(e) F<br> | (e)CMP | BSI-EI4-CEM00 | D6 | 6.05 | 9830708180-00 | 2019 - ? |
| Opel Grandland | EMP2 | BSI-EL3-CEM00 | D6 | 6.05 | 9830790580-00 | 2020 - ?|
| DS DS7 Crossback | EMP2 | BSI-EL5-CEM00 | D6 | 6.05 | 9830805680-00 | 2019 - ? |
| Opel Mokka-(e) | (e)CMP | BSI-EI4-CEM00 | D7 | 7.09 | 9832881080-00 | 2021 - ? |
| Peugeot (e)208<br>Peugeot (e)2008 | (e)CMP | BSI-EI4-CEM00 | D7 | 7.51 | 9846483980-00 | 2021 - ? |


### BSI Harness
The 60-pin connectors are mechanically coded. Black EP connector is used for the harness.
| Connector         | Pins     | Manufacturer | Part          | Link |
| ----------------- | -------- | ------------ | ------------- | ---- |
| EH1 (brown)<br>EP (black)<br>EPB (blue)<br>EH2 (yellow) | 60       | Aptiv (Formerly Delphi) | F001300<br>13854846<br>F070300<br>F170300<br>F270300<br>HD601-0.6-11J<br>144969-1     |[Connector (Reference)](https://www.mouser.de/ProductDetail/Aptiv-formerly-Delphi/F101300?qs=MLItCLRbWsxWImEpsa78qg%3D%3D) <br> [Connector (Coded)](https://www.mouser.de/ProductDetail/Aptiv-formerly-Delphi/13854846?qs=BJlw7L4Cy7%252BEB11mgqBWgg%3D%3D) <br> [Terminal (brown)](https://www.mouser.de/ProductDetail/Aptiv-formerly-Delphi/F070300?qs=SRYZG9HaIQ2x4f%252Bq7ksEBw%3D%3D) <br> [Terminal (blue)](https://www.mouser.de/ProductDetail/Aptiv-formerly-Delphi/F170300?qs=SRYZG9HaIQ03F834F05UMg%3D%3D) <br> [Terminal (white)](https://www.mouser.de/ProductDetail/Aptiv-formerly-Delphi/F270300?qs=SRYZG9HaIQ3H7TE3kpQvwg%3D%3D) <br>[Socket](https://www.hdconnectorstore.com/productdetail/14.html)<br>[Pins](https://www.mouser.de/ProductDetail/TE-Connectivity/144969-1-Loose-Piece?qs=u4fy%2FsgLU9PzpoIYn7PeTA%3D%3D)|

#### [Schematic](https://github.com/user-attachments/files/18695226/harness.pdf)
![image](https://github.com/user-attachments/assets/79f9d5f1-1354-4987-b83a-f59119794af0)




### Camera Harness
| Connector         | Pins     | Manufacturer | Part          | Link |
| ----------------- | -------- | ------------ | ------------- | ---- |
| Camera   | 12       | TE Connectivity | 1379095-2<br>1379219-1<br>144969-1<br>1379114-2<br>185740-2<br> 1379030-1<br> 953130-2 | [Connector](https://www.mouser.de/ProductDetail/TE-Connectivity-AMP/1379095-2?qs=EVI5SOJzNyfRbrjTeakcGw%3D%3D) <br> [Terminal](https://www.mouser.de/ProductDetail/TE-Connectivity-AMP/1379219-1?qs=GQ3BsEl46pnQAYZB88d5cQ%3D%3D) <br> [Pins](https://eu.mouser.com/ProductDetail/TE-Connectivity/144969-1-Loose-Piece?qs=u4fy%2FsgLU9PzpoIYn7PeTA%3D%3D) <br>[Socket Alt 1](https://www.mouser.de/ProductDetail/TE-Connectivity/1379114-2?qs=GQ3BsEl46pmmzP6tPYGptQ%3D%3D)<br> [Socket Alt 2](https://www.mouser.de/ProductDetail/TE-Connectivity/185740-2?qs=UMrTGIqlm7lDlatQWP7cIw%3D%3D)<br> [Socket Alt 3](https://www.mouser.de/ProductDetail/TE-Connectivity/1379030-1?qs=A9sEIK4flAfIbEP77rK6GA%3D%3D)<br> [Socket Alt 4](https://www.mouser.de/ProductDetail/TE-Connectivity-AMP/953130-2?qs=Q0GhXaox%252BNFZ2KG0Jd%252BK6w%3D%3D)



# Platforms
| Name                | Models                                                                                                                                                                                                                                                                                                                                                                                                                             | Developed by                                  | Wiki                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------|
| CMP                 | Alfa Romeo Junior (2024–present)<br>Lancia Ypsilon (2024–present)<br>Citroën C4 III (2020–present)<br>Citroën C4 X (2022–present)<br>Dongfeng Aeolus Yixuan (2019–present)<br>Dongfeng Aeolus Yixuan GS (2020–present)<br>DS 3 Crossback (2018–present)<br>Fiat 600 (2023–present)<br>Jeep Avenger (2023–present)<br>Opel Corsa F (2019–present)<br>Opel Mokka B (2020–present)<br>Peugeot 208 II (2019–present)<br>Peugeot 2008 II (2019–present) | PSA, Dongfeng                                 | [Link](https://en.wikipedia.org/wiki/Common_Modular_Platform)    |
| e-CMP               | Citroën ë-C4 (2020–present)<br>Citroën ë-C4 X (2022–present)<br>Dongfeng Aeolus Yixuan EV (2019–present)<br>DS 3 Crossback E-Tense (2019–present)<br>Opel Corsa-e (2019–present)<br>Opel Mokka-e (2020–present)<br>Peugeot e-208 (2020–present)<br>Peugeot e-2008 (2019–present)<br>Fiat 600e (2023–present)<br>Jeep Avenger EV (2023–present)<br>Lancia Ypsilon (2024–present)<br>Alfa Romeo Junior (2024–present)                                                   | PSA, Dongfeng                                 | [Link](https://en.wikipedia.org/wiki/Common_Modular_Platform)    |
| EMP2                | Citroën C4 Picasso/Spacetourer II (2013–2020)<br>Citroën Grand C4 Picasso/Spacetourer II (2013–2022)<br>Citroën C6 II (2016–2023)<br>Peugeot 308 II (2013–2021)<br>Peugeot 408 II (2014–present)<br>Citroën C5 Aircross (2017–present)<br>DS 7 Crossback (2017–present)<br>Opel Grandland (2017–present)<br>Peugeot 3008 II (2016–2023)<br>Peugeot 5008 II (2017–2024)<br>DS 9 (2020–present)<br>Peugeot 508 II (2018–present)<br>Citroën C5 X (2021–present)<br>DS 4 II (2021–present)<br>Opel Astra L (2021–present)<br>Peugeot 308 III (2021–present)<br>Peugeot 408 (2022–present)                                   | PSA, Toyota                                  | [Link](https://en.wikipedia.org/wiki/EMP2_platform)              |
| Smart Car Platform  | Citroën C3 (2022–present)<br>Citroën C3 Aircross (2023–present)<br>Citroën C3/e-C3 IV (2024–present)<br>Citroën Basalt (2024–present)<br>Opel Frontera (2024)<br>Fiat Grande Panda (2024–present)<br>Fiat Multipla (2025–present)<br>Fiat Pickup (2025–present)<br>Fiat Fastback (2026–present)                                                                                                                                                                   | Tata Consultancy Services for Stellantis      | [Link](https://en.wikipedia.org/wiki/Common_Modular_Platform#Smart_Car_Platform) |
| K0 Platform         | Citroën Jumpy III (2016–present)<br>Citroën SpaceTourer (2016–present)<br>Peugeot Expert (2016–present)<br>Peugeot Traveller (2016–present)<br>Toyota ProAce (2016–present)<br>Toyota ProAce Verso (2016–present)<br>Opel/Vauxhall Vivaro (2019–present)<br>Opel Zafira Life (2019–present)<br>Fiat Scudo (2022–present)<br>Fiat Ulysse (2022–present)                                                                                              | Stellantis, Toyota                            | [Link](https://en.wikipedia.org/wiki/EMP2_platform#K0_platform)  |
| eVMP                | Peugeot e-308 III (2022–present)<br>Peugeot e-408 (2025–present)<br>Opel Astra-e L (2023–present)                                                                                                                                                                                                                                                                                                                                 | Stellantis                                     | [Link](https://en.wikipedia.org/wiki/EMP2_platform#eVMP)         |
| STLA Medium         | Peugeot e-3008 III (2023–present)<br>Peugeot e-5008 III (2024–present)<br>Opel Grandland II (2024–present)<br>Citroën C5 Aircross (2025, upcoming)<br>Jeep Compass (2025, upcoming)<br>DS 8 (2025, upcoming)<br>Lancia Gamma (2026, upcoming)<br>Alfa Romeo Tonale II (2027, upcoming)<br>Alfa Romeo Giulietta (2028, upcoming)<br>Lancia Delta (2028, upcoming)                                                                                                                                                              | Stellantis                                     | [Link](https://en.wikipedia.org/wiki/EMP2_platform#STLA_Medium)  |
