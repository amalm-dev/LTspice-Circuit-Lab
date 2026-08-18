# Experiment 01: Ideal Linear Resistor

## Objective

Characterize the current-voltage behaviour of an ideal linear resistor and verify the relationship against hand calculations.

## Circuit and parameters

The planned circuit uses a voltage source `V1` and a resistor `R1 = 1 kΩ`. The source will be swept from `-10 V` to `+10 V` with a `10 mV` step. The voltage polarity and current reference direction must be stated in the schematic and report.

## Theory

For an ideal resistor,

```text
I = V/R
G = 1/R
P = VI = V²/R
```

The expected I-V characteristic is linear with slope `1/R`. Power is non-negative for a passive resistor under the adopted sign convention and follows a quadratic relationship with voltage magnitude.

## Selected LTspice analyses

| Analysis | Status | Engineering purpose |
| --- | --- | --- |
| `.dc` | Required | Characterize the I-V relationship |
| `.op` | Optional | Verify one reference operating point |
| `.step` | Optional | Study the effect of resistance value |
| `.ac` | Not required initially | An ideal resistor has frequency-independent impedance |
| `.tran` | Not required initially | No energy-storage state is being studied |
| `.noise` | Not required initially | Requires a meaningful resistor noise model and question |
| Monte Carlo | Later | Move tolerance methodology to the practical resistor study |

## Planned repository files

The schematic and netlist belong in `simulation/`. Handwritten engineering work belongs in `calculations/`. The detailed report and bibliography belong in `documentation/`. Schematic and result figures belong in `assets/`. Generated `.raw` output is intentionally not part of the publication set.

```text
01_Ideal_Linear_Resistor/
├── README.md
├── simulation/
├── calculations/
├── documentation/
└── assets/
```

## Results

This section will be completed after the LTspice run. It should include the measured slope, selected current values, power verification, and figures with meaningful captions.

## Analytical versus SPICE comparison

The final comparison should report analytical value, simulated value, absolute error, relative error, and an interpretation of any discrepancy. Do not fill this table with unverified values.

## Engineering insight

The ideal resistor is the baseline for later work on combinations, tolerance, temperature coefficient, noise, and nonlinear models. It is intentionally small: the goal is to establish a reliable experiment format before increasing circuit complexity.
