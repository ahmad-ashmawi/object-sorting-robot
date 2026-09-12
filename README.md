# Autonomous Object Sorting Robot

An autonomous **VEX IQ robot programmed in C++** that collects and sorts objects into designated locations. The system combines multiple sensors with closed-loop motor control for autonomous navigation and object handling.
<br></br>
## Overview

The robot completes an autonomous sorting cycle:
1. The user selects an object category using the touch sensor.
2. The robot drives forward and uses an optical sensor to find the corresponding coloured stripe.
3. It performs a PID-controlled 90° turn using inertial sensor feedback.
4. A distance sensor guides the robot as it moves toward the sorting box.
5. The claw and lift mechanisms release the object into its designated place.
6. Motor encoders track the travelled distance so the robot can return to its starting position.

   

## Control & Navigation

Implemented a **PID controller** for accurate 90° turns using inertial sensor feedback. A separate proportional correction continuously adjusts motor speeds during straight-line motion to compensate for heading deviations. 

Motor encoders track the robot's displacement during each navigation segment. The recorded distance is then used to retrace the path and return to the starting position without requiring a predefined map.

#### Sensors Used:

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
