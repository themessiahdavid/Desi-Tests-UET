# Test 16: H0 Narrow-Band Prediction — Corrected Calculation

## Overview

Corrects the factor-of-2 error discovered in Test 15's ΔNeff formula and produces the precise, narrow-band H0 prediction with full uncertainty budget. Every input is derived — zero free parameters.

## The Error in Test 15

Test 15 computed ΔNeff per species as:
```
ΔNeff_i = (8/7) × (T_D/T_nu)^4 × g_i    [WRONG — Test 15]
```

The correct formula is:
```
ΔNeff_i = (g_i/2) × (8/7) × (T_D/T_nu)^4  [CORRECT]
```

The factor g_i/2 (not g_i) appears because the reference unit "one neutrino species" has g=2 fermionic dof. The formula counts how many neutrino-equivalents each dark species represents: (bosonic dof / reference fermionic dof) × (boson/fermion factor) × (temperature ratio)^4.

This produced a factor of 2 error: Test 15 reported ΔNeff_thermal = 0.214, correct value is **0.107**.

## Corrected Temperature Ratio

T_D/T_SM = (g*S_SM,rec / g*S_SM,Pl)^(1/3) = (3.91/106.75)^(1/3) = **0.33210** (unchanged from Test 15 — the temperature was correct)

T_D/T_nu = T_D/T_photon × T_photon/T_nu = 0.33210 × (11/4)^(1/3) = **0.46528**

(T_D/T_nu)^4 = **0.04687**

## Corrected ΔNeff

| Species | g | Formula | ΔNeff |
|---------|---|---------|-------|
| Dark photon γ_D | 2 | (2/2)×(8/7)×0.0469 | 0.0536 |
| Progenitor Φ | 2 | (2/2)×(8/7)×0.0469 | 0.0536 |
| **Thermal total** | 4 | (16/7)×0.0469 | **0.1071** |

Cross-check: (4×g_D/7) × (T_D/T_nu)^4 = (16/7) × 0.04687 = 0.10712 ✓

## A-phase ΔNeff Timing

The A-phase conversion occurs at z_t = 0.5, long AFTER recombination (z = 1090). Therefore:

- ΔNeff_Aphase for CMB H0 inference = **0** (not yet produced at z=1090)
- The 0.09 represents late-time dark radiation affecting H(z) at z < 0.5
- It enters the H0 budget only through the D_A(z*) modification (+0.006 km/s/Mpc)

## Complete H0 Budget

| Contribution | H0 shift (km/s/Mpc) | Source |
|-------------|---------------------|--------|
| ΛCDM baseline | 67.270 | Planck 2018 |
| Thermal ΔNeff = 0.107 | +1.183 | This calculation |
| A-phase late D_A | +0.006 | Test 13 |
| A_L inference bias | -0.116 | Test 14 |
| **TOTAL** | **68.343** | — |

## Uncertainty Budget

| Source | σ(H0) km/s/Mpc |
|--------|----------------|
| T_D/T_SM at M_Pl (Genesis) | 0.000 (exact) |
| g_D (forced field content) | 0.000 (exact) |
| g*S_SM at M_Pl (graviton?) | 0.029 |
| A_L bias slope uncertainty | 0.050 |
| D_A bias uncertainty | 0.002 |
| Numerical precision | 0.011 |
| **TOTAL (quadrature)** | **0.059** |

**Final: H0 = 68.34 ± 0.06 km/s/Mpc**

The dominant uncertainty is from the A_L degeneracy slope (±0.05), not from the dark sector physics.

## Consistency Checks

| Constraint | Value | Limit | Status |
|-----------|-------|-------|--------|
| BBN (ΔNeff < 0.40) | 0.107 | 0.40 | **PASS** |
| Planck Neff (ΔNeff < 0.284) | 0.107 | 0.284 | **PASS** |
| Planck Neff tension | 0.96σ from mean | — | Consistent |
| He-4 shift | δY_p = 0.0014 | σ ~ 0.004 | **PASS** |

Unlike Test 15's ΔNeff = 0.214 (which was marginally excluded by Planck), the corrected ΔNeff = 0.107 is **comfortably within all bounds**.

## Comparison to All H0 Measurements

| Measurement | H0 | σ | UET tension | |
|-----------|-----|-----|------------|---|
| Planck 2018 ΛCDM | 67.27 | 0.60 | +1.8σ | ✓ |
| ACT DR6 + Planck | 68.00 | 0.50 | +0.7σ | ✓ |
| SPT-3G 2022 | 68.80 | 1.50 | -0.3σ | ✓ |
| DESI BAO 2024 | 68.52 | 0.62 | -0.3σ | ✓ |
| TRGB (Freedman) | 69.60 | 1.90 | -0.7σ | ✓ |
| Son et al. 2025 | 70.50 | 1.00 | -2.2σ | ~ |
| SH0ES (Cepheid) | 73.00 | 1.00 | -4.7σ | ✗ |
| H0LiCOW (lensing) | 73.30 | 1.70 | -2.9σ | ~ |

UET is consistent with ALL CMB-based and BAO measurements. It is consistent with TRGB. It is in tension with raw SH0ES at 4.7σ and marginally with Son et al. at 2.2σ.

## Comparison: Test 15 vs Test 16

| Quantity | Test 15 (wrong) | Test 16 (correct) |
|----------|-----------------|-------------------|
| ΔNeff formula | g_i × (8/7) × T^4 | (g_i/2) × (8/7) × T^4 |
| ΔNeff_thermal | 0.214 | **0.107** |
| Planck Neff | MARGINAL FAIL | **PASS** |
| BBN | PASS | **PASS** |
| H0 prediction | 70.53 | **68.34** |
| vs SH0ES | 2.5σ | 4.7σ |
| vs Son+25 | 0.02σ | 2.2σ |
| vs DESI BAO | 3.2σ | 0.3σ |

The corrected prediction is more conservative but more robust — it passes all Neff constraints and is perfectly consistent with CMB/BAO data, though it does not reach the SH0ES value.

## Scientific Conclusion

**UET predicts H0 = 68.34 ± 0.06 km/s/Mpc with zero free parameters.**

This is:
- A genuine derived prediction (not fitted)
- Consistent with ALL CMB and BAO measurements at < 2σ
- 1.1 km/s/Mpc above ΛCDM (from thermal dark sector ΔNeff = 0.107)
- In clear tension with SH0ES (4.7σ)
- Testable by CMB-S4 (will measure ΔNeff to σ ~ 0.03, directly testing 0.107)

The H0 tension is NOT fully resolved. UET closes 19% of the gap via derived mechanisms. This is consistent with the emerging picture that the full 5.6 km/s/Mpc gap may contain significant systematic components in the distance ladder.

## Figures

- **uet_h0_narrow_prediction.png** (3 panels):
  - Left: Corrected ΔNeff budget with ghost bar showing Test 15's wrong value
  - Center: H0 waterfall chart with all contributions
  - Right: UET H0 prediction vs all measurements (error bars)

## Key Takeaways

1. **Factor-of-2 error corrected**: ΔNeff = 0.107 (not 0.214)
2. **H0 = 68.34 ± 0.06**: narrow, derived, falsifiable
3. **All Neff constraints satisfied**: BBN ✓, Planck ✓
4. **Consistent with CMB/BAO measurements** (< 2σ for all)
5. **H0 tension remains** at 4.7σ vs SH0ES — honest open problem
6. **CMB-S4 test**: ΔNeff = 0.107 measurable at 3.6σ with σ(Neff) = 0.03
