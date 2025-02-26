# Openpilot-PSA

A resource collection for porting PSA (Peugeot, Citroën, DS, Opel/Vauxhall) vehicles to Openpilot.

## Contents
- [Introduction](#introduction)
- [Working BSI Harness](#working-bsi-harness)
- [Compatible Vehicles](#compatible-vehicles)
- [Diagnostic Tools](#diagnostic-tools)
- [Reference Information](#reference-information)
  - [Camera Harness](#camera-harness-reference-only)
  - [Test Routes](#test-routes)
  - [PSA Platforms](#psa-platforms)

## Introduction

This repository provides information and resources for integrating Openpilot with PSA (now part of Stellantis) vehicles. The primary focus is on the BSI (Body System Interface) harness, which is the working solution for connecting Openpilot to PSA vehicles.

## Working BSI Harness

The BSI (Body System Interface) harness is the **currently working solution** for connecting Openpilot to PSA vehicles.

### Connector Information
The 60-pin connectors are mechanically coded. Black EP connector is used for the harness.

| Connector | Pins | Manufacturer | Part |
|-----------|------|--------------|------|
| EP (black) | 60 | Aptiv (Formerly Delphi) | 13854846 |
| Terminal options | - | Aptiv | F070300 (brown)<br>F170300 (blue)<br>F270300 (white) |
| Socket alternative | - | HD Connector | HD601-0.6-11J |
| Pins alternative | - | TE Connectivity | 144969-1 |

### Harness Schematic
![BSI Harness Schematic](https://github.com/user-attachments/assets/79f9d5f1-1354-4987-b83a-f59119794af0)

[Download Schematic PDF](https://github.com/user-attachments/files/18695226/harness.pdf)

## Compatible Vehicles

The following table shows PSA vehicles with known BSI unit information. These are potential candidates for Openpilot integration.

| Model | Platform | BSI Name | HW | SW | Part Number |
|-------|----------|----------|----|----|-------------|
| Citroen Berlingo | EMP2 | BSI-EL3-CEM00 | D6 | 6.05 | 9830707680-00 |
| Citroen C3 III | PF1 | BSI-EL3-CEM00 | D6 | 6.05 | 9830790580-00 |
| Citroen C3 Aircross | PF1 | BSI-EL5-CEM00 | D7 | 7.10 | 9832880680-00 |
| Citroen C4 III | CMP | BSI-EI4-CEM00 | D7 | 7.09 | 9832881080-00 |
| Citroen ë-C4 | CMP | BSI-EI4-CEM00 | D7 | 7.09 | 9832881080-00 |
| Citroen C5 Aircross | EMP2 | BSI-EI5-CEM00 | D6 | 6.05 | 9830813080-00 |
| Citroen Jumpy | EMP2 | BSI-EL3-CEM00 | D7 | 7.11 | 9845141280-00 |
| DS 3 Crossback (E-Tense) | CMP | BSI-EL4-CEM00 | D6 | 6.05 | 9830707780-00 |
| DS 4 | EMP2 | BSI-Q04-01 | ? | ? | 9806687980 01 |
| DS 7 Crossback | EMP2 | BSI-EL5-CEM00 | D6 | 6.05 | 9830805680-00 |
| Jeep Avenger | CMP2 | BSI-EI4-CEM00 | D7 | 7.09 | 9832881080-00 |
| Opel Corsa(e) | CMP | BSI-EL4-CEM00 | D6 | 6.05 | 9830707780-00 |
| Opel Corsa(e) | CMP | BSI-EI4-CEM00 | D6 | 6.05 | 9830708180-00 |
| Opel Combo | EMP2 | BSI-EL3-CEM00 | D6 | 6.05 | 9830790580-00 |
| Opel Grandland | EMP2 | BSI-EL3-CEM00 | D6 | 6.05 | 9830790580-00 |
| Opel Mokka(e) | CMP | BSI-EI4-CEM00 | D7 | 7.09 | 9832881080-00 |
| Opel Vivaro | EMP2 | BSI-EL3-CEM00 | D6 | 6.05 | 9830790580-00 |
| Peugeot (e)208 / (e)2008 | CMP | BSI-EI4-CEM00 | D6 | 6.05 | 9830708180-00 |
| Peugeot (e)208 / (e)2008 | CMP | BSI-EI4-CEM00 | D7 | 7.51 | 9846483980-00 |
| Peugeot (e)308 III | EMP2 | BSI-Q03-01 | ? | ? | ? |
| Peugeot 508 | EMP2 | BSI-Q04-01 | ? | ? | 9806687980 01 |

*Note: (e) indicates models with electric variants*

## Diagnostic Tools

These tools can help with vehicle diagnostics and development:

- [Arduino PSA Diag Sketch](https://github.com/ludwig-v/arduino-psa-diag) - Arduino-based diagnostic tool for PSA vehicles
- [Diagnostique Tool](https://bitbucket.org/thoste5/diagnostique/src/master/) - Software for vehicle diagnostics

## Reference Information

### Camera Harness (Reference Only)

**Note: The camera harness is currently NOT WORKING and is provided for reference only. The camera does not directly command the EPS, and further development is needed.**

Camera connector pinout:

| Pin | Name | Color |
|-----|------|-------|
| 1 | GND | Green-Yellow |
| 4 | HS2 LOW | Purple |
| 5 | HS2 HIGH | Green |
| 8 | HS1 HIGH | Pink |
| 9 | HS1 HIGH | Orange |
| 12 | +12VDC | Grey |

![Camera Harness](https://github.com/user-attachments/assets/f65708d8-3114-4cde-9d2c-d535112ebe76)

Camera connector parts:

| Item | Manufacturer | Part Numbers |
|------|--------------|--------------|
| Connector | TE Connectivity | 1379095-2 |
| Terminal | TE Connectivity | 1379219-1 |
| Pins | TE Connectivity | 144969-1 |
| Socket alternatives | TE Connectivity | 1379114-2, 185740-2, 1379030-1, 953130-2 |

### Test Routes

- **Camera Harness Test**: 6a7075a4fdd765ee/00000011--7c1eb240a9
- **Joystick Mode Test**: 6a7075a4fdd765ee/000000ae--89b2f237b5
- **Dashcam Mode - Lane Departure**: 6a7075a4fdd765ee/00000052--dbdeef811e

### PSA Platforms

Major PSA vehicle platforms and their associated models:

| Platform | Description |
|----------|-------------|
| CMP/e-CMP | Common Modular Platform for compact vehicles (ICE and electric) |
| EMP2/eVMP | Efficient Modular Platform for mid-size vehicles |
| Smart Car Platform | For entry-level vehicles, developed with Tata Consultancy Services |
| STLA Medium | New platform for mid-size electric vehicles |

*For a detailed list of vehicles by platform, refer to the [PSA Platforms Wiki](https://en.wikipedia.org/wiki/Common_Modular_Platform).*
