# Openpilot-PSA
Information collection for porting PSA vehicles to Openpilot

# Opel Corsa F Port

| Project | Branch            | start commit  | end commit | Link |
| ------- | ----------------- | ------------- | ---------- | ---- |
| Openpilot | opel-corsa-f | 24c4b692beab04aec9f51b1e38d9a64260b1ed91 | c39c564104158e0eb684d8305dc0f491db63a17e |[openpilot](https://github.com/incognitojam/openpilot/tree/opel-corsa-f) |
| Panda | opel-corsa-f | c9a714565d96ed77c2f4d38cc03ce81c1eb9e3b8 | 26a14f7bb52f72b727f5adb39ed26c208acdf2e5 |[panda](https://github.com/incognitojam/panda/tree/opel-corsa-f) |
| Opendbc | aee2010 | 4fbb36b8d4df1fd0c5f13a3ec11b16f4756258d9 | 477746488b785cdead040590921e0b9d3889e1e9 |[opendbc](https://github.com/incognitojam/opendbc/tree/aee2010) |


# Links
- [Power Steering Code for CMP Platform](https://github.com/BusinessEthicsPeopleFirst/EPS_TMS570_PSA_CMP)
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



### Connectors

| Connector         | Pins     | Manufacturer | Part          | Link |
| ----------------- | -------- | ------------ | ------------- | ---- |
| EH1 (brown)<br>EP (black)<br>EPB (blue)<br>EH2 (yellow) | 60       | FCI / Yueqing Haidie Electric | FX01300<br>HD601-0.6-21J<br>Male: HD601-0.6-11J        |[Link](https://yqwakan.com/product_9749_FX01300.html) <br> [Alibaba](https://spanish.alibaba.com/product-detail/60--pin--female--electrical--wire--harness-1600238725189.html) <br> [Male Connector](https://www.hdconnectorstore.com/productdetail/14.html)|
| PAV               | 35       | TE Connectivity / YBADDVANCE | 98495002X    |[Link](https://www.fuelinjector-connectors.com/sale-13281295-98495002x-35-way-te-connectivity-amp-connectors-with-terminals.html)<br>[Alibaba](https://german.alibaba.com/product-detail/98495002X-35-Pin-Female-Cable-Harness-1600084328892.html)|


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
