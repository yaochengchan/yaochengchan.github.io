---
title: "Prototype of a Robot Puppeteering System"
layout: single
permalink: /puppet/
author_profile: true
---

## Overview
For my dissertation research in Human-Robot Interaction, I developed a robotic puppeteering interface to investigate how robot Communicative Behaviors influence pedestrians' Perceived Social Intelligence during social navigation tasks, addressing the sociotechnical gap as autonomous robots deploy into public spaces. The prototype features a two-degree-of-freedom robot and a corresponding physical puppet, which are linked via Raspberry Pis to execute real-time motor mirroring. I used an iterative design process to build and refine this system. To create a reliable proof of concept, I designed a robotic head inspired by Wall-E. I evaluated the prototype through remote pilot studies, and the testing confirmed that the real-time physical mirroring allowed users to effectively review and redesign recognizable expressions. Participant (as random pedestrians) feedback indicated that the robot was cute, and that its movements and eye gaze made people feel acknowledged and encouraged further interaction.

## Iterative Design of the Puppeteering System

### Prototype Setup
<img src="/files/prototype_wood.gif" alt="Initial wooden plate prototype">

The iterative design of the puppeteering system began with a simplified proof of concept restricted to two degrees of freedom. To reduce the complexity of movement data analysis, the initial prototype utilized a blank wooden plate rather than a digital display. Pilot testing showed that users were able to generate their own interpretations of basic emotions using this minimal setup. Most participants also reported viewing the wooden plate as the robot's face prior to receiving instructions.

### User Interaction Testing
<img src="/files/prototype_autodesk.png" alt="User interacting with the puppet system">
CAD model of a custom robotic head assembly designed for social interaction research, featuring a dual-eye camera housing and a motorized pan-tilt base for expressive movement.

### Hardware Iteration
<img src="/files/prototype_head.gif" alt="3D printed robot head with binocular eyes"> 

Following these initial tests, the hardware was updated to a 3D-printed head with binocular eye structures inspired by Wall-E. This structural iteration provided a clear forward orientation to assist users in designing and reviewing the robot's directional gaze during interaction studies.

## Technical Setup
The technical architecture of the puppeteering system is built on a distributed hardware and software framework designed for low-latency movement mirroring. The hardware consists of two identical 2-DOF pan-and-tilt units. Each unit utilizes two Dynamixel AX-12W servo motors connected to Raspberry Pi microcomputers via U2D2 USB interfaces.

The software stack is implemented in Python and utilizes standard TCP sockets to facilitate real-time data transmission between the devices. On the puppet side, a sender script leverages the Dynamixel SDK to poll the physical positions of the manipulated motors. These coordinates, along with timestamps, are packaged into JSON-formatted strings for transmission. To optimize network traffic, the script includes a timeout function that pauses data transmission during periods of inactivity. On the robot side, a receiver script running on a Raspberry Pi connects to the sender, parses the incoming JSON stream, and immediately writes the coordinates as goal positions to the robot's motors. This configuration allows the robot to accurately duplicate the puppet's movements with minimal delay.
