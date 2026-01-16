---
title: UBC Supermileage
date: 2025-10-17 00:00:00 +0800
categories: [software, hardware]
tags: [C++, KiCad, I2C, CAN, Microcontroller] 
pin: true
image:
  path: /assets/images/telemetry.jpg
  alt: Telemetry PCB and Housing
  class: shadow
---

As part of the UBC Supermileage car team, I helped design and program a telemetry system that allows the team to gain access to sensor data useful for improving the overall design of our cars. Our team annually participates in the Shell Ecomarathon (SEMA) in three different vehicle categories (Gas prototype, Urban EV, Hydrogen Fuel Cell), where we compete against other universities across the world to see who has the most efficient vehicle. Our telemetry system collects important sensor data such as speed, rpm, GPS location data, temperature, and acceleration through various sensors onboard the PCB as well as other electronics connected to the CAN bus. The PCB is centred around a Particle Boron LTE module, which contains a Nordic Semiconductor nRF52840 microcontroller. The peripheral features on the PCB include a CAN transciever, accelerometer, and numerous ports that connect to the ECU, Driver display, and GPS. The same telemetry board can be used for all three vehicle types, but the peripheral connections and firmware differ depending on the car (ex. engine ECU for gas, electric motor driver for EV). Our data is transmitted in a JSON format from the Boron LTE module to Google Cloud, and from Google Cloud to Grafana Dashboards, where we visualize and monitor the data in real time. 

What I am currently working on: 
- Extended Kalman Filter implementation using the BNO055 9-dof IMU and GPS module
- Designing a magnetic encoder based steering angle measurement setup
- Debugging hardware/software issues

Links:

Check out our firmware repository: [Firmware](https://github.com/supermileage/telemetry-firmware)

Check out our team website: [Team Website](https://www.supermileage.ca/)

# No Polygons

# Top Signal
![Top Signal](assets/images/Telemetry_Upper_Signal.png){: .w-75 .mx-auto .d-block }

# Ground
![Ground](/assets/images/Telemetry_GND.png){: .w-75 .mx-auto .d-block }

# Power
![Power](assets/images/Telemetry_Power.png){: .w-75 .mx-auto .d-block }

# Bottom Signal
![Bottom Signal](/assets/images/Telemetry_Lower_Signal.png){: .w-75 .mx-auto .d-block }

