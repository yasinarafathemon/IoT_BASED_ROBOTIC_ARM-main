# 🤖 IOT_BASED_ROBOTIC_ARM

*A Brain-Controlled Interface (BCI) based robotic arm using ESP8266 & PCA9685.*

## 🚀 **Project Overview**
IOT_BASED_ROBOTIC_ARM is a **WiFi-controlled robotic arm** designed to function using **brain-computer interface (BCI) signals**. It integrates an **ESP8266 microcontroller**, a **PCA9685 PWM driver**, and **three MG996R servo motors** for precise motion control.

Users can **control the robotic arm via a web interface**, allowing directional movements:  
➡ **Left, Right, Up, Down, and Reset**  

---

## 🛠 **Hardware Components**
| Component       | Description |
|----------------|-------------|
| **ESP8266** | WiFi microcontroller to control the arm |
| **PCA9685** | 16-channel PWM driver for servos |
| **MG996R Servos (x3)** | High-torque motors for arm movement |
| **5V 5A Power Supply** | Dedicated power for stable servo operation |
| **Jumper Wires & Breadboard** | Connecting components together |

---

## 🔌 **Wiring Diagram**
### **Connections Between ESP8266 and PCA9685**
| PCA9685 Pin | ESP8266 Pin | Purpose |
|------------|------------|---------|
| **VCC** | 3.3V | PCA9685 logic power |
| **GND** | GND | Common ground |
| **SDA** | D2 (GPIO4) | I2C Data |
| **SCL** | D1 (GPIO5) | I2C Clock |


![IMG-20250207-WA0006](https://github.com/user-attachments/assets/3747ab3a-59df-4d4c-831e-f1f4e03699e8)



### **Servo Power Connection**
- **V+ (PCA9685) → External 5V Power**
- **GND (PCA9685) → Common GND**
- **Servos connected to PCA9685 channels (S1=0, S2=1, S3=2)**

---

## 💾 **Software Setup**
### **Required Libraries**
Install these libraries in **Arduino IDE**:
- `Adafruit PWM Servo Driver`
- `ESPAsyncWebServer`
- `ESPAsyncTCP`

### **Uploading the Code**
1. Open `ESP8266.ino` in **Arduino IDE**.
2. Connect **ESP8266** via USB.
3. Select **Board:** `NodeMCU 1.0 (ESP-12E Module)`.
4. Click **Upload** (✓).

---

## 🌐 **Web Interface Controls**
Users can control the arm using the web interface:

| **Button** | **Servo 1 (Clutch)** | **Servo 2** | **Servo 3** |
|------------|----------------|---------|---------|
| **Left** | 90° | 180° | 0° |
| **Right** | 90° | 0° | 0° |
| **Up** | 90° | 90° | 90° |
| **Down** | 90° | 180° | 90° |
| **Reset** | 0° | 90° | 90° |

### **Accessing the Web Interface**
1. **Power on ESP8266**.
2. Connect to **ESP8266 WiFi network**.
3. Open browser → Enter ESP8266 **IP Address**.
4. Click **buttons to move the robotic arm**.

---

## ⚡ **Troubleshooting**
| **Issue** | **Cause** | **Solution** |
|-----------|----------|-------------|
| **Servos not moving** | Power issue | Use **5V 5A power supply** |
| **Jittery movement** | Weak ground connection | **Check GND wiring** |
| **Web page not loading** | ESP8266 IP address changed | **Find IP in Serial Monitor** |

---

## 🎯 **Future Improvements**
🚀 **Integrate EEG-based brain control (BCI signals).**  
🚀 **Add WebSockets for real-time movement control.**  
🚀 **Use AI-based gesture recognition for automation.**  

---


## 📜 **License**
This project is **open-source** under the **MIT License**.NB: Wihtout my permission no one can change or use it.
---
