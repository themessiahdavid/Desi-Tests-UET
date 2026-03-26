# Test 14: A_L — H0 Degeneracy Analysis

## Overview

Tests whether reducing the CMB lensing amplitude to UET's predicted A_L = 0.943 shifts the Planck-inferred H0 upward (helping the H0 tension) or downward (worsening it). This is a follow-up to Test 13, investigating whether the A_L pathway offers any additional H0 relief.

## Physical Question

Planck fits LCDM to CMB data and finds A_L = 1.073 (above unity, the "lensing anomaly") correlated with H0 = 67.4. UET predicts A_L,eff = 0.943 through growth suppression (sigma8: 0.83 -> 0.78). When A_L is forced to different values in the Planck likelihood, H0 shifts along a degeneracy direction. What is that direction?

## Key Data: Planck 2018 Published Values

| Configuration | A_L | H0 | sigma8 | Omega_m | Source |
|--------------|-----|------|--------|---------|--------|
| LCDM baseline (A_L=1 fixed) | 1.000 | 67.27 +/- 0.60 | 0.8331 | 0.3166 | Planck 2018 VI Table 2 |
| A_L free best-fit | 1.073 +/- 0.069 | 67.32 +/- 0.65 | 0.8128 | 0.3103 | Planck 2018 VI Table 5 |

Critical observation: increasing A_L by 0.073 shifts H0 by only +0.05 km/s/Mpc. **A_L and H0 are nearly orthogonal in Planck.**

## Degeneracy Slopes from Planck Chains

| Parameter | Slope per unit A_L |
|-----------|-------------------|
| dH0/dA_L | +0.685 km/s/Mpc |
| dOmega_m/dA_L | -0.086 |
| dsigma8/dA_L | -0.278 |

The H0 slope is shallow — A_L primarily trades with sigma8 and Omega_m, not H0.

## Compiled dH0/dA_L Estimates

| Source | Slope |
|--------|-------|
| Planck chains (A_L free vs fixed) | +0.685 |
| Linear fit to Planck projections | +0.878 |
| Efstathiou & Gratton 2021 | +0.800 |
| Calabrese et al. 2013 | +1.200 |
| **Mean** | **+0.891 +/- 0.191** |

## Results at UET A_L = 0.943

Starting from Planck best-fit A_L = 1.073, UET shifts A_L by -0.130:

| Parameter | Shift |
|-----------|-------|
| Delta A_L | -0.130 |
| Delta H0 | **-0.116 km/s/Mpc** (DOWNWARD) |
| Delta Omega_m | +0.011 |
| Delta sigma8 | +0.036 |

**The A_L pathway shifts H0 in the WRONG DIRECTION.** Reducing A_L below 1 causes the CMB fit to infer slightly lower H0, not higher.

## ACT DR6 Cross-Check

ACT DR6 measures A_L = 1.01 +/- 0.10 (closer to 1 than Planck) and H0 = 67.9 +/- 1.5 (slightly higher). The naive slope from ACT is +63 km/s/Mpc per unit A_L — but this is misleading because ACT's higher H0 comes from different CMB spectra, not the A_L degeneracy alone. The Planck-internal slope (0.685) is more reliable for the A_L-specific degeneracy.

## Complete Updated H0 Budget

| Mechanism | H0 shift | Uncertainty |
|-----------|----------|-------------|
| Delta Neff = 0.09 (A-phase) | +1.000 | 0.100 |
| D_A(z*) modification | +0.006 | 0.001 |
| A_L CMB inference bias | **-0.116** | 0.025 |
| **TOTAL** | **+0.890** | **0.103** |

**UET H0 = 68.16 +/- 0.10 km/s/Mpc**

Previous estimate (Test 13, without A_L): 68.40 km/s/Mpc
A_L correction: -0.116 km/s/Mpc (shifted DOWN from -0.24 revision off the baseline reference)
The A_L correction makes the situation marginally worse, reducing the total derived H0 shift from +1.0 to +0.89 km/s/Mpc.

## Gap Analysis

| Comparison | UET H0 | Target | Gap | Tension |
|-----------|--------|--------|-----|---------|
| vs SH0ES (73.0) | 68.16 | 73.0 | 4.84 | 4.8 sigma |
| vs Son et al. (70.0) | 68.16 | 70.0 | 1.84 | 1.8 sigma |
| vs Son et al. (70.5) | 68.16 | 70.5 | 2.34 | 2.3 sigma |

Total gap closure: 0.89 km/s/Mpc = **15.9% of original 5.6 km/s/Mpc gap**.

## Key Finding

**The A_L -- H0 degeneracy runs in the WRONG DIRECTION for UET.**

Physical explanation: Reducing A_L means less CMB lensing smoothing. To compensate, the Planck fit increases Omega_m and sigma8 slightly, which requires slightly lower H0 to maintain the acoustic scale theta_star. The effect is small (-0.116 km/s/Mpc) but definitively the wrong sign for H0 resolution.

## All 9 H0 Mechanisms Evaluated

| # | Mechanism | Contribution | Status |
|---|-----------|-------------|--------|
| 1 | Delta Neff = 0.09 | +1.000 | REAL |
| 2 | D_A(z*) bias | +0.006 | Negligible |
| 3 | A_L CMB inference | -0.116 | WRONG DIRECTION |
| 4 | Dark photon Delta Neff | 0 | Never thermalized |
| 5 | Early A-phase | 0 | z_A=99, after recombination |
| 6 | Scalaron/f(R) | 0 | R=0 during radiation |
| 7 | SH0ES bias | 0 | UET=LCDM at z<0.3 |
| 8 | Terminal constraint | 0 | No energy injection |
| 9 | MDL selection | 0 | H0 is IC, not operator |

## Conclusion

UET predicts H0 = 68.2 +/- 0.1 km/s/Mpc after exhaustive evaluation of all derived mechanisms. The gap to SH0ES (73.0) remains 4.8 sigma. The A_L pathway, which was the last untested avenue, goes the wrong direction by 0.12 km/s/Mpc.

H0 is UET's one acknowledged open problem. The theory correctly predicts S8, wa, A_L, fsigma8, Lya consistency, and DESI BAO agreement — but cannot close the Hubble tension without either (a) systematic correction to the local H0 measurement, or (b) extension of UET's dark sector to produce larger early-time Delta Neff.

## Figures

- **uet_al_h0_bias.png** (3 panels):
  - Left: A_L -- H0 degeneracy line with Planck data, UET prediction, and SH0ES/Son et al. bands
  - Center: H0 budget waterfall showing LCDM baseline + each contribution
  - Right: Updated H0 consistency landscape with all measurements

## Relation to Other Tests

- **Test 12**: Established A_L,eff = 0.943 from growth suppression
- **Test 13**: Evaluated all H0 mechanisms except A_L bias → total +1.0 km/s/Mpc
- **Test 14 (this)**: Adds A_L bias → total +0.89 km/s/Mpc (slightly worse)
- Combined conclusion: H0 gap remains 4.8 sigma after all derived mechanisms exhausted
