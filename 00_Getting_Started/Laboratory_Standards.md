# Laboratory Standards

Use numbered, descriptive directory names and lowercase filenames for simulation artefacts. Keep experiment-specific files with the experiment. Reserve global directories for genuinely global resources only. Do not commit `.raw` files, editor caches, personal credentials, proprietary models, or unexplained generated output.

Every completed experiment should identify the objective, assumptions, parameters, circuit, selected analyses, results, comparison, limitations, and engineering insight. A result without a baseline calculation is incomplete; a calculation without a reproducible circuit is also incomplete.

Before committing, check that the schematic opens, the netlist is consistent, plots have captions or explanatory names, units are correct, and the README does not claim results that have not been generated. Use Git history as a laboratory notebook: one coherent experiment per commit, with messages that describe the engineering change.
