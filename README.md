<h1 align="center">⚙️ PLC Automation – Material Mixing System (CODESYS)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/PLC-CODESYS-blue?logo=siemens" alt="PLC"/>
  <img src="https://img.shields.io/badge/Language-Structured%20Text%20%7C%20CFC-green" alt="ST CFC"/>
  <img src="https://img.shields.io/badge/Application-Automation-orange" alt="Automation"/>
</p>

<p align="center">
  <b>Automated bulk material mixing process implemented in <i>CODESYS</i> using Structured Text (ST) and Continuous Function Chart (CFC).</b>
</p>

---

## 📌 Project Overview
This project simulates an **automated mixing process** for bulk materials.  
It uses **two bunkers**, **two conveyor belts**, and a **mixer** to handle products in precise quantities.  

The system logic is implemented in **CODESYS** using **Structured Text (ST)** and **CFC**, providing both flexibility and graphical control.

---

## ⚡ System Description

- **Bunkers (2x)**  
  - Equipped with **weight sensors** (for measuring 2kg batches)  
  - **Release valves** control discharge of materials  

- **Conveyor Belts (2x)**  
  - Driven by **motors**  
  - Transport material from bunkers to mixer  

- **Mixer (1x)**  
  - Driven by a **motor**  
  - Operates for a set mixing duration  
  - Equipped with a **release valve** to discharge mixed product  

---

## 🔄 Process Flow
1. **Bunker Filling** → Each bunker releases a specified quantity (e.g., **2 kg**) of material.  
2. **Conveyor Operation** → Conveyor belts transport the materials to the mixer.  
3. **Mixing** → The mixer motor runs for a specified mixing time (e.g., **30 seconds**).  
4. **Discharge** → Mixer release valve opens, sending the product to the next stage.  
5. **Cycle Repeats** → System resets for the next batch.  

---

## 🛠️ Implementation
- **Structured Text (ST)** used for:  
  - Weight sensor monitoring  
  - Batch size control logic  
  - Timer-based mixing sequence  
  - Valve & motor interlocks  

- **CFC (Continuous Function Chart)** used for:  
  - Process flow visualization  
  - Interconnection of timers, comparators, and motor controls  
  - Easier debugging and logical sequence representation  

---

## 📂 Repository Structure

---

## 📊 Control Logic Summary
- **Inputs:**  
  - Weight sensors (Bunker1_Weight, Bunker2_Weight)  
  - Start/Stop push buttons  
  - Emergency stop  

- **Outputs:**  
  - Bunker valves (Valve1, Valve2)  
  - Conveyor motors (Conveyor1_Motor, Conveyor2_Motor)  
  - Mixer motor (Mixer_Motor)  
  - Mixer discharge valve (Mixer_Valve)  

- **Timers:**  
  - T#10s (bunker release duration)  
  - T#30s (mixer operation)  

---

## 🚀 Future Enhancements
- Add **HMI interface** for operator control (start, stop, batch size entry).  
- Integrate **alarm & fault detection** (overweight, motor fault, emergency stop).  
- Implement **recipe control** for mixing different materials.  
- Add **data logging** for production tracking.  

---

<p align="center">
  <i>“Automating bulk material mixing for efficiency and reliability ⚡”</i>
</p>
