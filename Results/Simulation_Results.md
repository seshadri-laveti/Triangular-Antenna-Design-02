# Simulation Results — Triangular Slotted Antenna – Design 02

## Original HFSS screenshots

- Geometry: `../Images/01_antenna_geometry.png`
- S11 plot: `../Images/02_s11_parameter.png`
- 3D gain pattern: `../Images/03_3d_gain_pattern.png`

## Visual interpretation of the supplied S11 graph

A deep S11 dip is visible around 7.3 GHz. The graph image does not provide a clear exact marker readout.

| Visual feature | Frequency (GHz) | S11 (dB) |
|---|---:|---:|
| 1 | 2.250 | -2.000 |
| 2 | 3.450 | -9.000 |
| 3 | 4.650 | -5.000 |
| 4 | 5.600 | -8.000 |
| 5 | 6.100 | -14.000 |
| 6 | 7.250 | -29.000 |
| 7 | 9.180 | -14.500 |

**Caution:** values in this table are transcribed or estimated from the screenshot labels/visual curve. They are not a substitute for the original HFSS exported sweep. For designs without visible numeric markers, treat all values as approximate.

## Gain plot legend

- Maximum displayed legend value: 1.97
- Minimum displayed legend value: 0.00

Confirm whether the plotted quantity is gain, realized gain or directivity and confirm the units in HFSS before reporting a peak gain in dBi.

## Illustrative data

`../data/illustrative_s11_dataset.csv` and `../figures/illustrative_s11_curve.png` are **synthetic illustrative examples** created to demonstrate data organization and plotting. They are not measured, simulated, digitized or exported HFSS results and must not be cited as actual antenna performance.

## Exact calculations required from HFSS export

Export frequency and dB(S(1,1)) to CSV and calculate:
- Resonant frequency at each local minimum.
- Lower and upper −10 dB crossings for each continuous band.
- Absolute bandwidth: BW = f_H − f_L.
- Center frequency: fc = (f_H + f_L)/2.
- Fractional bandwidth: FBW (%) = 100 × BW/fc.
- VSWR, if needed: VSWR = (1 + |Γ|)/(1 − |Γ|), where |Γ| = 10^(S11_dB/20).

A -10 dB threshold corresponds to |Γ| ≈ 0.316 and VSWR ≈ 1.925.
