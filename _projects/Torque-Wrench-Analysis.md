---
layout: project
title: Cube Craze Robot
description: Autonomous cube-gathering robot designed for MAE 3780 Mechatronics competition.
technologies: [Arduino, C, Fusion, RPL]
---
This project was the final design assignment for MAE 3780 Mechatronics. The goal was to design and build an autonomous robot to compete in the "Cube Craze" competition, gathering as many cubes as possible within one minute on a two-color field.

---
###### Overview
We built a robot on the stock kit chassis with two continuous rotation servos, each driven by an L9110H H-bridge. Two 3D-printed extensions on either side widened the robot's perimeter to sweep cubes inward. All code was written in C using AVR registers on an Arduino UNO r3.

###### Sensors
- TCS3200 color sensor on the underside of the chassis for zone detection
- Two QTI reflectance sensors at the front edges for black border detection

###### Strategy
The basic idea was to sweep back and forth across the field and collect cubes as we went. The robot sampled the color sensor at the start of each match to establish a baseline, then drove forward until it detected a zone crossing. At each crossing it nudged forward, turned left or right (alternating), moved over slightly, updated its baseline, and repeated.


###### Design Process
We originally planned servo-actuated arms that could open to gather cubes and close to hold them. Late in the build period we found the open arms exceeded the 12-inch diameter cylinder constraint, so we switched to fixed 3D-printed extensions. The servo control code is still visible in commented-out sections of the final submission.


###### Competition Results
- Won our round robin group and advanced to single elimination
- An unintended advantage: the rigidity of the extensions let us knock opponents off the board, causing them to drop gathered cubes
- Lost in the bracket to a large block-style robot whose build let it passively hold cubes


###### Summary
- Autonomous navigation using color and QTI sensor feedback
- 3D-printed custom extensions designed and fabricated at the RPL
- All code in C using AVR registers — no Arduino commands
- Advanced out of round robin in a field of ~62 teams
