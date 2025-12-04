🌱🤖 HARI – An Intelligent Agricultural Robot

Precision Farming | Edge AI | Autonomous Robotics | Rocker-Bogie Rover

📌 Overview

HARI is an AI-powered agricultural robot designed to make farming more efficient, intelligent, and sustainable. Built by a three–member multidisciplinary team, the project integrates embedded systems, robotics, mechanical engineering, and machine learning into a rugged ground robot capable of navigating uneven terrains and providing real-time agronomic insights.

This repository contains the core code modules used in the HARI robot—robot arm control, real-time sensor monitoring, and edge-based plant disease detection workflows.

> 🚀 HARI reached the final round of the Accenture Innovation Challenge 2024 (Sandbox Round)
Due to academic commitments, the team could not attend the finale in Chennai.


👥 Team Hari

Member	Contribution

Hemant Kumar Mahto	Hardware architecture, chassis design, mechanical integration, system assembly
Sanchay Kumar	Embedded software development, AI/ML integration, robot arm programming, systems software
Mohit Pal	Power systems, battery module design, field endurance engineering

🌟 Features at a Glance

AI-driven plant disease detection using a custom CNN deployed via Edge Impulse

ESP32-CAM for real-time leaf analysis on the edge (no cloud required)

Rocker-bogie suspension inspired by NASA’s Mars Rovers

Modular sensor suite for soil & environmental monitoring

Web-based dashboard for live telemetry and robot-arm control

Record & playback system for automated arm movements

Future-ready architecture designed for cloud analytics & autonomous navigation


🧠 AI & Embedded Intelligence

HARI uses a Convolutional Neural Network (CNN) deployed on the ESP32-CAM to classify plant diseases directly on-device.

Tools & Platforms:

Edge Impulse → Model training, optimization, and quantization

ESP32-CAM → On-edge inference & imaging

ESP32 DevKit → Main controller + local HTTP server + data aggregator


Planned Cloud Integration:

Crop health dashboards

Soil & atmospheric analysis reports

Historical farm analytics



---

🚜 Mechanical System – Rocker-Bogie Suspension

To ensure stable mobility across farms, mud, pits, and uneven terrains, HARI uses a six-wheel rocker-bogie system, the same mechanism used in NASA’s Curiosity and Perseverance rovers.

Benefits:

✓ Maximum wheel contact

✓ No active suspension required

✓ Excellent obstacle handling

✓ High stability on rough terrain



---

🔧 Sensors & Data Acquisition

HARI integrates multiple low-cost sensors for real-time agricultural analytics.

Sensor	Purpose

DHT11	Temperature + Humidity
Rain Sensor	Precipitation detection
BMP180	Atmospheric pressure + temperature
Soil Moisture Sensors (x2)	Irrigation analysis
(Planned) Soil Nitrogen Sensor	Nutrient profiling
(Planned) Micro-agri Drone	Aerial mapping



---

📡 System Architecture

+---------------------------+
         |        ESP32 DevKit       |
         |  - Main Controller        |
         |  - WiFi Web Server        |
         |  - Sensor Fusion          |
         +------------+--------------+
                      |
        +-------------+-----------------------+
        |                                     |
+---------------+                     +------------------+
| ESP32-CAM     |                     | Sensor Module    |
| - AI Model    |                     | - BMP180         |
| - Disease CLS |                     | - Soil Sensors   |
+---------------+                     | - Rain & DHT11   |
                                      +------------------+

                     +------------------+
                     | Robot Arm Module |
                     | - Servo Control  |
                     | - Record/Replay  |
                     +------------------+


---

📂 Repository Structure

Hari-Robot/
│
├── /robot-arm-control/        # ESP32 DevKit robotic arm server + UI
│   └── hari_arm_control.ino
│
├── /sensor-module/            # Soil + BMP180 + moisture web server
│   └── sensors.ino
│
├── /docs/
│   ├── architecture-diagram.png
│   ├── suspension-mechanism.png
│   └── team-photo.jpg
│
└── README.md                  # You are here


---

🤖 Robot Arm Control Module

This module includes:

4-axis robotic arm (Base, Shoulder, Elbow, Gripper)

Servo control via ESP32 DevKit

Web-based slider interface (HTML + WebSockets)

Record & Playback automation system


Code File:

📁 /robot-arm-control/hari_arm_control.ino
(Your provided code is already integrated here.)


---

🌦 Sensor Monitoring Module

This module hosts a live dashboard displaying:

Soil moisture (% + Dry/Medium/Wet)

Atmospheric temperature

Barometric pressure

Controls to fetch sensor data every second


Code File:

📁 /sensor-module/sensors.ino
(Your provided code is already integrated here.)


---

🛠 Getting Started

✔ Requirements

ESP32 DevKit

ESP32-CAM

Servo motors (x4)

BMP180 sensor

Soil moisture sensors (x2)

Rain sensor

DHT11

Rocker-bogie chassis

12V Li-ion battery pack



---

🔌 Setup Instructions

1. Clone the repository



git clone https://github.com/yourusername/Hari-Robot.git

2. Install Required Libraries



ESP32Servo

AsyncTCP

ESPAsyncWebServer

SFE_BMP180

WiFi / WebServer


3. Upload hari_arm_control.ino



Controls robot arm

Opens WebSocket UI


4. Upload sensors.ino



Sets up a sensor dashboard

Displays real-time telemetry


5. Connect via Wi-Fi



Check serial monitor for IP address

Open browser → http://<ESP32-IP>/


---

🧭 Roadmap

[ ] Full autonomous navigation

[ ] Inter-row path planning

[ ] Cloud-backed agronomic dashboard

[ ] Integration with a drone for aerial imaging

[ ] Solar-powered endurance module

[ ] LORA-based long-range communication



---

🏆 Achievement

HARI qualified for the Accenture Innovation Challenge 2024 (Sandbox Round)—a testament to the team’s dedication and technical execution.


---

🤝 Contributing

Contributions, suggestions, and collaborations are welcome.
Feel free to open an issue or submit a pull request.


Would you like that?
