# Hand Calculation: Series and Parallel Resistors

## Given values

| Network | Source | Resistors |
| --- | --- | --- |
| Series | `V1 = 9 V` | `R1 = 1 kΩ`, `R2 = 2 kΩ` |
| Parallel | `V2 = 9 V` | `R3 = 1 kΩ`, `R4 = 2 kΩ` |

## Series network

The equivalent resistance is

\[
R_{eq,s} = R_1 + R_2 = 1\,\mathrm{k\Omega}+2\,\mathrm{k\Omega}=3\,\mathrm{k\Omega}.
\]

The series current is therefore

\[
I_s = \frac{V_1}{R_{eq,s}}
= \frac{9\,\mathrm{V}}{3\,\mathrm{k\Omega}}
= 3\,\mathrm{mA}.
\]

The voltage drops are

\[
V_{R1}=I_sR_1=(3\,\mathrm{mA})(1\,\mathrm{k\Omega})=3\,\mathrm{V},
\]

\[
V_{R2}=I_sR_2=(3\,\mathrm{mA})(2\,\mathrm{k\Omega})=6\,\mathrm{V}.
\]

The drops satisfy KVL:

\[
V_{R1}+V_{R2}=3\,\mathrm{V}+6\,\mathrm{V}=9\,\mathrm{V}=V_1.
\]

The individual powers and total power are

\[
P_{R1}=I_s^2R_1=9\,\mathrm{mW},
\qquad
P_{R2}=I_s^2R_2=18\,\mathrm{mW},
\]

\[
P_{series,total}=P_{R1}+P_{R2}=27\,\mathrm{mW}.
\]

## Parallel network

The equivalent resistance is

\[
R_{eq,p}=\frac{R_3R_4}{R_3+R_4}
=\frac{(1\,\mathrm{k\Omega})(2\,\mathrm{k\Omega})}{1\,\mathrm{k\Omega}+2\,\mathrm{k\Omega}}
=666.6667\,\Omega.
\]

Both branches have the source voltage across them:

\[
V_{R3}=V_{R4}=V_2=9\,\mathrm{V}.
\]

The branch currents are

\[
I_{R3}=\frac{9\,\mathrm{V}}{1\,\mathrm{k\Omega}}=9\,\mathrm{mA},
\qquad
I_{R4}=\frac{9\,\mathrm{V}}{2\,\mathrm{k\Omega}}=4.5\,\mathrm{mA}.
\]

The total current is

\[
I_{p,total}=I_{R3}+I_{R4}=13.5\,\mathrm{mA}.
\]

The total power is

\[
P_{parallel,total}=V_2I_{p,total}
=(9\,\mathrm{V})(13.5\,\mathrm{mA})=121.5\,\mathrm{mW}.
\]

The branch powers are `81 mW` for `R3` and `40.5 mW` for `R4`.

## Analytical versus LTspice comparison

| Measurement | Analytical | LTspice | Approximate relative error |
| --- | ---: | ---: | ---: |
| Series current `I(R1)` | `3.000000 mA` | `3.000000002608 mA` | `8.69 × 10⁻⁸ %` |
| Series drop `V(n_s0,n_s1)` | `3.000000 V` | `3.000000 V` | `0 %` at displayed precision |
| Series drop `V(n_s1)` | `6.000000 V` | `6.000000 V` | `0 %` at displayed precision |
| Parallel current `I(R3)` | `9.000000 mA` | `8.999999961257 mA` | `4.30 × 10⁻⁷ %` |
| Parallel current `I(R4)` | `4.500000 mA` | `4.499999980628 mA` | `4.30 × 10⁻⁷ %` |
| Parallel voltage `V(n_p)` | `9.000000 V` | `9.000000 V` | `0 %` at displayed precision |

The tiny differences are numerical solver precision and do not indicate a physical-model discrepancy. The simulation verifies series addition, parallel equivalent resistance, KVL, voltage division, and current division for the selected ideal resistor networks.
