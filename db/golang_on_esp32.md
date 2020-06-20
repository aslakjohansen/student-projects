# Golang on ESP32

**Tags:** iot, embedded, esp32, golang, evaluation

## Introduction

At the Software Engineering of IoT course at SDU there has so far been a choice of two programming languages: Embeeded python and C. Embedded python is horrible in terms of concurrency and C does not have a garbage collector. This should make the choice of C an easy one, but most of our students rely heavily on the presence of a garbage collector.

Golang might prove a workable middle-ground with its strong concurrency support. The support for the ESP32 chip that we are currently using might only be preliminary at the moment. However, it would be interesting to see how well it works.

Alternatively, we could explore the possibility of having the course switch platform from ESP32 to one of:

- [HiFive1 Rev B](https://www.sifive.com/boards/hifive1-rev-b) or similar [RISC-V board](https://www.seeedstudio.com/catalogsearch/result/?q=risc-v)
- Something [else](https://tinygo.org/microcontrollers). Does this include a [Teensy](https://www.pjrc.com/store/)?

## Problem

Make a nontrivial demo program for an ESP32 (e.g., the [ESP32 Azure Kit](https://www.espressif.com/en/products/devkits/esp32-azure-kit/overview)). This should have multiple concurrent processes.

The task is to evaluate:
- What does it take to port an existing python driver to tinygo?
  - A process would have to be defined and lessons learned documented.
- How does the language perform?

## Approach

As for the language performance evaluation the onus is on how disruptive the garbage collections is when it kicks in.

## Related Work

- [Go Language](https://golang.org)
- [TinyGo](https://tinygo.org)
- [TinyGo and ESP32](https://tinygo.org/faq/what-about-esp8266-esp32/)
- [GoBot](https://gobot.io)

