# Test 13: Hubble Tension Analysis — Derived Mechanisms Only

## Overview

Systematic investigation of whether UET can resolve the Hubble tension (H0 = 73.0 vs 67.4 km/s/Mpc, a 5.6 km/s/Mpc gap) through parameter-free, derived mechanisms. No tuning allowed — every prediction follows from existing UET parameters. This is the honest assessment.

## Fixed UET Parameters (all previously derived)

- H0_true = 67.4 km/s/Mpc (Planck CMB)
- z_t = 0.5, Delta = 0.1, D_A = 0.02, Omega_DS = 0.27
- m_Phi = 1e-22 eV, n_star/n_DM_today ~ 1e6
- epsilon_kinetic = 1e-49 (dark-SM kinetic mixing)
- delta_Neff_late = 0.09 (previously computed)

## Calculation 1: CMB H0 Inference Bias

Does UET's late-time H(z) modification create a systematic bias in CMB's H0 inference?

The CMB infers H0 from theta_star = r_s(z_star)/D_A(z_star) assuming LCDM. If D_A(z_star) differs between LCDM and UET, the inferred H0 shifts.

### Results

| Quantity | LCDM | UET | Difference |
|----------|------|-----|------------|
| D_A(z*) | 13927.88 Mpc | 13926.63 Mpc | -0.009% |
| D_A(z<2) | 5307.63 Mpc | 5307.25 Mpc | -0.007% |
| D_A(z>2) | 8620.26 Mpc | identical | 0% |

- H0 bias from D_A shift: **+0.006 km/s/Mpc** (negligible)
- H0 shift from late ΔNeff = 0.09: **+0.996 km/s/Mpc**
- Total Calculation 1: **+1.002 km/s/Mpc** (closes 17.9% of gap)

The UET H(z) modification at z ~ 0.5 barely changes D_A to recombination because it is a tiny perturbation integrated over a small fraction of the total path length.

## Calculation 2: Complete Dark Sector ΔNeff Budget

### Dark Photon Thermal History

With kinetic mixing epsilon = 1e-49, the thermalization rate Gamma ~ epsilon^2 * alpha * T. Setting Gamma = H(T) gives decoupling temperature:

T_dec = epsilon^2 * alpha * M_Pl = (1e-49)^2 * (1/137) * 1.22e28 = **8.9e-73 eV**

This is absurdly below T_CMB = 2.35e-4 eV, meaning the dark photon interaction rate was ALWAYS slower than Hubble — it was **never in thermal equilibrium** with the SM bath. Therefore:

**ΔNeff_darkphoton = 0** (never thermalized)

Note: The initial run had a logic bug that treated T_dec << T_EW as "thermalized" — this was caught and corrected. The correct interpretation is: T_dec below today's CMB temperature means the dark photon never achieved equilibrium at any epoch.

### Early A-Phase

The cosmic mean dark matter density equals n_star at redshift z_A = (n_star/n_0)^(1/3) - 1 = 99.

z_A = 99 < z_rec = 1090 → Early A-phase occurs AFTER recombination → **No contribution to CMB H0**.

### Complete Budget

| Source | ΔNeff | H0 shift |
|--------|-------|----------|
| Dark photon | 0.000 | +0.000 km/s/Mpc |
| Early A-phase | 0.000 | +0.000 km/s/Mpc |
| Late A-phase | 0.090 | +0.996 km/s/Mpc |
| **TOTAL** | **0.090** | **+0.996 km/s/Mpc** |

## Calculation 3: Local H0 Measurement Bias

Does the UET phase transition bias the SH0ES distance ladder?

SH0ES measures H0 using Cepheids and SNe Ia at z = 0.02-0.15. At these redshifts:

| z | H_UET/H_LCDM - 1 |
|---|------------------|
| 0.05 | -13.6 ppm |
| 0.15 | -79.4 ppm |

**UET is identical to LCDM at z < 0.3 to parts per million.** The SH0ES measurement is completely unaffected by the UET conversion at z_t = 0.5.

Distance modulus residuals mu_UET - mu_LCDM at SH0ES redshifts are < 0.001 mag — far below the ~0.15 mag measurement uncertainty.

## Calculation 4: What H0 Does UET Actually Predict?

UET prediction chain:
```
  Planck baseline:  67.40 km/s/Mpc
  + ΔNeff total:   + 1.00 km/s/Mpc
  + D_A bias:      + 0.01 km/s/Mpc
  = UET H0:         68.40 km/s/Mpc
```

