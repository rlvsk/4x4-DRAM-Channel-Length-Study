# 4×4 DRAM Design and Channel Length Study (Cadence Virtuoso)

## 🔹 Project Overview

This project presents the design and simulation of a **4×4 DRAM array** using **Cadence Virtuoso** in **gpdk180 technology**.  
A complete DRAM subsystem was implemented, including:

- 1T–1C DRAM cells  
- Row decoder  
- Precharge circuitry  
- Custom-designed sense amplifier  
- Read/write control logic  

The primary focus of the project is to study the **qualitative effect of access transistor channel length** on DRAM behavior.

---

## 🔹 Tools & Technology

- **EDA Tool**: Cadence Virtuoso  
- **Simulator**: Spectre  
- **PDK**: gpdk180  
- **Supply Voltage**: 1.8 V  

---

## 🔹 DRAM Cell Design

- **Type**: 1T–1C DRAM  
- **Access Transistor**: NMOS  
- **Storage Capacitance**: 100 fF  
- **Operation**: Wordline-controlled access to bitline  

The channel length of the **access NMOS transistor** was varied while keeping the width constant to observe its impact on memory operation.

---

## 🔹 Peripheral Circuits

- **Row Decoder**: CMOS logic-based decoder  
- **Precharge Circuit**: Bitline precharge before read operation  
- **Sense Amplifier**: Custom CMOS-designed sensing circuit (no reference design used)  
- **Read/Write Control**: Proper timing coordination verified using transient simulations  

---

## 🔹 Channel Length Sweep Study

- **Swept Parameter**: Channel length (L) of DRAM access transistor  
- **Range**: 180 nm → 1000 nm  
- **Width**: Kept constant  

### Observations

- Increasing channel length **slows the charging and discharging** of the storage capacitor  
- Longer channel length results in:
  - Reduced drive current  
  - Slower bitline interaction  
  - Improved charge retention tendency  
- Shorter channel length enables faster access but leads to quicker discharge  

This study highlights the **trade-off between access speed and retention behavior** in DRAM design.

---

## 🔹 Simulations

- Transient read/write operation verified  
- Precharge, read, and write timing validated  
- Parametric sweeps performed using ADE  

All results are based on **qualitative waveform analysis**, suitable for architectural and device-level understanding.

---

## 🔹 Project Context

- **Type**: BTech course project  
- **Objective**: Understanding DRAM operation and device-level trade-offs  
- **Focus**: Impact of transistor channel length on memory behavior  

---

## 🔹 Disclaimer

This repository contains **schematic and simulation screenshots only**.  
No PDK files or proprietary models are included.
