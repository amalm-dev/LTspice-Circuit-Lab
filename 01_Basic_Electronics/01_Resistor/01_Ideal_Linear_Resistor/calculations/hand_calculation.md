# Hand Calculation: Ideal Linear Resistor

## Given

| Quantity | Symbol | Value |
| --- | --- | ---: |
| Resistance | `R` | `1 kΩ` |
| Evaluation voltage | `V` | `5 V` |
| LTspice measured current | `I_SPICE` | `4.99999988824 mA` |

## Analytical current

For an ideal resistor, Ohm's law gives

\[
I = \frac{V}{R}
\]

Therefore,

\[
I_{analytical} = \frac{5\,\mathrm{V}}{1000\,\Omega}
= 0.005\,\mathrm{A}
= 5.000000\,\mathrm{mA}
\]

## Conductance

\[
G = \frac{1}{R}
= \frac{1}{1000\,\Omega}
= 1\,\mathrm{mS}
\]

The slope of the I–V curve is therefore `1 mS`.

## Power at 5 V

Using the passive-resistor relationship,

\[
P = VI = \frac{V^2}{R}
\]

\[
P_{5V} = \frac{(5\,\mathrm{V})^2}{1000\,\Omega}
= 0.025\,\mathrm{W}
= 25\,\mathrm{mW}
\]

## Analytical versus SPICE comparison

The absolute current error is

\[
\left|I_{SPICE}-I_{analytical}\right|
= \left|4.99999988824-5.00000000000\right|\,\mathrm{mA}
= 0.00000011176\,\mathrm{mA}
\]

or approximately `0.11176 nA`.

The relative error is

\[
\epsilon_r =
\frac{\left|I_{SPICE}-I_{analytical}\right|}
{I_{analytical}}\times 100
\approx 2.24\times 10^{-6}\%.
\]

This is numerical solver and display precision, not a physical modelling discrepancy. The ideal resistor model is linear and has no tolerance or temperature coefficient in this experiment.

## Conclusion

At `V = 5 V`, the analytical current is `5 mA` and LTspice reports `4.99999988824 mA`. The result verifies Ohm's law and the expected `1 mS` I–V slope within numerical precision. The corresponding ideal-resistor power is `25 mW`.
