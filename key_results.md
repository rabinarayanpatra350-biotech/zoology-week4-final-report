# Key results

Urban Noise, Light and Heat and the Vocal Behaviour of Birds — Final report (Week 4 capstone)

Rabi Narayan Patra | 19 October 2026

## The dataset

- 981 recordings, 24 cities, 30 species
- analysis sample: 922 recordings (909 with a usable activity rate)
- heat island intensity: 1.50 to 5.33 degC
- heat correlates 0.29 with noise and 0.37 with light

## The multi-stressor models

| Response | Stressor | Estimate | 95% CI | p |
|---|---|---|---|---|
| Signal: min freq (Hz) | noise | 4.6814 | 4.2198 to 5.143 | 6.531e-88 |
| Signal: min freq (Hz) | light | -0.2934 | -0.7739 to 0.1872 | 0.2315 |
| Signal: min freq (Hz) | heat | 0.9228 | -2.4964 to 4.342 | 0.5968 |
| Timing: onset (min) | noise | 0.0994 | 0.0536 to 0.1451 | 2.084e-05 |
| Timing: onset (min) | light | -0.4286 | -0.4904 to -0.3669 | 3.675e-42 |
| Timing: onset (min) | heat | -1.0329 | -1.4992 to -0.5667 | 1.413e-05 |
| Timing: onset (min) | noise x light | -0.0053 | -0.0107 to 0.0 | 0.05119 |
| Timing: onset (min) | heat x light | -0.0104 | -0.0509 to 0.0302 | 0.6161 |
| Effort: activity (songs/min) | heat | -0.1879 | -0.2147 to -0.1612 | 3.589e-43 |
| Effort: activity (songs/min) | noise | 0.0221 | 0.0184 to 0.0257 | 9.898e-33 |
| Effort: activity (songs/min) | light | -0.0002 | -0.0034 to 0.003 | 0.9097 |

## Ownership: unique R2 beyond species identity

| Response | Noise | Light | Heat | Owner |
|---|---|---|---|---|
| minimum frequency (Hz) | 0.0022 | 0.0000 | 0.0000 | **noise** |
| onset (min) | 0.0220 | 0.1489 | 0.0186 | **light** |
| activity rate (songs/min) | 0.0941 | 0.0000 | 0.1162 | **heat** |

## Power analysis

| Cities | Power: noise x light | Power: heat x light |
|---|---|---|
| 24 | 14% | 5% |
| 50 | 25% | 9% |
| 100 | 61% | 7% |
| 150 | 76% | 10% |
| 200 | 85% | 16% |
| 300 | 95% | 20% |

Cities needed for 80% power on noise x light: **200**
City-level residual SD: 0.75 min (recording-level: 5.08 min)

## Validation against ground truth

| Parameter | True | Recovered | 95% CI | Within CI |
|---|---|---|---|---|
| Noise -> minimum frequency | 5.0 | 4.6814 | [4.2198, 5.1430] | True |
| Light -> onset | -0.4 | -0.4286 | [-0.4904, -0.3669] | True |
| Heat -> onset | -0.9 | -1.0329 | [-1.4992, -0.5666] | True |
| Heat -> activity rate | -0.18 | -0.1879 | [-0.2147, -0.1612] | True |
| Heat x light -> onset | -0.003 | -0.0104 | [-0.0509, 0.0302] | True |
| Heat -> minimum frequency (built as zero) | 0.0 | 0.9228 | [-2.4965, 4.3420] | True |

## Robustness

| Effect | Point | Bootstrap 95% CI | Leave-one-city-out | Sign stable |
|---|---|---|---|---|
| noise -> min freq | 4.6814 | 3.8727 to 4.9922 | 4.4325 to 4.7816 | True |
| light -> onset | -0.4286 | -0.5745 to -0.3591 | -0.4505 to -0.4065 | True |
| heat -> onset | -1.0329 | -1.682 to -0.3927 | -1.2426 to -0.8583 | True |
| heat -> activity | -0.1879 | -0.2055 to -0.1563 | -0.1937 to -0.1776 | True |
