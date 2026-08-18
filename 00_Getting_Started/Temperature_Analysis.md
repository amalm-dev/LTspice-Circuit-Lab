# Temperature Analysis

Temperature analysis is meaningful when a device model or circuit parameter changes with temperature. Record the temperature range, step size, model assumptions, nominal reference temperature, and the quantities used to assess drift.

```spice
.temp -40 27 85
```

Do not add temperature sweeps to an ideal model merely to increase the number of plots. First identify the temperature coefficient or physical mechanism that the model represents, then compare the result with an analytical estimate where possible.
