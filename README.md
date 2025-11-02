# Hardware-Accelerated A* Path Planning on Nexys A7-100T (Artix-7)

A fully synthesizable **A\*** path planner for a 2D grid implemented in Verilog and targeted to the **Digilent Nexys A7-100T (XC7A100T-1CSG324C)** using **Vivado 2024.2**.  
The design uses a **binary min-heap** for the open set and a **Manhattan heuristic** (4-connected N/E/S/W moves, unit edge cost). A simple top module drives an LED so you can demo “path found” directly on hardware.

---

## ✨ Highlights

- Verilog-2001 RTL, portable and classroom-friendly
- Configurable grid (default **32×32**), heap capacity, and data widths
- Cycle counter (`cycles`) and node counter (`expanded`) for **quantitative evaluation**
- Behavioral testbench prints an ASCII map + recovered path
- Clean **XDC** for Nexys A7-100T (100 MHz clock, reset, LED)

---

## 📦 Repository Layout

