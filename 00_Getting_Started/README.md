# 00: Getting Started & Laboratory Standards

Welcome to the **LTspice Circuit Analysis & Design Laboratory**. This directory outlines the workflow, naming conventions, directory structure, and SPICE simulation standards used across all lab experiments.

---

## 1. Repository Directory Structure

The repository is structured hierarchically by topic, sub-topic, and specific experimental setup:

```text
LTspice-Circuit-Lab/
├── 00_Getting_Started/             # Setup guides, standards, and SPICE basics
├── 01_Basic_Electronics/           # Linear/Non-linear passive elements, KVL/KCL
│   ├── 01_Linear_Resistor/
│   │   ├── 01_Ideal_Resistor/      # Individual experiment folder
│   │   │   ├── assets/             # Screenshots, plots, and figures (.png)
│   │   │   ├── circuit.asc         # LTspice schematic source file
│   │   │   ├── circuit.net         # Generated SPICE netlist
│   │   │   ├── circuit.log         # LTspice simulation log
│   │   │   └── README.md           # Formal experiment report
│   │   └── 02_Series_Parallel/
│   └── 02_Non_Linear_Resistor/
├── 02_Circuit_Analysis/            # Thevenin, Norton, Nodal, Mesh, Superposition
├── 03_RLC_Circuits/                # Transient response, resonance, filters
├── 04_Semiconductor_Devices/       # Diodes, Zener regulation, rectifiers
├── 05_MOSFET/                      # MOSFET \(I\text{--}V\) characteristics, biasing
├── 06_CMOS/                        # CMOS digital logic, inverters, switching dynamics
├── 07_Analog_Amplifiers/           # Common Source, Common Emitter, frequency response
├── 08_Operational_Amplifiers/      # Inverting, Non-inverting, Integrator, Active Filters
├── 09_Feedback_Stability/          # Pole-zero analysis, Bode plots, Phase Margin
├── 10_Noise/                       # Thermal, flicker, and equivalent noise spectral density
├── 11_Advanced_Analysis/           # Monte Carlo, Worst-Case, Temperature sweeps
└── 12_CMOS_180nm/                  # Sub-micron CMOS technology node modeling
```
