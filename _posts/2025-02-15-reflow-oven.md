---
title: N76E003 Reflow Oven Controller
date: 2025-02-15 00:00:00 +0800
categories: [hardware, software]
tags: [Assembly, I2C, Circuit, Python] 
pin: true
image:
  path: /assets/images/reflow_controller.jpg
  alt: N76E003 Reflow Oven Controller
  class: shadow
---

As part of coursework, we made a reflow oven controller that controls a 1500W toaster oven to follow a reflow temperature profile through a solid state relay.
- Firmware written in 8051 Assembly
- temperature data displayed using a Python program and serial port.
- I2C LCD panel and buttons for user interface
- Thermocouple with op amp used to make precise temperature measurements (+/-3C)

### Hardware Block Diagram
![Reflow Oven Hardware Diagram](/assets/images/reflow_hardware_block_diagram.png){: .w-75 .mx-auto .d-block }
_Figure: Block diagram of the reflow oven controller hardware._

### Software Block Diagram
![Reflow Controller Software Diagram](/assets/images/reflow_software_diagram.png){: .w-75 .shadow .rounded-10 }
_Figure: Block diagram of the reflow oven controller firmware._





  
