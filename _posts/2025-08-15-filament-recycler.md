---
title: Coin Picker Robot
date: 2025-04-26 00:00:00 +0800
categories: [hardware, software]
tags: [C, I2C, SPI, Microcontroller, Altium, Circuit] 
pin: true
image:
  path: /assets/images/Recycler_PCB
  alt: Coin Picker Robot
  class: shadow
---

### PCB Top View
![PCB](/assets/images/Recycler_PCB){: .w-75 .mx-auto .d-block }

As part of UBC Rapid, I designed a Filament Recycler that controls the following peripherals:
- ILI9431 SPI Display, Buttons and Rotary Encoder
- Two TMC2209 Stepper Drivers
- Four MOSFET Based PWM 5V Fan Controllers
- EEPROM
- One I2C Sensor, for hall effect sensor
- One SPI Sensor, because there were extra pins
- Logic level converter for controlling an external motor driver, for the large shredder motor

In order to power all of circuitry on this PCB, I implemented a 24V to 5V Buck Converter and a 5V to 3.3V LDO, which can provide power at 24V, 5V, and 3.3V. This PCB can also be programmed and powered
through a USB-C port or serial wire debug pins.
  


### Microcontroller and Boot Switch Schematic
![STM32](/assets/images/Recycler_STM32){: .w-75 .mx-auto .d-block }

- I used an STM32F4 as the microcontroller for this project

  

### Stepper Driver
![Software Block Diagram](/assets/images/stepper_driver){: .w-75 .shadow .rounded-10 }

- Two TMC2209 steppermotor drivers powered by 24V input and communicates via UART to the STM32
