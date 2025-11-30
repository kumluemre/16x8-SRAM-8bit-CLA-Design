# 16x8 SRAM & 8-bit CLA Design

## Abstract
This project presents the full-custom design of a digital system integrating a **16x8 SRAM** and an **8-bit Carry Lookahead Adder (CLA)**. The design is implemented using **180nm CMOS technology** in **Cadence Virtuoso**.

## Key Features
The system performs read/write operations and high-speed addition of stored data with external inputs.

### 1. SRAM Architecture
The 16x8 SRAM block includes the following submodules:
* **6T Memory Cell Array:** Optimized for area and stability.
* **Sense Amplifier:** For fast low-swing signal detection.
* **Precharge Circuit:** Ensures bit-line equalization.
* **Write Driver & Row Decoder:** For reliable data access.
* **2-Phase Clock Generator:** Non-overlapping clock for timing synchronization.

### 2. Arithmetic Unit (CLA)
* An **8-bit Carry Lookahead Adder (CLA)** is integrated to perform fast addition, minimizing propagation delay compared to standard ripple carry adders.

## Implementation Details
* **Technology:** 180nm CMOS
* **Tools:** Cadence Virtuoso (Schematic & Layout)
* **Verification:** Post-layout simulation with parasitic extraction.

---

### 📄 Project Report
Click the link below to view the detailed design report, schematics, and simulation results:

[View Full Project Report (PDF)](./16x8-SRAM-8bit-CLA-Design.pdf)
