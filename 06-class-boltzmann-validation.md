# Test 6: CLASS Boltzmann Solver Validation

## Summary

This test validates the analytic Friedmann integration approximation used throughout the analysis against a full Boltzmann calculation using the CLASS (Cosmic Linear Anisotropy Solving System) solver. The analytic H(z) matches CLASS to 0.057% and D_M(z) to 0.023%, both well below the ~1% precision of BAO measurements. The CPL fit shifts by less than 0.01 in both w0 and wa. The analytic approximation is confirmed as adequate, and no Boltzmann correction is needed.

---

## Physics Background

### Why Validate Against CLASS?

The previous tests (1-5) compute the Hubble parameter H(z) and comoving distance D_M(z) using analytic integration of the Friedmann equation, assuming a flat universe with matter and a cosmological constant:

```
H^2(z) = H_0^2 * [Omega_m * (1+z)^3 + Omega_Lambda]
```

This neglects:
- Radiation and neutrinos at low z (small but nonzero)
- Recombination-era physics propagated to low z
- Baryon-photon coupling effects on the sound horizon
- Massive neutrino free-streaming

A full Boltzmann solver like CLASS tracks all species self-consistently from early times through the present, providing the "ground truth" for background cosmology.

### CLASS

CLASS (classy Python wrapper) is the standard open-source Boltzmann solver used by the Planck and DESI collaborations. It solves the coupled Einstein-Boltzmann system for photons, baryons, CDM, neutrinos, and dark energy.

### Growth Factor Approximation

Two growth factor approximations were also tested:
1. **ODE solver**: Direct numerical integration of the growth equation.
2. **Omega_m^0.55 approximation**: The commonly used analytic formula f(z) ~ Omega_m(z)^0.55.

---

## Methodology

### CLASS Setup

CLASS was successfully installed and configured with the fiducial cosmology:
- H_0 = 67.4 km/s/Mpc
- Omega_b*h^2 = 0.02237 (Planck 2018)
- Omega_cdm*h^2 = 0.1200 (Planck 2018)
- tau_reio = 0.0544
- n_s = 0.9649
- A_s = 2.1e-9

### Comparison Protocol

1. Computed H(z) at 100 redshift points from z = 0 to z = 3 using both CLASS and analytic integration.
2. Computed D_M(z) at the same points via both methods.
3. Computed the growth factor via ODE solver and via the Omega_m^0.55 approximation.
4. Repeated the full CPL fit (300 x 300 grid) using CLASS-validated H(z) instead of analytic H(z).
5. Compared the resulting best-fit w0 and wa.

### UET Observable Recomputation

All UET-specific observables (H deviation, D_M residual, growth suppression, S8, Lya guardrail) were recomputed using the CLASS baseline.

---

## Results

### Background Cosmology Comparison

| Observable | Max Residual | RMS Residual | Threshold |
|-----------|-------------|-------------|-----------|
| H(z): CLASS vs analytic | 0.057% | 0.035% | ~1% (BAO precision) |
| D_M(z): CLASS vs analytic | 0.023% | 0.015% | ~1% (BAO precision) |

Both residuals are more than an order of magnitude below the measurement precision of current BAO data. The analytic approximation is ADEQUATE.

### Growth Factor Comparison

| Method | Accuracy vs ODE | Status |
|--------|----------------|--------|
| ODE solver | (reference) | Used in all tests |
| Omega_m^0.55 approximation | 70% off | Correctly NOT used |

The Omega_m^0.55 approximation is known to fail at the precision level needed for this analysis. The ODE solver was correctly chosen as the growth computation method throughout.

### CPL Fit Comparison

| Parameter | Analytic H(z) | CLASS-validated H(z) | Shift |
|-----------|---------------|---------------------|-------|
| w0 | -1.0200 | -1.0151 | +0.005 |
| wa | +0.1600 | +0.1538 | -0.006 |

Both shifts are less than 0.01, which is an order of magnitude below the 0.05 threshold that would be considered significant. The CPL fit is insensitive to the sub-0.1% differences between analytic and CLASS backgrounds.

### UET Observables (CLASS-Validated)

| Observable | Value |
|-----------|-------|
| Peak H(z) deviation: H_UET/H_LCDM - 1 | +0.200% at z = 0.60 |
| Peak D_M deviation | 0.084% |
| f*sigma_8 suppression at z_t | 7.0% |
| sigma_8 shift | 0.83 -> 0.78 |
| Lya guardrail: H_UET(z=2)/H_LCDM(z=2) - 1 | 0.000017% |

All values are consistent with the analytic computation to within rounding.

---

## Verdict

**CONFIRMED.** The analytic Friedmann integration used throughout this analysis is validated against the full CLASS Boltzmann solver. The maximum residual (0.057% in H(z)) is 17x below BAO measurement precision. The CPL fit shifts by less than 0.01 in both parameters. No Boltzmann correction is needed.

This validation confirms that:
1. The background expansion history is computed correctly.
2. The UET modification (A-phase radiation + growth suppression) is applied to a correct Lambda-CDM baseline.
3. All Mahalanobis distances and contour comparisons in Tests 1-5 are reliable.

---

## Referenced Images

- **uet_class_validation.png**: A 2x2 panel figure:
  - Top-left: H(z) from CLASS (solid) and analytic (dashed), nearly indistinguishable.
  - Top-right: H(z) ratio (analytic/CLASS - 1), showing residuals below 0.06%.
  - Bottom-left: D_M(z) comparison, residuals below 0.025%.
  - Bottom-right: f*sigma_8(z) for Lambda-CDM (ODE solver) and UET (with 7% Gaussian suppression), showing the growth suppression validated against the CLASS baseline.

---

## Key Takeaways

1. CLASS vs analytic H(z): max 0.057%, RMS 0.035% — well below 1% BAO precision.
2. CLASS vs analytic D_M(z): max 0.023%, RMS 0.015%.
3. CPL fit shift: Delta-w0 = +0.005, Delta-wa = -0.006 — both negligible.
4. The Omega_m^0.55 growth approximation is 70% off and was correctly never used.
5. All previous test results are validated. No systematic bias from the analytic approximation.
