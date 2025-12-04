An agriculture Robot That's an impressive project! Hari is a fantastic example of applying space-exploration engineering (Rocker-Bogie) and cutting-edge AI (Edge Impulse, offline CNN) to a down-to-earth problem like precision agriculture.

Here is a structured, comprehensive README file for Project "Hari," designed to be clear, professional, and suitable for sharing in academic, professional, or open-source contexts.

🤖 Project Hari: An Autonomous Agricultural Robotics Platform 🌱 Hari is an intelligent, ruggedized agricultural robot designed to bring precision farming and AI-enabled diagnostics directly to the field. Leveraging a robust Rocker-Bogie suspension system and edge-based machine learning, Hari provides real-time, offline plant health monitoring and environmental data collection to assist farmers in optimizing yield and resource management.

🌟 Features & Capabilities Offline Plant Disease Detection: Utilizes a custom CNN model trained via Edge Impulse and deployed on an ESP32-CAM to perform real-time, field-side classification of plant diseases without cloud dependency.

Rugged Mobility: Employs a Rocker-Bogie Suspension system (the same principle used by NASA's Mars rovers) for exceptional stability, high traction, and smooth obstacle traversal on uneven agricultural terrain. Real-Time Telemetry: An ESP32 DevKit hosts a local HTTP server to display sensor data and system status on a dedicated web dashboard, providing immediate insights to the user.

Multi-Sensor Data Acquisition: Collects critical environmental and soil data through an integrated sensor suite. Hardware & Software Architecture Component Function Central Controller ESP32 DevKit Vision/AI Processor ESP32-CAM Motor & Drive System 6-Wheel Drive with Rocker-Bogie Linkage Environmental Sensor DHT11 (Temperature & Humidity) Atmospheric Sensor BMP180 (Atmospheric Pressure & Temperature) Soil Sensor Soil Moisture Sensor Precipitation Sensor Rain Sensor Power System Dedicated Power and Battery Management System Software & Technology Stack AI/ML: Custom CNN Model for plant disease detection.

Edge ML Platform: Edge Impulse for model training and deployment.

Core Logic: Embedded C/C++ (on ESP32).

Communication: Local HTTP Server for telemetry dashboard. Engineering Highlights Rocker-Bogie Suspension The Rocker-Bogie design was chosen specifically for its passive stability. It articulates without the need for springs or complex dampers, allowing all six wheels to remain in contact with the ground even over large obstacles, which is crucial for maintaining stability for the onboard sensors and AI camera.

AI at the Edge The decision to run the disease detection model completely offline was a critical design choice, ensuring reliability in remote farming areas with limited to no internet connectivity.

👥 Team Hari Hari was developed by a small, passionate, and multidisciplinary team:

Hemant kumar Mahto: Hardware Architecture, Mechanical Integration, System Assembly.

Sanchay Kumar: Embedded Software Development, AI Model Integration, Software Architecture.

Mohit pal: Power and Battery Management for Long-Duration Field Operation.

🛣️ Future Development & Roadmap Due to initial constraints (budget, academic schedule), several ambitious features were deferred. These represent the key areas for future growth:

Soil Nitrogen Sensor Integration: Incorporating a dedicated sensor for soil nitrogen levels to provide deeper fertilization recommendations.

Cloud-Based Analytics: Integrating a cloud platform for long-term data storage, deeper agronomic insights, and advanced environmental analytics.

Aerial Data Complement: Developing and integrating a mini agricultural drone for aerial crop mapping to complement Hari's ground-level data.

Autonomous Navigation: Implementing full field path planning and obstacle avoidance for true autonomous operation.

🏆 Project Recognition Accenture Innovation Challenge 2024: Qualified for the Sandbox Round.
