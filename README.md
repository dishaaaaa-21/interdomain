Autonomous Mecanum Robot -PROBLEM STATEMENT BY SRM TEAM ROBOCON [INTERDOMAIN]
📝 Problem Statement
Design and implement a control system for a four-wheeled Mecanum-wheeled robot that can perform an automated inventory scan in a warehouse aisle. The robot must autonomously navigate along a row of shelves, maintaining a consistent, safe distance to allow a camera or scanner to capture data from the products. The system should use proximity sensors to stay parallel to the shelves, handle corners and obstacles, and provide real-time position and distance data for analysis.

🛠️ Components Used
ESP32 Development Board (main controller)

4x Mecanum Wheels (omnidirectional movement)

4x DC Motors (wheel actuation)

2x L298N Motor Drivers (motor control)

4x Ultrasonic Sensors (HC-SR04) (distance measurement: front, back, left, right)

Power Supply (battery pack)

Chassis (robot frame)

(Optional for future): ESP32-CAM or mobile phone for inventory scanning

📍 Pinouts (ESP32 GPIO Assignments)
Function	Pin Number
FL1 (Front Left Dir1)	19
FL2 (Front Left Dir2)	18
FLP (Front Left PWM)	21
FR1 (Front Right Dir1)	5
FR2 (Front Right Dir2)	4
FRP (Front Right PWM)	2
RL1 (Rear Left Dir1)	16
RL2 (Rear Left Dir2)	27
RLP (Rear Left PWM)	14
RR1 (Rear Right Dir1)	25
RR2 (Rear Right Dir2)	33
RRP (Rear Right PWM)	32
FTrig (Front Trigger)	12
FEcho (Front Echo)	13
BTrig (Back Trigger)	15
BEcho (Back Echo)	36
RTrig (Right Trigger)	16
REcho (Right Echo)	17
LTrig (Left Trigger)	23
LEcho (Left Echo)	22



👥 Team Members
Disha – SPACED

Sana – SAMBED

Devdath – SIESED

Jatin – MCSOCD

🚀 Project Overview
This project demonstrates a fully autonomous robot capable of:

Navigating warehouse aisles using mecanum wheels for omnidirectional movement

Maintaining a precise, parallel path to shelves using real-time feedback from ultrasonic sensors

Avoiding obstacles and handling corners without human intervention

Providing live sensor data for inventory scanning and analysis

🏗️ How It Works
Initialization: All pins are set up for motor control and sensor input. PWM channels are configured for smooth speed control.

Sensing: Four ultrasonic sensors continuously measure distances to obstacles and shelves.

Decision Making: The ESP32 processes sensor data and decides movement (forward, strafe, or turn) to maintain a safe, parallel path.

Actuation: Motor drivers receive PWM and direction signals to move the robot as decided by the control logic.

Data Output: Sensor readings are sent to the serial monitor (and can be sent to a mobile device or cloud for further analysis).

🧩 Future Improvements
Integrate camera (ESP32-CAM or mobile) for automated inventory scanning

Implement PID control for even more precise distance and angle maintenance

Add feedback from wheel encoders for speed calibration

Develop a mobile/web dashboard for live monitoring and control 
