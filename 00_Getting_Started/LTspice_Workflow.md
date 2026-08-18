# LTspice Workflow

Begin with a one-sentence engineering question. Define the expected relationship symbolically, choose nominal parameters, and calculate at least one reference result by hand. Draw the circuit with clear labels and save the schematic inside the relevant experiment's `simulation/` directory.

Run the minimum analysis set. Record the exact directive, source values, model names, temperature, and any solver settings that affect interpretation. Use `.meas` where a numerical result matters, and save plots as assets with meaningful names. Do not publish `.raw` files by default.

After simulation, compare the result with the analytical expectation. A discrepancy is useful only when it is investigated: check sign conventions, units, node orientation, initial conditions, model assumptions, and numerical settings. Finish by updating the experiment README and, when appropriate, a LaTeX report.

A good commit should represent one coherent learning unit. Prefer messages such as `feat(resistor): add ideal linear resistor dc characterization` over vague messages such as `update files`.
