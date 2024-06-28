---
layout: default
title: ESP32-S3 Pins
parent: Hardware
nav_order: 2
---

# ESP32-S3 Pin Definitions

<div class="code-example" markdown="1">

| GPIO# | Funtion                            | Mode                 |
| :---: | :--------------------------------- | :--------------------|
| 0     | Boot0                              |                      |
| 1     | Stepper Driver 2 RST               | Output               |
| 2     | Stepper Driver 2 STEP              | Output               |
| 3     | LCD Backlight                      | Output               |
| 4     | Rotary Encoder SW                  | Input (Active Low)   |
| 5     | SPI MISO / I2C SCL                 |
| 6     | SPI MOSI / I2C SDA                 |
| 7     | SPI CLK                            |
| 8     | Rotary Encoder A                   | Input                |
| 9     | ADC Current                        | Analog Input         |
| 10    | ADC VIN                            | Analog Input         |
| 11    | Buzzer                             | Output (Active High) |
| 12    | Current Fault                      | Input (Active Low)   |
| 13    | ZVS High Current On/Off            | Output (Pulsed 100Hz+) |
| 14    | Unused                             |                |
| 15    | SPI CS                             | Output               |
| 16    | LCD A0                             | Output               |
| 17    | LCD RST                            | Output               |
| 18    | Rotary Encoder B                   | Input                |
| 19    | USB D-                             | USB                  |
| 20    | USB D+                             | USB                  |
| 21    | Cooling Pump Tach                  | Input                |
| 35    | Drop Solenoid                      | Output (Active High) |
| 36    | Case Detector IR Out               | Output (Active High) |
| 37    | Case Detector Input                | Input (Active Low)   |
| 38    | Stepper Driver 1 STEP              | Output               |
| 39    | Stepper Driver 1 RST               | Output               |
| 40    | DS18B20 One Wire                   | Input/Output         |
| 41    | Stepper Drivers FLT                | Input (Active Low)   |
| 42    | Stepper Drivers DIR                | Output               |
| 43    | Case Height Adjustment Home Switch | Input (Active Low)   |
| 44    | Start/Stop Button                  | Input (Active Low)   |
| 46    | ZVS Control (Low Current)          | Output (Active High) |
| 47    | Pump On/Off                        | Output (Active High) |
| 48    | Fans On/Off                        | Output (Active High) |

</div>