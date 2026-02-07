# Analog-Interface-Design-and-Simulation

## 📌 Project Overview
This project presents the design, simulation, and analysis of a **multi-stage analog interface** built using operational amplifiers.  
The system processes low-level analog signals through amplification, filtering, programmable gain control, and final signal conditioning.

The project was developed as part of the **Systems with Analog Integrated Circuits** course.

---

## 🎯 Project Objectives
- Design a complete analog signal chain using op-amps
- Ensure correct biasing and linear operation of all stages
- Achieve the required gain, bandwidth, and distortion specifications
- Validate performance through DC, AC, and transient simulations

---

## 🧩 System Architecture
The system is composed of **four main stages**:

### 1️⃣ First Stage – Instrumentation Amplifier
- Amplifies a small differential input signal
- High CMRR for common-mode noise rejection
- Linear gain: **0.002 V/V**
- Bandwidth much higher than the filtering stage

**Key parameters:**
- Gain: 0.002 V/V  
- Bandwidth: 3.215 MHz  
- CMRR ≈ 126 dB  
- THD < 1%

---

### 2️⃣ Second Stage – Low-Pass Active Filter
- Limits the signal bandwidth
- Removes high-frequency noise
- High gain in the passband

**Key parameters:**
- Cutoff frequency: ≈ 3 kHz (simulated 4.22 kHz)
- Passband gain: **H₀ = 5000 (74 dB)**
- Quality factor: Q ≈ 1.41
- THD < 1%

---

### 3️⃣ Third Stage – Programmable Gain Amplifier (PGA)
- Adjustable gain using switched resistors
- Multiple discrete gain steps

**Gain steps:**
- 5 dB  
- 7 dB  
- 9 dB  
- 11 dB  

**Key parameters:**
- Gain range: 4.57 dB – 11.6 dB  
- Bandwidth >> 3 kHz for all gain steps
- THD < 1% for minimum and maximum gain

---

### 4️⃣ Fourth Stage – Output Conditioning Stage
- Final signal scaling
- Inverting amplifier configuration

**Key parameters:**
- Gain: 2 V/V
- Linear operation confirmed through DC sweep and transient analysis

---

## 🧪 Simulations Performed
- **DC Operating Point (DCOP)**
- **AC Frequency Response**
- **CMRR Analysis**
- **PSRR Analysis**
- **Transient Analysis**
- **Total Harmonic Distortion (THD)**

All simulations confirm compliance with the design specifications.

---

## 📊 Final Results Summary

| Stage | Parameter | Expected | Simulated |
|------|----------|----------|-----------|
| Stage 1 | Gain | 0.002 V/V | 1.99 mV |
| Stage 1 | Bandwidth | > 3 kHz | 3.215 MHz |
| Stage 1 | THD | < 1% | 0.12% |
| Stage 2 | Bandwidth | 3 kHz | 4.22 kHz |
| Stage 2 | Gain | 5000 | 74 dB |
| Stage 3 | Gain Min | 5 dB | 4.57 dB |
| Stage 3 | Gain Max | 11 dB | 11.6 dB |
| Stage 4 | Gain | 2 | 2.06 |

---

## 🛠 Tools Used
- Analog circuit simulator (SPICE-based)
- Operational amplifier macromodels
- Frequency and distortion analysis tools

---

## 👩‍🎓 Author
**Salajan Denisa Patricia**  
3rd Year – EA  
Technical University of Cluj-Napoca  

---

## 📄 License
This project is intended for **educational purposes only**.
