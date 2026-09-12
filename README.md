# Autonomous Object Sorting Robot

An autonomous **VEX IQ robot programmed in C++** that collects and sorts objects into designated locations. The system combines multiple sensors with closed-loop motor control for autonomous navigation and object handling.

## Overview

The robot completes an autonomous sorting cycle:

1. User selects an object category using a **touch sensor**.
2. The robot drives forward and detects the corresponding coloured stripe using an **optical sensor**.
3. An **inertial sensor** provides heading feedback for a controlled 90° turn.
4. A **distance sensor** detects the sorting box and controls the final approach.
5. A motorized claw and lift release the object.
6. **Motor encoders** measure travelled distance so the robot can return to its starting position.
## Control & Navigation

#### Closed-Loop Control

Implemented a **PID controller** for accurate 90° turns using inertial sensor feedback. A separate proportional correction continuously adjusts motor speeds during straight-line motion to compensate for heading deviations.

#### Encoder-Based Navigation

Motor encoders track the robot's displacement during each navigation segment. The recorded distance is then used to retrace the path and return to the starting position without requiring a predefined map.

#### Multi-Sensor Integration

| Sensor | Purpose |
|---|---|
| Inertial Sensor | Heading measurement and turning |
| Optical Sensor | Coloured stripe detection |
| Distance Sensor | Sorting box detection |
| Touch LED | Category selection |
| Motor Encoders | Position and distance tracking |


<br></br>
## Project

**MTE 100 & MTE 121 — University of Waterloo, Fall 2025**  
Team project by **Anshia Yaqoob, Jaime McGale, Martin Montgomery, and Ahmad Ashmawi**.

**[Watch the demo](https://youtu.be/CaOrTIv2SYU)**.
**[View the project report](https://drive.google.com/file/d/1MJbCLCNo2NveWUUdiiL4WoyymR6oygXf/view?usp=sharing)**.
