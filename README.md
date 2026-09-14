# Smart Anti-Theft Security System (ESP32)

An IoT-based vehicle anti-theft system designed to protect cars and motorcycles from unauthorized access. The system detects suspicious activity around the vehicle, triggers alarms, and allows the owner to monitor and control it remotely via a cloud dashboard.

**Detect → Analyze → React → Notify**

---

## 📋 Overview

This system protects a vehicle by combining motion sensing, sound-based authentication, and an automated locking mechanism, while streaming live status data to a cloud dashboard for remote monitoring.

---

## 🔧 Hardware Components

| Component | Role |
|---|---|
| **ESP32** | Main microcontroller and MQTT client |
| **Ultrasonic Sensor** | Detects motion/proximity near the vehicle |
| **Microphone Sensor** | Listens for a specific two-clap authentication code |
| **Servo Motor** | Acts as the vehicle's locking mechanism |
| **Buzzer** | Sounds the alarm on unauthorized activity |
| **LEDs** | Visual system-state indicator |

**LED Indications:**
- 🟢 Green — Safe mode
- 🟡 Yellow — Suspicious activity
- 🔴 Red — Theft detected

---

## ⚙️ System Features

- Motion detection around the vehicle
- Clap-based authentication for authorized users
- Alarm activation using buzzer and LED indicators
- Servo motor used as a vehicle locking mechanism
- Real-time monitoring through a cloud dashboard

---

## 📡 Communication

The system transmits sensor data using the **MQTT protocol** to a cloud dashboard built on **ThingSpeak** for remote monitoring.

---

## 🔄 Workflow

1. The ultrasonic sensor detects motion near the vehicle, initiating the security protocol.
2. The microphone sensor listens for a predefined clap pattern to identify an authorized user.
3. If the correct clap sequence is detected, the servo motor unlocks the vehicle.
4. If an incorrect sequence or unauthorized activity is detected, the buzzer and LED alarm activate and the vehicle stays locked.
5. Sensor data and system status are sent to the cloud dashboard in real time.

### System Scenarios

**Scenario 1 — Suspicious Activity**
- Motion detected, person nearby but no tampering
- → Warning mode: dashboard shows distance and time, Yellow LED turns on

**Scenario 2 — Theft Attempt**
- Motion detected at very close range for a long duration, with loud tampering sound
- → Alarm activated, vehicle doors locked, notification sent to the dashboard

---

## ✅ Advantages

- Low-cost solution
- Real-time monitoring from home
- Preventive security approach
- Easy installation
- Scalable and upgradable

---

## 🚀 Applications

- Vehicle anti-theft systems
- Smart garage security
- IoT-based security solutions

---

## 🔮 Future Improvements

- GPS tracking integration
- Camera monitoring
- Machine learning-based behavior analysis
- Biometric authentication (RFID or fingerprint)

---

## 📂 Repository Contents

- `docs/Smart-Anti-Theft-Security-System-Presentation.pdf` — full project presentation
- Firmware/code for the ESP32 (add as you upload it)

---

## 🛠️ Tools & Technologies

- ESP32 (Arduino framework)
- MQTT protocol
- ThingSpeak (cloud dashboard)
