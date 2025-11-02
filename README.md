#Hardware-Accelerated A* Path Planning on Nexys A7-100T (Artix-7)

This project implements a hardware-accelerated A* path planner for a two-dimensional grid on the Digilent Nexys A7-100T (Artix-7 XC7A100T-1CSG324C) using Vivado 2024.2. The design uses a binary min-heap for the open set and a Manhattan heuristic for N/E/S/W motion with unit edge costs. A simple board-level top module exposes a “search complete” indicator on an LED so the hardware can be demonstrated without additional peripherals. A behavioral testbench prints an ASCII map of the grid and the recovered path to the simulator console, which makes functional verification straightforward.

#Motivation

A* is a widely used graph search algorithm, but software implementations can become latency-bound when the open set grows. This project evaluates whether a simple, fully synthesizable A* design—built from a sequential heap and compact on-chip memories—can achieve competitive latency and predictable resource usage on an FPGA. To make the result useful for a computer architecture course, the repository includes a methodology for comparing the Verilog design against a Python A* baseline under identical conditions.
