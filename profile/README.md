# 🌞 SunWhirl  
### Hybrid Solar–Wind Intelligent Energy Platform

SunWhirl is a compact renewable-energy system that combines **solar** and **wind** power monitoring with **real-time communication**, **AI predictions**, and a **modern dashboard**.  
The project is designed as a modular prototype where the entire embedded layer runs on a **single Raspberry Pi**, while the backend, AI module, and dashboard operate as separate services.

---

## 🧱 System Components

### **1. Embedded Control (Raspberry Pi)**
All hardware subsystems run together on the Raspberry Pi and are stored in the same repository:
- Solar tracking and MPPT control  
- Wind turbine yaw optimization algorithm  
- Battery monitoring  
- Telemetry publishing via MQTT  

This device acts as the primary source of real-time data.

---

### **2. MQTT Communication**
A lightweight MQTT broker (e.g., Mosquitto) enables:
- Real-time streaming of sensor data  
- Low-latency communication between the Pi and backend  
- Decoupled, scalable system architecture  

---

### **3. Backend Service**
Processes incoming data and provides connectivity between components:
- Subscribes to MQTT telemetry  
- Sends data to the AI module  
- Stores historical metrics in a time-series database  
- Streams live data to the dashboard over WebSockets  
- Exposes REST endpoints for historical visualization  

---

### **4. AI Module**
A small standalone service used for Power forecasting (solar & wind)  
Backend communicates with it via HTTP.

---

### **5. Dashboard**
A web dashboard that visualizes:
- Live sensor data  
- Historical charts  
- AI predictions  
- System health indicators  

Built for clarity, speed, and real-time updates.

---

## 🎯 Project Purpose
SunWhirl demonstrates a unified renewable-energy monitoring system that merges:
- Embedded control  
- IoT data communication  
- AI-assisted insights  
- Web visualization  

The architecture is kept modular to allow each layer to evolve independently.

---

