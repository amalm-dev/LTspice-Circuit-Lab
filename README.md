# LTspice Circuit Lab

**A structured, evidence-based simulation laboratory for an M.Tech VLSI student developing toward mixed-signal IC design, AI hardware, neuromorphic computing, memristive systems, accelerators, robotics, embedded systems, and IoT.**

This repository records a progression from circuit fundamentals to analog CMOS and process-aware 180 nm studies. Each experiment is organized around a physical or modelling question rather than around a list of LTspice commands. The purpose is not to collect screenshots; it is to make the chain from theory to circuit, simulation, measurement, comparison, and engineering interpretation reproducible.

> **Repository rule:** Every experiment uses the minimum set of analyses needed to answer its engineering question.

## Learning architecture

| Stage | Subject | Engineering direction |
| --- | --- | --- |
| `00` | Getting Started | LTspice, SPICE syntax, analyses, measurements, and laboratory standards |
| `01` | Basic Electronics | R, C, and L behaviour, parasitics, tolerances, and nonlinear models |
| `02` | Circuit Analysis | Kirchhoff laws, network methods, equivalent circuits, and small-signal reasoning |
| `03` | RLC Circuits | Impedance, transfer functions, filters, resonance, and time response |
| `04` | Semiconductor Devices | Diodes, BJTs, device characteristics, biasing, and small-signal models |
| `05` | MOSFET | Operating regions, threshold, body effect, short-channel effects, `g_m`, `r_o`, noise, and extraction |
| `06` | CMOS | Inverters, VTC, noise margins, delay, power, logic gates, current mirrors, and oscillators |
| `07` | Analog Amplifiers | Common-source, differential, cascode, active-load, and frequency-response studies |
| `08` | Operational Amplifiers | Multistage design concepts, OTA behaviour, CMRR, PSRR, slew rate, and stability |
| `09` | Feedback and Stability | Loop gain, poles, zeros, margins, compensation, and robust closed-loop design |
| `10` | Noise | Thermal, flicker, resistor, MOSFET, and input-referred noise |
| `11` | Advanced Analysis | Sweeps, tolerance, Monte Carlo, temperature, worst case, measurements, and statistics |
| `12` | CMOS 180 nm | Educational versus process-aware models and analog building blocks |

The broader professional direction includes open-source analog IC design, AI and neuromorphic hardware, memristor-inspired circuits, hardware accelerators, robotics, embedded systems, and IoT. This repository deliberately establishes the circuit-analysis foundation first; later repositories can extend the same evidence-based workflow into open-source EDA, digital VLSI, FPGA, embedded, and research projects.

## Experiment standard

A completed experiment should contain a concise `README.md`, the LTspice schematic and netlist under `simulation/`, hand calculations under `calculations/`, a report and references under `documentation/`, and explanatory figures under `assets/`. Generated `.raw` files are excluded unless a future experiment proves that publishing raw data is necessary for reproducibility.

The experiment README is a laboratory index, not a replacement for the report. It should state the objective, circuit, parameters, theory, selected analyses, results, analytical-versus-SPICE comparison, and engineering insight. Detailed derivations belong in the report or calculation record.

## Current status

The repository architecture has been rebuilt on the `restructure/clean-learning-architecture` branch. Stage 1 begins with `01_Basic_Electronics/01_Resistor/01_Ideal_Linear_Resistor/`. Its result files will be added only after the circuit is simulated, checked against hand calculations, and interpreted. Empty directories are represented by `.gitkeep` placeholders until real work replaces them.

## Reproducible workflow

1. Define the engineering question and the expected mathematical behaviour.
2. Draw the smallest circuit that answers the question.
3. Derive the expected result by hand before simulation.
4. Select only physically meaningful LTspice analyses.
5. Run the simulation and record parameters, plots, and measurements.
6. Compare analytical and simulated values, including error and likely causes.
7. Write the concise experiment README and the detailed report.
8. Commit a coherent experiment with a descriptive message.

## Repository hygiene

Do not add a new top-level folder for every analysis command. `.op`, `.dc`, `.ac`, `.tran`, `.noise`, `.step`, `.temp`, Monte Carlo, and measurement directives belong inside the subject or experiment where they have physical meaning. Do not commit passwords, proprietary foundry models, unlicensed course material, unnecessary generated files, or results that cannot be explained.

## Related professional direction

The repository is one part of a larger engineering portfolio. The intended funnel is:

`Circuit theory → LTspice evidence → analog CMOS → open-source IC flow → AI/neuromorphic hardware → embedded/robotics/IoT systems → research documentation → portfolio and CV`

The quality standard is therefore simple: every committed experiment should show what was learned, what was implemented, what was measured, and what remains uncertain.

## License

This project is released under the MIT License. See [LICENSE](LICENSE).
