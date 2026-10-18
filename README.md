# 🔌 Clairvo IoT - Hardware Node (ESP32)

![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Espressif](https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white)

This repository contains the C++ firmware and hardware configuration for the **Clairvo Smart Air Quality Monitoring System**. The physical node collects environmental data using various sensors and transmits it to a Firebase NoSQL database in real-time, while also automatically controlling an exhaust fan based on air quality thresholds.

## 🔗 Web Dashboard Repository
The full-stack Next.js web dashboard that displays this sensor data can be found here:
**[Clairvo Air Quality Monitor - Web Dashboard](https://github.com/dlynndaaa/clairvo-air-quality-monitor)**  
*(Live Demo: [clairvo-air-quality-monitor.vercel.app](https://clairvo-air-quality-monitor.vercel.app))*

## 📸 Hardware Setup & Schematic
<img width="459" height="258" alt="Sistem Pemantauan dan Pengendalian Kualitas Udara Bengkel Berbasis IoT (1)" src="https://github.com/user-attachments/assets/bc0e10cd-274f-4788-be55-f44d8e9b993d" />
<br>
Figure 1: IoT Node Schematic Wiring.
<br>

<img width="205" height="143" alt="Sistem Pemantauan dan Pengendalian Kualitas Udara Bengkel Berbasis IoT" src="https://github.com/user-attachments/assets/01a75201-af75-469a-a420-c4a25ec7f955" />
<br>
Figure 2: Physical Enclosure Setup with Exhaust Fan.

## ⚙️ Hardware Components
The smart monitor is built using the following physical components:
- **Microcontroller:** ESP32 (Wi-Fi enabled)
- **Gas Sensor:** MQ-135 (Detects harmful gases and overall air quality)
- **Particulate Sensor:** PMS6003 (Measures PM2.5 and PM10 particles)
- **Display:** LCD Module (For local data monitoring inside the enclosure)
- **Actuator:** 5V Relay Module 
- **Output:** Exhaust Fan (Triggered automatically to clear bad air)

## 💻 Firmware Features
- Reads real-time analog and digital data from the MQ-135 and PMS6003 sensors.
- Processes and calibrates sensor values.
- Connects to a local Wi-Fi network.
- Transmits data securely to the Firebase cloud database.
- Controls an external exhaust fan system via relays based on predefined air quality thresholds.

## 🛠️ How to Flash (Arduino IDE)

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/dlynndaaa/clairvo-esp32-node.git
2. Open the smart_air_quality.ino file using the Arduino IDE.
3. Ensure you have installed the ESP32 board manager and the necessary sensor libraries (e.g., for the PMS6003 sensor and LCD).
4. Update the Wi-Fi credentials (SSID and PASSWORD) and Firebase configuration keys in the code.
5. Connect your ESP32 board via USB, select the correct COM port, and click Upload.

