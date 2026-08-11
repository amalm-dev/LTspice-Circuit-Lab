# LTspice Circuit Lab

An open-source simulation laboratory dedicated to exploring basic circuit theory, semiconductor device physics, and analog integrated circuit (IC) design using **LTspice**.

---

## Laboratory Objectives

* Verify theoretical hand calculations against SPICE simulation models.
* Characterize passive and active components across linear and non-linear operating regions.
* Analyze DC operating points (`.op`), small-signal AC responses (`.ac`), and large-signal transient dynamics (`.tran`).
* Document schematic topologies, SPICE netlists, simulation plots, and analytical notes.

---

## Laboratory Architecture

```text
LTspice-Circuit-Lab/
├── 00_Getting_Started/       # SPICE syntax, simulation directives, shortcuts
├── 01_Basic_Electronics/     # R, L, C, Diode topologies
├── 02_Circuit_Analysis/      # KCL, KVL, Thevenin, Norton, Superposition
├── 03_RLC_Circuits/          # Transient response, resonance, active/passive filters
├── 04_Semiconductor_Devices/ # PN junction, Zener, BJT characterization
├── 05_MOSFET/                # ID-VDS, ID-VGS, VTH, gm, ro, Body Effect
├── 06_CMOS/                  # Inverters, pass transistors, logic gates, ring oscillators
├── 07_Analog_Amplifiers/     # Common-Source, Common-Gate, Source Follower, Cascode, Diff Pair
├── 08_Operational_Amplifiers/# Two-stage CMOS op-amps, gain, bandwidth, slew rate
├── 09_Feedback_Stability/    # Loop gain, Phase Margin, Gain Margin, compensation
├── 10_Noise/                 # Thermal noise, flicker (1/f) noise, input-referred noise
├── 11_Advanced_Analysis/     # Parameter sweeps (.step), Monte Carlo, temperature sweeps
├── 12_CMOS_180nm/            # 180nm process simulations using custom .lib models
├── netlists/                 # Hand-crafted SPICE netlists (.cir) and subcircuits (.sub)
├── models/                   # Custom SPICE device models and foundry libraries
├── calculations/             # Python & symbolic hand-calculation scripts
└── notes/                    # Theoretical derivations and SPICE cheat sheets
```

---

## Simulation Matrix

| Domain | Analysis Type | SPICE Directive | Primary Parameters Extracted |
| :--- | :--- | :--- | :--- |
| **DC Operating Point** | Bias & Linearization | `.op` | $V_{GS}$, $V_{DS}$, $I_D$, $g_m$, $r_o$, Region of Operation |
| **DC Sweep** | Large-Signal / Non-Linear | `.dc` | Transfer Curves, Triode-to-Saturation Boundary, $V_{TH}$ |
| **AC Sweep** | Small-Signal / Linear | `.ac` | Frequency Response, Gain ($A_v$), Bandwidth, Phase Margin |
| **Transient** | Time-Domain / Dynamic | `.tran` | Slew Rate, Settling Time, Harmonic Clipping |
| **Fourier Analysis** | Non-Linear Distortion | `.four` | Total Harmonic Distortion (THD), Harmonic Amplitudes |
| **Noise Analysis** | Stochastic | `.noise` | Input-Referred Noise Spectrum ($\mathrm{nV}/\sqrt{\mathrm{Hz}}$) |

---

## Quickstart

1. Clone the repository:
   ```bash
   git clone [https://github.com/amalm-dev/LTspice-Circuit-Lab.git](https://github.com/amalm-dev/LTspice-Circuit-Lab.git)
   ```
2. Launch LTspice and open any `.asc` file within the module folders.
3. For custom model files, ensure the schematic includes the relative path directive:
   ```spice
   .include ../models/cmos180nm.lib
   ```
4. Press **Run (`F5`)** to execute the simulation.

---

<p align="center">
  <sub>Maintained by <b>Amal Madhu</b> • M.Tech VLSI & Analog Design</sub>
</p>
