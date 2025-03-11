# ESP-Hosted

Fork of [Espressif's ESP-Hosted](https://github.com/espressif/esp-hosted)
This repository is made to reproduce an issue while using the WiFi network adapter on SPI with a touch element peripheral.

## Issue description

## Hardware

The original platform showing the issue is our custom device. For collaboration reasons, this repository aims to reproduce the issue in a widely available setup: Raspberry Pi 4 Model B + ESP32S3 DevKit C



## Setup
Follow [setup.md](docs/setup.md)

Reproduce the issue:
Once the ESP32-S3 is flashed with the network_adapter firmware on `esp_hosted_ng/esp/esp_driver/network_adapter`, on the host (Raspberry Pi), go to the `host` directory and just run the `rpi_init.sh` script like this
``` bash
./rpi_init.sh spi resetpin=518
```
