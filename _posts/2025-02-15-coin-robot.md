---
title: Coin Picker Robot
date: 2025-04-26 00:00:00 +0800
categories: [hardware, software]
tags: [C, I2C, Microcontroller, Circuit] 
pin: true
image:
  path: /assets/images/IMG_5350 (1).jpg
  alt: Coin Picker Robot
  class: shadow
---

As part of coursework, we made a remote controlled coin picking robot from a EFM8 (robot) and STM32 (remote) capable of moving around and picking up coins. 

This robot includes:
- Firmware written in C
- Two JDY-40 wireless radios for wireless remote control. Each radio sends or recieves basic letters, which then represents a specific instruction dictated by the code.
- Two H-bridges, enabling directional control for two simple DC motors
- A colpitts oscillator for coin detection. The frequency emitted by the oscillator changes in response to magnetic interference, which allows the robot to detect metal objects such as coins.
- A double jointed servo arm and electromagnet for picking up coins and collecting them in an onboard container.
- An autonomous mode, which enables the robot to move around, detect and pick up coins without human input.
- A Manual mode, which allows a human to control the robot through a joystick and buttons. 



### Hardware Block Diagram
![Hardware Block Diagram](/assets/images/hardwareROBOT2.jpg){: .w-75 .mx-auto .d-block }
_Figure: Block diagram of the coin picking robot hardware._

### Software Block Diagram
![Software Block Diagram](/assets/images/softwareROBOT.jpg){: .w-75 .shadow .rounded-10 }
_Figure: Block diagram of the coin picking robot software._
