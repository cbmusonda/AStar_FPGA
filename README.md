# Hardware-Accelerated A* Path Planning on Nexys A7-100T (Artix-7)

This project implements a fully synthesizable **A\*** path planner for a 2D grid in Verilog (Vivado 2024.2) on the **Digilent Nexys A7-100T (XC7A100T-1CSG324C)**, and is **explicitly designed to be compared against a Python A\*** baseline under identical conditions. The repository includes a minimal Python A* reference and a clear methodology to run an apples-to-apples performance evaluation (latency, nodes expanded, resource usage, and timing).

---

## ✨ Highlights

- **Hardware A\*** in Verilog-2001 with **binary min-heap** open set and **Manhattan** heuristic (4-connected N/E/S/W, unit cost).
- **Direct Python A\* comparison baked in**: reference script included; evaluation steps and result table scaffold provided.
- Configurable grid (default **32×32**), heap capacity, and data widths for architectural exploration.
- Built-in **performance counters**—`cycles` (latency) and `expanded` (nodes popped)—for rigorous HW/SW analysis.
- Behavioral testbench prints ASCII grid and recovered path for quick functional validation.
- Clean **XDC** for Nexys A7-100T (100 MHz clock, reset, LED). Simple top toggles **LED0 = done** for an instant board demo.




