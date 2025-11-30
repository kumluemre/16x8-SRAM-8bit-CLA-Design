# 16x8 SRAM & 8-bit Carry Lookahead Adder (CLA) Design

## 🚀 Project Overview
This project presents the full-custom mixed-signal design of a digital system integrating a **16x8 Static Random Access Memory (SRAM)** and an **8-bit Carry Lookahead Adder (CLA)**. The system is designed to perform high-speed arithmetic operations between stored memory words and external input data.

The design was implemented using **180nm CMOS technology** in **Cadence Virtuoso**, covering the complete flow from transistor-level schematic to physical layout and post-layout verification with parasitic extraction.

---

## 📊 Performance Metrics (Post-Layout Results)
The following results were obtained from analog extracted simulations (Post-Layout) at **1.8V** supply voltage:

| Metric | Value |
| :--- | :--- |
| **Technology** | 180nm CMOS |
| **Operating Frequency** | 100 MHz |
| **Read Access Time** | **1.79 ns** |
| **Write Access Time** | 2.16 ns (Worst Case) |
| **Total Layout Area** | **49,424 µm²** |
| **Total Power Dissipation** | 616 µW |
| **SRAM Core Area** | 33,726 µm² |

---

## 🛠️ System Architecture

### 1. SRAM Design (16x8-bit)
The storage unit utilizes a robust **6T Memory Cell** architecture. Key submodules include:
* **6T Bit-Cell Array:** Optimized for stability and area efficiency.
* **Two-Phase Non-Overlapping Clock:** Generated to synchronize precharge and read/write cycles, preventing short-circuit currents.
* **Precharge Circuit:** Pulls bit-lines to VDD during Phase 1 for fast sensing.
* **Sense Amplifier:** Detects low-swing voltage differences on bit-lines to accelerate read operations.
* **Row Decoder & Write Driver:** For precise address selection and data driving.

### 2. 8-bit Carry Lookahead Adder (CLA)
Instead of a slow ripple-carry architecture, a hierarchical **CLA** topology is used:
* Composed of two cascaded **4-bit CLA blocks**.
* Generates carry signals in parallel using **Generate (G)** and **Propagate (P)** logic.
* Significantly reduces critical path delay compared to standard adders.

---

## 💻 Tools & Verification
* **Schematic Entry:** Cadence Virtuoso Schematic Editor
* **Physical Layout:** Cadence Virtuoso Layout Suite XL
* **Verification:** DRC (Design Rule Check), LVS (Layout vs. Schematic)
* **Simulation:** Analog Design Environment (ADE) with **Parasitic Extraction** to account for interconnect capacitance and resistance.

---

## 📄 Project Report & Layouts
For detailed schematics, layout views (DRC/LVS clean), and waveform analysis, please refer to the full project report:

### 👉 [View Full Project Report (PDF)](./16x8-SRAM-8bit-CLA-Design.pdf)