| Comparison | UET H0 | Target | Tension |
|-----------|--------|--------|---------|
| vs SH0ES (73.0 +/- 1.0) | 68.4 | 73.0 | **4.6σ** |
| vs Son et al. (70) | 68.4 | 70.0 | **1.6σ** |
| vs Son et al. (71) | 68.4 | 71.0 | **2.6σ** |

ΔNeff needed to fully close gap to 73: 0.51 (current: 0.090, need 6x more).

## Calculation 5: Systematic Search for Missed Mechanisms

| Mechanism | Verdict | Reason |
|-----------|---------|--------|
| Dark photon thermal ΔNeff | DEAD END | T_dec = 8.9e-73 eV — never thermalized |
| Early A-phase (z > z_rec) | DEAD END | z_A = 99 — after recombination |
| Scalaron at z_eq | DEAD END | R = 0 during radiation domination |
| f(R) sound speed correction | DEAD END | c_s is electromagnetic, not modified |
| Late A-phase ΔNeff | COMPUTED | +1.0 km/s/Mpc |
| D_A(z*) bias | COMPUTED | +0.006 km/s/Mpc |
| SH0ES bias in UET | DEAD END | UET = LCDM at z<0.3 to ppm |
| MDL selects H0 | NOT DERIVED | H0 is initial condition, not operator |
| Terminal constraint | DEAD END | Selects histories, doesn't add energy |

Summary: 2 computed, 0 viable new sources, 5 dead ends, 1 not derivable from current axioms.

## Final Verdict

```
DERIVED H0 CONTRIBUTIONS:
  Late A-phase ΔNeff:    +0.996 km/s/Mpc
  D_A(z*) bias:          +0.006 km/s/Mpc
  All others:            +0.000 km/s/Mpc
  ─────────────────────────
  TOTAL:                 +1.002 km/s/Mpc

GAP:      5.6 km/s/Mpc
CLOSES:   1.0 km/s/Mpc (18%)
REMAINING: 4.6 km/s/Mpc
```

**UET DOES NOT RESOLVE the Hubble tension through derived mechanisms.**

UET shifts H0 from 67.4 to 68.4 — closing only 18% of the 5.6 km/s/Mpc gap. Every possible derived mechanism was exhausted:

- Dark photon ΔNeff: zero (never thermalized due to ε = 1e-49)
- Early A-phase: zero (occurs at z=99, after recombination)
- Scalaron/f(R): zero (inactive during radiation domination)
- SH0ES bias: zero (UET = LCDM at z < 0.3)
- D_A(z*) modification: negligible (0.009%)

### Consistency Paths

For UET to coexist with H0 measurements:

**(a) H0 tension is partly systematic.** Son et al. 2025 suggests SH0ES may overestimate H0 due to Cepheid progenitor age biases, placing H0_local ~ 70-71. At H0_local = 70, UET tension drops to 1.6σ — tolerable.

**(b) UET requires extension.** A new mechanism beyond current axioms (e.g., enhanced early-time dark sector activity with different n_star) could increase ΔNeff. This would require at least 1 new free parameter.

**(c) H0 is an honest open problem for UET.** UET resolves S8, wa, Lya, A_L, and fsigma8 but does not close the H0 gap. This is scientifically honest — a theory that resolves 5 tensions while honestly failing on 1 is more credible than one that claims to solve everything.

### Context

No model in current cosmology resolves H0 without introducing new free parameters. EDE (3 params) achieves H0 ~ 71 but worsens S8. IDE (3 params) achieves H0 ~ 69.5. UET achieves H0 ~ 68.4 with 0 free parameters — a smaller shift, but from a parameter-free prediction.

## Figures

- **uet_hubble_analysis.png** (2 panels):
  - Left: Horizontal bar chart of each mechanism's H0 contribution, with gap and total markers
  - Right: H0 consistency landscape showing Planck, SH0ES, UET, and Son et al. distributions

## Key Takeaways

1. **UET shifts H0 by +1.0 km/s/Mpc** (67.4 → 68.4) through late-time ΔNeff = 0.09
2. **All other mechanisms are dead ends**: dark photon never thermalized, early A-phase after recombination, scalaron inactive during radiation era, SH0ES unbiased
3. **Gap remains 4.6 km/s/Mpc** (4.6σ vs SH0ES, 1.6σ vs Son et al. corrected value of 70)
4. **Honest conclusion**: H0 is an open problem for UET, not a resolved tension
5. **Critical bug found and fixed**: initial code incorrectly computed ΔNeff_darkphoton = 0.57 due to logic error in thermal equilibrium check (T_dec = 8.9e-73 eV was treated as "thermalized" instead of "never thermalized"). Corrected result: ΔNeff_darkphoton = 0.
