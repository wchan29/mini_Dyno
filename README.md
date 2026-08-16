# Mini Dyno

Mechanical design files for a compact 10 N·m dynamometer built for the [WEMPEC](https://wempec.wisc.edu/) research lab at UW-Madison.

## Overview

A dynamometer measures the rotational speed and torque output of a motor to determine instantaneous power and efficiency. This project is a bench-scale dynamometer for characterizing small electric machines (up to IEC100 frame size), designed to:

- Fit on a standard lab bench
- House a pre-selected Rockwell Kinetix MP servo as the load motor
- Enclose the test setup for operator protection
- Allow quick installation/removal of test motors with minimal realignment
- Support HMI control from the enclosure door

More background and photos: https://wchan29.github.io/portfolio/wempec_mini_dyne/

## Design

**Mechanical**
- ThorLabs MB3090/M aluminum optical breadboard as the baseplate
- MISUMI L-shaped welded mounts for servo motor attachment
- OptoSigma optical rails and carriages for interchangeable test-motor mounting
- 8020 T-slot aluminum framing for the enclosure
- 1/4" polycarbonate protective panels

**Electrical**
- Servo drive: Allen-Bradley Kinetix 300 (2097-V33PR6, 3 kW)
- Load motor: Rockwell Kinetix MPL-A4540F-MJ74AA (2.6 kW, 3000 RPM)
- HMI: 7" Rockwell PanelView 800 touchscreen mounted on the enclosure door
- Controller: Micro820 PLC over Ethernet
- Supporting hardware: 24V DC power supply, Ethernet hub, brake relay, torque transducer module

**Specs**
- Max torque: 10 N·m
- Max speed: 3000 RPM

The servo and torque transducer are mounted as a swappable unit on the optical rail carriage, so either can be serviced or replaced independently of the rest of the setup.

## Repository contents

All design files live under [`Dyno Enclosure REV_B/`](Dyno%20Enclosure%20REV_B/), a SolidWorks project:

| Folder / File | Contents |
| --- | --- |
| `220 - Dyno Enclosure - 8020/` | T-slot frame, door, and hinge assemblies |
| `220 - Dyno Enclosure - Optical Table/` | Optical breadboard baseplate |
| `220 - Dyno Enclosure - OptoSigma/` | Optical rail and carriage components |
| `220 - Dyno Enclosure - Polycarbonate/` | Enclosure panels |
| `220 - Optical Rail and Carriage/` | Motor mounting carriage hardware |
| `220 - Bracket & Misc/` | Brackets, alignment jig, torque transducer base, couplings |
| `220 - Cable Routing/` | Cable management components |
| `220 - Electronics/` | Electrical/control hardware models |
| `Pictures/` | Reference images |
| `220 - Dyno Enclosure - BOM.SLDDRW` / `..._BOM_PDF.pdf` | Bill of materials |
| `_220 - Dyno Enclosure - Enclosure Full Assembly.SLDASM` | Top-level enclosure assembly |
| `220 - Dyno Setup Assembly.SLDASM` | Top-level full dyno assembly |

Files are native SolidWorks (`.SLDPRT`/`.SLDASM`/`.SLDDRW`), with some parts also provided as `.igs`/`.DXF`/`.pdf` for interchange. Requires SolidWorks (or a compatible viewer) to open.
