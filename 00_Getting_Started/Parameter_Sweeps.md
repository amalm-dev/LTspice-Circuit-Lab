# Parameter Sweeps

A parameter sweep answers how a circuit changes when one design variable changes. Define the nominal value first, then choose a range that reveals the relevant trend without creating an unreadable plot.

```spice
.param Rload=1k
Rload out 0 {Rload}
.step param Rload list 500 1k 2k 5k
```

For a source sweep, use `.dc Vsource start stop step`. For multiple parameters, document the nesting order and the number of simulated cases. A sweep is not automatically a tolerance analysis: a deterministic list of values and a random distribution answer different questions.
