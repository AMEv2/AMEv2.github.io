---
layout: default
title: Hardware Description
parent: Hardware
nav_order: 1
---

# Harware
Hardware description of the AME board.

## 3D Model
A Step model of the AME Board is avaialble for [download](../../assets/step/AME_V2.0.0.step)

## Features
**ESP32-S3**

The ESP32-S3 is the **AME** boards main controller. This allows for Bluetooth control, Over-the-Air updates, Wi-fi connection and more.

**Built-in 60W 12V power supply**

The AME board has a built-in 60W 12V output power supply. Supported input voltage 12V - 60V.

**Built-in high current switch for the ZVS induction annealer board**
There is a on board low-side high current switch with a failsafe control circuit. To turn on the ZVS board, the fail-safe control circuit has to be pulsed at a rate of 100Hz or more. If the control output is held either high or low, the ZVS board is turned off.

**Built-in low voltage control of the ZVS induction annealer board**

Additional to the high current control, there is also an optional low-current control output. This is 4 inputs connected to ground through schottky diodes and a transistor. The four outputs gets connected to up to four gates of the FETs on the ZVS Annealer board. By turning the transistor on, the ZVS annealer will be turned off.

The concept is to turn on the annealer using the high current switch when starting an anneal session, then using the low voltage control to turn the ZVS annealer on to anneal a case and off between cases. And at the end of the session, turn off the low side high current control.

**Built-in Current Sensor**

On-Board ACS71240 current sensor. Max current 30A.

**Dual Stepper motor drivers**

The AME board has 2 stepper drivers. The FLT and DIR pins are shared by the two stepper drivers.
 - One for a case feeder: [3D Printed Case Feeder](https://www.thingiverse.com/thing:4902058/files "Thingiverse")
 - One for case height adjustment.

**DS18B20 Temperature sensor**

2x 3Pin JST-XH connectors for DS18B20 One Wire temperature sensors.

**Pump Control**

4-way standard PC fan connector for the Pump, with low side control and tach feedback. The speed control pin is NOT wired to the ESP32-S3.

**Dual Fan Controls**

2x 4-way standard PC fan connectors for 2 fans, with low side control. Tach feedback and speed control pins are NOT wired to the ESP32-S3.

**Drop Solenoid Control**

Low side control of drop solenoid for case dropper.

**Case Detector/Pickup**

Output and input for an optical case detector circuit. Custom PCB will be available for this as well.

**Support for SPI or I2C Displays**

SPI with LCD Reset as well as LCD A0 pins broken out to JST-XH connector for connecting to LCD display. The MISO and MOSI pins can be used as I2C for connecting to an I2C LCD as well. Default LCD is 128x64 SSD1306.

**Rotary Encoder Input**

Input for rotary encoder (A, B and SW)

**Dedicated Start/stop button**

Input for dedicated start stop button.

**Homing Switch**

Input for microswitch to use with case height adjustment module as home switch.

**Pluggable Connectors**

All Connectors are pluggable type connectors. 
 - JST-XH for most of them. 
 - XT-60 Female for the DC-input. 12V - 60V, max 30A
 - XT-60 Male for ZVS Induction board
 - Standard 4 pin Fan connectors