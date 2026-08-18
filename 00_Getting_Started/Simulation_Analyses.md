# Simulation Analyses

An analysis directive asks LTspice to solve a particular mathematical problem. Select an analysis because it answers the engineering question, not because it is available in the software.

| Directive | Meaning | Typical question | Main evidence |
| --- | --- | --- | --- |
| `.op` | Operating point | What are the DC node voltages and branch currents? | Bias values and device region |
| `.dc` | DC sweep | How does a circuit vary with a source or parameter? | I-V curve, transfer curve, operating range |
| `.ac` | Small-signal AC | What is the linearized frequency response around bias? | Magnitude, phase, poles, zeros, bandwidth |
| `.tran` | Transient | How does the circuit evolve in time? | Rise time, settling, delay, overshoot, energy |
| `.noise` | Noise analysis | What noise is generated and how is it referred to the input? | Spectral density and integrated noise |
| `.four` | Fourier analysis | What harmonics are present in a periodic transient waveform? | Harmonic amplitudes and distortion |
| `.step` | Parameter sweep | How sensitive is behaviour to a design variable? | Family of curves and trends |
| `.temp` | Temperature sweep | How does temperature affect the model or circuit? | Drift, corners, and thermal sensitivity |
| `.mc` | Monte Carlo | How does random variation affect yield or spread? | Distribution, mean, sigma, yield estimate |
| `.tf` | Transfer function | What is the low-frequency gain and resistance around an operating point? | Gain, input resistance, output resistance |
| `.meas` | Numerical measurement | Can a result be extracted reproducibly? | Named scalar values in the log |

For a simple ideal resistor, `.dc` is the primary analysis for the I-V characteristic. `.op` can verify one operating point, while `.step` becomes useful for resistance variation. `.ac`, `.tran`, `.noise`, and `.four` are not automatically meaningful for the ideal-resistor question; use them only when the physical model and question justify them.

## Assumption discipline

`.ac` is a small-signal linearization around a bias point. `.tran` solves time-domain behaviour and may depend on initial conditions and numerical timestep. `.noise` depends on device noise models and source definitions. Monte Carlo results are statistical estimates, not proof of yield unless the sample size, distributions, and acceptance criteria are documented.
