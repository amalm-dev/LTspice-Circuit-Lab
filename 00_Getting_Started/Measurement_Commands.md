# Measurement Commands

Measurement directives make simulation results auditable and reduce dependence on manually reading a graph. Use them for quantities that appear in the experiment's objective or comparison table.

```spice
.meas DC I_at_5V FIND I(R1) WHEN V(in)=5
.meas DC Vout_max MAX V(out)
.meas TRAN t_rise TRIG V(out) VAL=0.5 RISE=1 TARG V(out) VAL=4.5 RISE=1
.meas AC gain_at_1k FIND mag(V(out)/V(in)) AT=1k
```

The exact syntax depends on the analysis type. State the waveform, threshold, direction, and event number clearly. When a measurement can be ambiguous, include a plot and explain the chosen event in the README.

Use measurement names that describe the engineering meaning rather than the implementation detail. Keep units explicit in the comparison table and distinguish peak, RMS, average, magnitude, and phase quantities.
