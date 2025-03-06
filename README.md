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

