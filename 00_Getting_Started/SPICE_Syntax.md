# SPICE Syntax

SPICE netlists describe a circuit as a collection of elements, node connections, values, models, and analysis directives. A line beginning with `*` is a comment. Element names normally begin with a letter that identifies the element family, such as `R` for resistor, `C` for capacitor, `L` for inductor, `V` for independent voltage source, and `I` for independent current source.

## Minimal example

```spice
* Voltage divider
V1 in 0 DC 5
R1 in out 1k
R2 out 0 1k
.op
.end
```

Node `0` is the reference node. Each element must connect to valid nodes, and the value suffix must be interpreted correctly. Common suffixes include `m` for milli, `u` for micro, `n` for nano, `p` for pico, `k` for kilo, and `meg` for mega. Treat `m` and `meg` as different quantities.

## Parameterized example

```spice
.param Rtop=1k Rbottom=1k
V1 in 0 5
R1 in out {Rtop}
R2 out 0 {Rbottom}
.step param Rtop list 500 1k 2k
.op
.end
```

Curly braces indicate parameter substitution. Keep parameter names descriptive, and record the nominal value and sweep range in the experiment README.

## Engineering checks

Every netlist should have a reference node, a solvable DC path where the selected analysis requires one, explicit units, and comments for non-obvious modelling choices. The schematic, netlist, README, and report must agree about node names, component values, source waveforms, and analysis directives.
