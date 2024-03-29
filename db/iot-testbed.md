# IoT Testbed

**Tags:** iot, testbed, instrumentation, embedded

## Introduction

While having access to a physical IoT device in invaluable while developing, sometimes (e.g., under COVID-19) that is not possible. Also, during certain periods of development you might need to experiment with a larger number of devices. For these purposes you can construct testbeds; installations of devices which you can remotely program, probe and observe.

## Problem

How can one enable a number of users to upload code to and operate (provide input to/receive output from) IoT devices deployed under different circumstances?

- How should users be represented?
- How should users receive time on the instrumented devices?
- How can we provide artificial inputs (scenarios) to the devices (e.g., make sure that a pin goes high or that a "temperature" sensor provides some particular value)?
- How can we read the outputs of the device (LEDs and pins)?
- How can we provide an uplink?
- How can we provice a downlink?
- Which price-points are available to us, and how do they map to functionality?

## Approach

Potential devices:
- [PyCom FiPy](https://pycom.io/product/fipy/)
- [ESP32 - Azure IoT Kit](https://www.espressif.com/en/products/devkits/esp32-azure-kit/overview)
- [Pine64 PineNut](https://pine64.com/product/pinenut-model12s-wifi-ble5-stamp/?v=b440ee21efe2)
- Various Ardiuno platforms.

## Related Work

