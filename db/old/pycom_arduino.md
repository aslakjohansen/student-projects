# Arduino on PyCom

**Tags:** iot, arduino, pycom, porting, evaluation

## Introduction

We have been using PyCom boards (LoPy and FiPy) for the “Software Engineering of Internet of Things” course. These come with a wide range of communication options and a fairly powerful microcontroller that is meant to be programmed using embedded python. Each of these boards are attached to a PyCom PySense board with a selection of sensors.

The toolchain provided by pycom has proven to be problematic: There has been problems uploading code to the devices and python -- being a garbage-collected language -- is a bad choice for doing timing-dependent low-level operations.

However, there is a [project](https://forum.pycom.io/topic/3134/using-pycom-boards-with-arduino-ide) for programming these boards using the Arduino IDE (and more importantly, the C-based stack).

## Problem

In this project we would like to evaluate what it would take to use our PyCom boards using the Arduino pipeline, and how well the resulting setup would work.

## Approach

1. Follow the instructions on the link above
2. Write a suite of test programs to evaluate various features (sensors, actuators and other peripherals)
3. Identify missing code (e.g., driver for the ambient light sensor)
4. Implement a sensible subset of the missing code

## Related Work

