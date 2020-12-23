# Project Title

**Tags:** occupancy, iot, embedded, computer vision, privacy

## Introduction

Occupancy counters are being used for many purposes:
- Determining queue lengths at the airport
- Security
- Creating models of how occupants use a space (e.g., a building)

Today, occupancy counters are typically based around relatively expensive stereo cameras. That limits the applicability. Most, if not all, are also capable of streaming a video feed to a user of the camera. This has privacy implications.

Perhaps a different way is possible?

## Problem

How far (in terms of counting accuracy and privacy preservation) can we get by using a dirt-cheap IoT device with a single low-resolution camera?

## Approach

Use ESP32-Cam modules:
- They are cheap: [Here](https://www.amazon.de/Aideepen-Entwicklungsplatine-Bluetooth-Modul-Kamera-Modul-AP-Arbeitsmodus/dp/B08G1FR1VF/ref=sr_1_9?dchild=1&keywords=esp32-cam&qid=1608718478&sr=8-9) is 3 modules for 22€
- They have a dual-code 32-bit processor running 240MHz.
- They have 520kB SRAM and 4M PSRAM.
- They have communication: WIFI and BLE.
- They have a 2Mpixels camera.
- They have a MicroSD card reader.
- **Note:** Separate programmer needed.

In order to preserve privacy an image should never leave the device (except for when debugging).

Ideally, the relevant counting lines will be automatically determined based on actual movement patterns. However, this might prove too complicated or a hard to reason about from a consuming applications point of view.

## Related Work

- [ESP32-CAM Video Streaming and Face Recognition with Arduino IDE](https://randomnerdtutorials.com/esp32-cam-video-streaming-face-recognition-arduino-ide/)
- Commercial competition: [Xovis](https://www.xovis.com/en/products/)

