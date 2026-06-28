# ESP32-S3-LCD-1.47 Enclosure (ESP-STICK)

A compact enclosure and firmware workspace for the Waveshare
ESP32-S3-LCD-1.47 development board.

The project currently contains the mechanical STEP model for the ESP-STICK
enclosure, reference resources, and a baseline firmware sketch for the SerialSIM
device.

Product reference:
https://www.waveshare.com/wiki/ESP32-S3-LCD-1.47


## Project Status

- Hardware: enclosure STEP files are organized under `hardware/step/`.
- Printable STL exports are organized under `hardware/stl/`.
- Firmware: the current Arduino sketch is under `firmware/SerialSIM/`.

## Features

- Designed around the Waveshare ESP32-S3-LCD-1.47 board.
- Two-part enclosure model with top and bottom shells.
- Assembly STEP file for reviewing the full device.
- Firmware workspace for serial, TCP, and protocol-simulation work.
- Device notes for the SerialSIM target.

## Bill of Materials

| Item | Qty | Part / File | Notes |
|---|---:|---|---|
| ESP32-S3-LCD-1.47 development board | 1 | [Waveshare ESP32-S3-LCD-1.47](https://www.waveshare.com/product/esp32-s3-lcd-1.47.htm) | Target board for the enclosure and firmware. |
| Enclosure top | 1 | [ESP-STICK-ENCLOSURE-TOP.stl](hardware/stl/ESP-STICK-ENCLOSURE-TOP.stl) | Printable top shell. |
| Enclosure bottom | 1 | [ESP-STICK-ENCLOSURE-BOTTOM.stl](hardware/stl/ESP-STICK-ENCLOSURE-BOTTOM.stl) | Printable bottom shell. |
| EDDM-M2-L4 screw | 4 | [JLCMC EDDM-M2-L4](https://jlcmc.com/product/s/E02/EDDM/phillips-ultra-thin-head-screw?k=EDDM-M2-L4&productModelNumber=EDDM-M2-L4) | Mounting hardware for the enclosure assembly. |
| ELSV-S1W-M1.4-L8-S2.5 screw | 4 | [JLCMC ELSV-S1W-M1.4-L8-S2.5](https://jlcmc.com/product/s/E02/ELSV/cross-recessed-precision-electronic-mini-screw?k=ELSV-S1W-M1.4-L8-S2.5&productModelNumber=ELSV-S1W-M1.4-L8-S2.5) | Mounting hardware for the enclosure assembly. |

## Repository Structure

```text
.
├── firmware/
│   ├── README.md
│   └── SerialSIM/
│       ├── DeviceDetails.md
│       └── SerialSIM.ino
├── hardware/
│   ├── README.md
│   ├── assy-bottom.png
│   ├── assy-exploded.png
│   ├── assy-top.png
│   ├── step/
│   │   ├── ESP-STICK-ASSEMBLY.step
│   │   ├── ESP-STICK-ENCLOSURE-BOTTOM.step
│   │   └── ESP-STICK-ENCLOSURE-TOP.step
│   └── stl/
│       ├── ESP-STICK-ENCLOSURE-BOTTOM.stl
│       └── ESP-STICK-ENCLOSURE-TOP.stl
└── README.md
```

## Hardware

Mechanical source files are stored in `hardware/step/`, and printable STL
exports are stored in `hardware/stl/`.

- `ESP-STICK-ASSEMBLY.step` is the full assembly.
- `ESP-STICK-ENCLOSURE-TOP.step` and `ESP-STICK-ENCLOSURE-BOTTOM.step` are the
  enclosure shells.
- `ESP-STICK-ENCLOSURE-TOP.stl` and `ESP-STICK-ENCLOSURE-BOTTOM.stl` are the
  current printable exports.

Export to other printer-ready formats from the STEP models as needed. Keep those
exports under a dedicated hardware subfolder such as `hardware/stl/` or
`hardware/3mf/`.

Current STL exports are tracked, but slicer settings and orientation should be
reviewed before printing.

## Printing Recommendations

For the cleanest appearance, resin printing is the preferred process for this
enclosure. SLA/MSLA resin prints can produce sharper edges, smoother surfaces,
and less visible layer texture than FDM, which should suit the small screen
opening and compact handheld form factor well.

Use a tough, ABS-like, or engineering resin rather than a standard brittle resin
if the enclosure will be handled often, screwed together repeatedly, or carried
loose in a bag. FDM in PETG or ABS is still a good option for rough prototypes,
heat exposure, or parts where impact resistance matters more than surface finish.

Resin prints should be washed and post-cured according to the resin
manufacturer's guidance. Avoid over-curing, since some resins can become more
brittle with excessive UV exposure.

## Firmware

Firmware lives in `firmware/`.
The current sketch is:

```text
firmware/SerialSIM/SerialSIM.ino
```

The SerialSIM notes describe the target device, current scope, and intended
future behavior. See `firmware/SerialSIM/DeviceDetails.md`.

## Contributions

Contributions, improvements, and remixes are welcome.
