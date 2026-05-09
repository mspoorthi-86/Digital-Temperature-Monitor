# Digital Temperature Monitoring & Visualization

## 🎯 Project Goal
[cite_start]The objective of this task is to design a real-time monitoring system that captures environmental temperature data and displays it on an external interface[cite: 3]. [cite_start]The system ensures high data integrity by using digital communication protocols and provides a local readout for immediate feedback[cite: 4].

## 🛠 Hardware Components
* [cite_start]**Microcontroller:** Arduino UNO R3 (ATMega328P)[cite: 6].
* [cite_start]**Temperature Sensor:** HW-506 (DS18B20 Digital Thermometer)[cite: 7].
* [cite_start]**Display:** 0.96" I2C OLED Display (SSD1306)[cite: 8].
* [cite_start]**Interface:** Breadboard and High-Quality Jumper Wires[cite: 9].

## 🔌 Circuit Connections
[cite_start]The following table outlines the hardware wiring[cite: 11]:

| Component | Pin Label | Arduino Pin | Function |
| :--- | :--- | :--- | :--- |
| **HW-506 Sensor** | S (Signal) | Digital Pin 2 | OneWire Data |
| | + (VCC) | 5V | Power |
| | - (GND) | GND | Ground |
| **OLED Display** | VCC | 5V | Power |
| | GND | GND | Ground |
| | SDA | Analog Pin A4 | I2C Serial Data |
| | SCL | Analog Pin A5 | I2C Serial Clock |

## 💻 Software Implementation
[cite_start]This project is built using the Arduino IDE with the following library dependencies[cite: 13]:
* [cite_start]**OneWire.h & DallasTemperature.h:** Handles the 1-Wire communication protocol for the digital sensor[cite: 14].
* [cite_start]**Adafruit_SSD1306.h & Adafruit_GFX.h:** Manages the pixel-based rendering on the OLED screen[cite: 15].

## 🔬 Circuit Analysis
* [cite_start]**I2C Protocol:** The OLED display communicates via the I2C bus at address 0x3C[cite: 18]. [cite_start]It uses only two wires (SDA/SCL) to send high-speed graphical data[cite: 19].
* [cite_start]**OneWire Protocol:** The HW-506 sensor converts temperature into a 12-bit digital signal within the sensor housing, which prevents signal degradation over wires[cite: 20, 21].
* [cite_start]**Power Efficiency:** The system operates at 5V and can be powered directly from the Arduino’s USB interface[cite: 22].

## 🚀 How to Run
1. [cite_start]Connect the hardware as per the wiring table[cite: 24].
2. [cite_start]Install the required libraries in the Arduino IDE[cite: 25].
3. [cite_start]Upload the source code sketch[cite: 26].
4. [cite_start]Open the **Serial Monitor (115200 baud)** to see the data log[cite: 27].
5. [cite_start]View the live temperature update on the OLED screen[cite: 28].
