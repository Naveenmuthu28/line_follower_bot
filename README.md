# Line Follower Robot Using Arduino Nano with PID Control

This project showcases a compact and efficient line follower robot designed to follow a black line on a white surface using PID (Proportional–Integral–Derivative) control for improved accuracy and stability.

The robot is built with affordable components, a custom 3D-printed chassis, and uses a PID algorithm to ensure smooth turns and accurate tracking even at higher speeds or on complex paths.

---

## Key Components

- Arduino Nano — Acts as the brain, reading sensors and controlling motors
- IR Sensor Array — Detects line position and sends analog/digital input for PID processing
- L298N Motor Driver — Connects Arduino with BO motors and handles direction/speed control
- BO Motors + Wheels — Provide movement based on PID speed adjustments
- 3.7V Li-ion Battery — Lightweight power source for portability
- Custom 3D-Printed Chassis — Tailored frame for optimal balance and component placement

---

## How It Works

1. The IR sensors continuously monitor the surface below.
2. The Arduino reads sensor values and calculates positional error (how far off the center line the robot is).
3. A PID control algorithm processes this error:
   - Proportional (P) reacts to the error amount
   - Integral (I) handles accumulated past errors
   - Derivative (D) predicts future errors
4. Based on the PID output, the Arduino adjusts motor speeds.
5. This keeps the robot on track and prevents excessive zig-zagging or overcorrection, especially on curves.

---

## Features

- Smooth line following on both straight and curved paths
- Intelligent error correction using PID control
- Real-time sensor feedback loop for adaptive steering
- Easy to tweak PID constants for different track types
- Suitable for robotics competitions or academic demonstrations

---

## Project Structure
```
line_follower/
│
├── line_follower.ino # Main Arduino code implementing PID control
├── README.md # Project documentation
└── LICENSE # MIT License
```
---

## Usage

1. Upload `line_follower.ino` to your Arduino Nano using the Arduino IDE.
2. Power the robot using the 3.7V Li-ion battery.
3. Place it on a black line track over a white background.
4. Manually tune the PID values in the code and upload, check if it follows the line. if it doesn't then repeat the process until it follows.
5. Watch it follow the path with PID-driven precision!

---

## License

This project is licensed under the MIT License.
