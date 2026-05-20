# Firmware

Firmware for the ESP-STICK lives here. The current firmware target is
SerialSIM, an ESP32-S3 serial and TCP test device used with SerialHub.

## Contents

```text
firmware/
├── README.md
└── SerialSIM/
    ├── DeviceDetails.md
    └── SerialSIM.ino
```

## SerialSIM

`SerialSIM/SerialSIM.ino` is an Arduino sketch for the Waveshare
ESP32-S3-LCD-1.47 board. It currently provides:

- USB serial command and response testing.
- TCP command and response testing over Wi-Fi.
- Basic display status for serial, TCP, and activity indicators.
- RGB LED feedback for TCP connection state.

Device notes and project scope are in `SerialSIM/DeviceDetails.md`.

## Configuration

Edit these values near the top of `SerialSIM/SerialSIM.ino` before flashing:

```cpp
constexpr uint32_t SERIAL_BAUD = 9600;
constexpr char WIFI_STA_SSID[] = "WIFI_STA_SSID";
constexpr char WIFI_STA_PASSWORD[] = "WIFI_STA_PASSWORD";
constexpr uint16_t TCP_PORT = 5000;
```

## Build and Flash

Open `SerialSIM/SerialSIM.ino` in Arduino IDE or another Arduino-compatible
workflow.

Expected dependencies:

- ESP32 board support for Arduino.
- `Arduino_GFX_Library`.
- Waveshare ESP32-S3-LCD-1.47 board selected or equivalent ESP32-S3 settings.

After flashing, connect over USB serial at the configured baud rate. If Wi-Fi
credentials are set, the device also opens the configured TCP port for testing.
