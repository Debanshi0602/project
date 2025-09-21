# Low-Power Peripheral Accelerator for Sensor Data (Microwatt Integration)

## 📌 Project Overview
Embedded systems often need to handle high-frequency or noisy sensor data streams. Processing this raw data on the CPU (Microwatt) increases power consumption and latency.  
This project proposes a **low-power hardware accelerator** that preprocesses sensor data before handing it off to the Microwatt core.  

By integrating the accelerator as a peripheral, repetitive filtering and compression tasks are offloaded from the CPU, reducing switching activity and improving overall system efficiency.

---

## 🎯 Objectives
- Design and implement a **sensor preprocessing accelerator** in Verilog.  
- Provide two main functions:  
  - **Moving Average Filter** → for noise reduction.  
  - **Run-Length Compression** → for simple data compression.  
- Interface with Microwatt via a **memory-mapped I/O peripheral**.  
- Compare CPU-only vs. accelerator-based implementations in terms of performance and power.  
- Provide reproducible testbenches, simulation results, and PPA analysis.  

---

## 🏗️ Methodology
1. **RTL Design**  
   - Implement modules for filtering and compression.  
   - Develop a top-level wrapper for Microwatt integration.  

2. **Verification**  
   - Write Verilog testbenches to simulate real sensor data.  
   - Verify functional correctness of both filter and compressor.  

3. **Integration with Microwatt**  
   - Expose accelerator as a memory-mapped peripheral.  
   - Demonstrate data transfer between Microwatt and accelerator.  

4. **Evaluation**  
   - Run workloads in simulation (GHDL / Verilator).  
   - Measure cycle savings and switching activity.  
   - Compare against CPU-only software implementation.  

5. **Documentation & Results**  
   - Document block diagrams, methodology, and results.  
   - Summarize PPA (Power, Performance, Area) trade-offs.  

---

## 🔧 Tools & Technologies
- **HDL**: Verilog  
- **Simulation**: GHDL, Verilator  
- **Synthesis/PPA**: Yosys, OpenROAD  
- **Microwatt Core**: [OpenPOWER Microwatt](https://github.com/antonblanchard/microwatt)  
- **Version Control**: Git + GitHub  

---

## 📂 Repository Structure
