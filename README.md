# WRO26_Future-Engineers_RoboX
WRO 2026 Future Engineers Category _ Autonomous Vehicle Documentation &amp; Source Code for RoboX Team
1. Introduction and Team Overview:
   - Team Name: RoboX
   - Team Members: Hajer Al Salmani, Fatima Al Mamari
   - Institution: Modern College of Business and Scince (MCBS)
   - Category: Future Engineers (WRO 2026)
   - The project focuses on engineering a self-contained, autonomousrobotic vehicle capable of navigating a dynamic track, avoiding unexpected obstacles (red and green traffic pillars), and executing a percise parallel parking maneuver inside a designated zone.
2. Mobilitiy & Mechanical Design:
Our physical platform is currently being assembled utilizing a rigid, lightweight synthetic micro:bit/elecfreaks optimized for tight cornering dynamics inside the 3-meter by 3-meter competition track. 

Steering & Kinematics
Instead of a differential drive setup, our vehicle utilizes an authentic car-like Ackermann steering geometry. This design implements a front steering axle driven by a dedicated, high-torque  motor. Ackermann steering minimizes tire scrubbing and provides predictable turning radii, which is essential for calculating precision maneuvers during the obstacle challenge. 

Drivetrain & Performance Targets
Actuation: Dual rear-wheel DC gear motors configured for maximum low-end torque.
Target Wheel Diameter: Approximately [56mm rubber] tires to maximize traction and achieve consistent encoder feedback.
Velocity Goal: The gear ratios are selected to maintain a stable, controllable cruising velocity of[ 0.3 to 0.5 ]meters per second, balancing processing latency with lap-time efficiency.

Ongoing Mechanical Iteration (Work in Progress)
During our current physical assembly phase, a major structural challenge involves optimizing the steering clearance. Initial mockups revealed that the inner edges of the front tires experienced frictional contact with the chassis frame(beams)at maximum steering angles. We are currently iterating the front axle spacers and trimming the lower chassis beams to expand our turning clearance without widening the overall vehicle track width beyond the competition limits.


3. Power & Sensor Architecture
The electronic subsystem is built around an ESP32 microcontroller, chosen specifically for its dual-core processing capabilities, clock speeds up to 240MHz, and built-in hardware timers which are necessary for handling simultaneous sensor interrupts.

4. Software Logic & System Architecture
The software environment is developed using Python/Arduino, translating complex algorithmic operations into clean, high-level structural scripts.

5. Design Choices & Trade-offs (Systems Thinking)
Choosing the ESP32 over a standard Arduino Uno or a heavy Single Board Computer (like a Raspberry Pi) represents our primary system trade-off. While an Arduino is simple, it lacks the memory required to process rapid Python logic loops. Conversely, a Raspberry Pi introduces massive power consumption and long boot times. The ESP32 gives us the perfect middle ground: fast execution, hardware interrupts, and low energy draw.

6. Project Reproducibility & Setup Guide

Hardware Dependencies
- Microcontroller: ESP32 Development Board
- breadbored
- ESP32 CAM
- servo motor driver
- L298N motor
- Blocks
- batteries
- Programming Language: MicroPython / Python syntax
