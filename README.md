# Dht11_Firestore
# DHT11 Sensor with ESP8266 and Google Firestore

This project demonstrates how to use the DHT11 temperature and humidity sensor with the ESP8266 microcontroller to read environmental data and store it in Google Firestore, a NoSQL database. The setup is ideal for IoT applications, where real-time environmental data is essential.

---

## Table of Contents
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Setup Instructions](#setup-instructions)
- [Project Overview](#project-overview)
- [Code Explanation](#code-explanation)
- [How to Use](#how-to-use)
- [Future Improvements](#future-improvements)

---

## Features
- Reads temperature and humidity data using the DHT11 sensor.
- Connects to a Wi-Fi network using the ESP8266.
- Sends real-time sensor readings to Google Firestore.

---

## Hardware Requirements
- ESP8266 NodeMCU
- DHT11 Temperature and Humidity Sensor
- Jumper Wires
- Breadboard
- Micro-USB Cable

---

## Software Requirements
- Arduino IDE
- ESP8266 Board Manager (installed in Arduino IDE)
- Libraries:
  - `DHT` by Adafruit
  - `Firebase ESP8266` by Mobizt
  - `ArduinoJson`

---

## Setup Instructions

### Step 1: Hardware Setup
1. Connect the **DHT11** sensor to the ESP8266:
   - VCC to 3.3V
   - GND to GND
   - Data pin to GPIO2 (D4 on NodeMCU)
2. Ensure all connections are secure.

### Step 2: Configure Firestore
1. Set up a Google Cloud Platform (GCP) project.
2. Enable Firestore in Native Mode.
3. Generate a service account key (JSON file) and download it.
4. Note your Firestore database URL.

### Step 3: Code Preparation
1. Install required libraries in Arduino IDE.
2. Replace the placeholders in the code:
   - Wi-Fi credentials: `SSID` and `Password`
   - Firestore details: database URL and service account credentials.

### Step 4: Upload Code
1. Connect the ESP8266 to your computer via USB.
2. Open the code in Arduino IDE.
3. Select the correct board and port.
4. Upload the code to the ESP8266.

---

## Project Overview
The ESP8266 reads data from the DHT11 sensor and connects to a Wi-Fi network. It then sends the temperature and humidity readings to a Firestore database at regular intervals, providing a simple yet effective way to store IoT data in the cloud.

---

## Code Explanation
- **Wi-Fi Connection**: The ESP8266 connects to the Wi-Fi network using SSID and password.
- **Sensor Reading**: The `DHT` library is used to fetch temperature and humidity values from the DHT11 sensor.
- **Firestore Upload**: The Firebase ESP8266 library is utilized to authenticate and send data to Firestore in JSON format.

---

## How to Use
1. Power the ESP8266.
2. Open the Firestore database to monitor incoming data.
3. View real-time temperature and humidity readings.

---

## Future Improvements
- Add support for additional sensors.
- Implement a web dashboard for live data visualization.
- Optimize power consumption for battery-operated devices.

