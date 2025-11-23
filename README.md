<div align="center">
  <img src="https://github.com/user-attachments/assets/33701f5e-6b2d-4f3c-b07d-f97840edfe5f" alt="IoT Smart Irrigation System Banner" width="100%">
</div>

## IoT Smart Irrigation System (LoRa/GSM & ESP32)

We have developed an automated irrigation solution designed for remote rural areas with limited internet infrastructure. The system features reliable telemetry transmission and autonomous control through the implementation of a hybrid communication architecture that combines LoRa radio technology and GSM modules, enabling real-time remote monitoring via a customized mobile app.

## Project Overview

This project addresses the challenge of connectivity in precision agriculture through the development of an **IoT Smart Irrigation System**. The hardware architecture is built around the **Heltec WiFi LoRa 32 (V3)** development board, integrating soil moisture sensors and actuators to perform autonomous irrigation based on environmental data, reducing water and labor waste.

To overcome the lack of stable internet in the field, the system uses a dual communication strategy. It encompasses Heltec's integrated **LoRa** radio for long-range, low-power local communication and **GSM/WiFi** modules to connect this data to the cloud (**Google Firebase**). This ensures that farmers can monitor their crops remotely via a mobile app, regardless of local connectivity conditions.

### Key Results

* **Hybrid Connectivity:** Successful implementation of communication protocols using LoRa for local range and GSM/WiFi for cloud synchronization.
* **Autonomous Control:** Development of firmware logic in C++ for self-regulating irrigation based on sensor thresholds.
* **Complete Integration:** Creation of a complete ecosystem connecting hardware, cloud database (Firebase), and an easy-to-use mobile app.
* **Field Validation:** Testing to verify communication range and system efficiency under real operating conditions.

## Technologies and Tools

Technologies Used:
* **Firmware:** C++.
* **Hardware:** Heltec WiFi LoRa 32 (V3), GSM Modules, Soil Sensors, Actuators.
* **Connectivity:** LoRaWAN, GSM/GPRS, WiFi, Google Firebase (Realtime Database).
* **Mobile App:** Android, User Authentication, Cloud Synchronization.
* **Tools:** Arduino IDE, EasyEDA.

## System Architecture (How it Works)

The system operates in a synchronized cycle to ensure crop health and data availability:

1. **Sensing:** Soil moisture sensors and battery voltage dividers continuously monitor field conditions.
2. **Processing:** The Heltec ESP32 processes the data and determines if irrigation is needed based on programmed thresholds.
3. **Actuation:** If soil moisture is low, the system automatically triggers the irrigation pumps.
4. **Communication:** Data is transmitted via LoRa (using the on-board radio) or directly via WiFi/GSM to the internet gateway.
5. **Cloud Sync:** The data is pushed to **Google Firebase**, updating the real-time database.
6. **Monitoring:** The **Mobile App** retrieves this data, allowing the user to view status and configure settings remotely.

## Implementation Details

### Firmware and Control
Developed in **C++**, optimizing the architecture for low-power operation.
* **Communication Logic:** Routines implemented to switch between WiFi, GSM, or LoRa based on availability.
* **Automation:** Logic for autonomous pump activation and safety shutdowns.

### Hardware Layer
* **Main Controller:** Use of **Heltec WiFi LoRa 32 (V3)**, which integrates the ESP32-S3 chip and SX1262 LoRa transceiver, reducing wiring and improving the format.
* **Sensors and Actuators:** Circuit design for accurate reading of resistive/capacitive soil sensors and relay control for pumps.

### IoT and Mobile Device Integration
A comprehensive mobile solution was developed to manage the hardware remotely, using **Firebase** as the backend.

**1. Mobile app features**
The Android app offers a complete user interface:
* **Authentication:** secure registration, login, and password recovery flow.
* **Dashboard:** real-time visualization of soil moisture levels (sensor readings).
* **System integrity:** monitoring of system battery levels.
* **Scheduling:** interface for recording and modifying irrigation pump activation schedules.

**2. Cloud data management**
* **Real-time database:** used to store sensor records, user settings, and system status updates, ensuring synchronization between field hardware and the user's smartphone.

## Academic context

* **Institution:** Instituto Federal de Educação, Ciência e Tecnologia de Alagoas (IFAL)
* **Research topic:** Development of an automatic irrigation system with monitoring via mobile application in regions with difficult Internet access using the Lora-Esp32 platform and the GSM kit.
* **Program:** PIBITI (Technological Research and Development)
* **Period:** September 2023 - August 2024
* **Advisor:** MSc José Irineu Ferreira Júnior 
