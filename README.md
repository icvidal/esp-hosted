# ESP-Hosted

Fork of [Espressif's ESP-Hosted](https://github.com/espressif/esp-hosted)
This repository is made to reproduce an issue while using the WiFi network adapter on SPI with a touch element peripheral.

## Issue description

## Hardware

The original platform showing the issue is our custom device. For collaboration reasons, this repository aims to reproduce the issue in a widely available setup: Raspberry Pi 4 Model B + ESP32S3 DevKit C

## Connections

| Signal | Raspberry Pi | ESP32S3 (SPI2) |
| --------------- | --------------- | --------------- |
| MISO | 19 | 37 |
| MOSI | 21 | 35 |
| SCK | 23 | 36 |
| CS | 24 | 39 |
| GND | 25 | GND |


## Software configuration

 * SPI = SPI2

 TODO: Configure SDK


## Setup
Setup IDF with [TODO]
```
cd espo_hosted_ng/esp_esp_driver
cmake -B build
```

To be continued

## How to reproduce

```
cd esp_hosted_ng/esp/esp_driver/network_adapter
. ../esp-idf/export.sh
idf.py set-target esp32s3
idf.py build
idf.py flash
```

Running `idf.py monitor` verify the ESP32 boots and by touching the GPIOs (TODO: Describe which ones) the message "Touch Slider Example: Slider Calculate, position: XX" is printed.

After flashing, connect the SPI bus as described in the table above and boot the Raspberry Pi, and ESP32.
Once the Raspberry Pi boots, load esp32_hosted_ng

