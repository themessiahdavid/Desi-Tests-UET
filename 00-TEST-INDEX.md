# UET vs DESI Analysis — Master Test Index

## Overview

This document indexes the complete set of quantitative tests comparing Universe Engine Theory (UET) predictions against DESI DR2 dark energy measurements. Each test isolates a specific observable or parameter dependency, building a cumulative case for how UET's late-time X-to-U phase conversion maps onto the apparent dynamical dark energy signal reported by DESI.

All tests use a common fiducial cosmology: Omega_m = 0.31, Omega_Lambda = 0.69, H_0 = 67.4 km/s/Mpc, Omega_DS = 0.27.

---

## Test Listing

| # | File | Title | One-Line Summary |
|---|------|-------|------------------|
| 1 | [01-effective-dark-energy-eos.md](01-effective-dark-energy-eos.md) | Effective Dark Energy Equation of State | UET's phase conversion produces effective CPL parameters w0=-1.05, wa=+0.39 — matching DESI's wa almost exactly. |
| 2 | [02-multi-contour-comparison.md](02-multi-contour-comparison.md) | Multi-Contour DESI Comparison | UET sits inside DESI BAO-only 1-sigma at 0.50-sigma and beats Lambda-CDM in every constraint set. |
| 3 | [03-da-parameter-scan.md](03-da-parameter-scan.md) | A-Phase Drag Parameter D_A Scan | D_A cannot close the w0 gap; growth suppression dominates the CPL fit. |
| 4 | [04-zt-conversion-redshift-scan.md](04-zt-conversion-redshift-scan.md) | Conversion Redshift z_t Scan | wa is stable across the physical corridor; UET moves toward DESI as z_t increases. |
| 5 | [05-high-z-null-test.md](05-high-z-null-test.md) | High-z Null Test vs DESI DR2 | UET's prediction that w_eff = -1 at z > 1.5 is supported by BAO and BAO+CMB data. |
| 6 | [06-class-boltzmann-validation.md](06-class-boltzmann-validation.md) | CLASS Boltzmann Solver Validation | Analytic Friedmann integration validated against full CLASS solver to 0.06% accuracy. |
| 7 | [07-lya-forest-leakage.md](07-lya-forest-leakage.md) | Lyman-alpha Forest Leakage Analysis | Standard FDM Lya mass bounds do not apply to UET — 8.5 orders of magnitude safer. |
| 8 | [08-nonparametric-wz-reconstruction.md](08-nonparametric-wz-reconstruction.md) | Non-parametric w(z) Reconstruction | Model-independent GP reconstruction confirms w(z>1.5) = -1 and DESI signal is low-z only. |
| 9 | [09-lrg1-anomaly.md](09-lrg1-anomaly.md) | LRG1 Anomaly Investigation | DESI LRG1 H(z=0.51) excess is most likely a 2.1-sigma statistical fluctuation; does not falsify UET. |
| 10 | [10-isw-cross-correlation.md](10-isw-cross-correlation.md) | ISW-Galaxy Cross-Correlation Prediction | UET predicts a peaked +16% ISW enhancement at z~0.85 returning to Lambda-CDM at z>1.5. |
| 11 | [11-fsigma8-growth-suppression.md](11-fsigma8-growth-suppression.md) | fσ8(z) Growth Suppression Test | UET fits 21 RSD measurements better than LCDM by Delta-chi2=+2.0 with zero free parameters; suppression amplitude independently confirms S8 corridor. |
| 12 | [12-bayesian-model-comparison.md](12-bayesian-model-comparison.md) | Bayesian Model Comparison + A_L | UET scores 11/14 anomalies with 0 free parameters vs IDE 12/14 with 3 params; A_L reduced from 1.1σ to 0.8σ via same growth mechanism as S8. |
| 13 | [13-hubble-tension-analysis.md](13-hubble-tension-analysis.md) | Hubble Tension Analysis | UET shifts H0 by +1.0 km/s/Mpc (18% of gap) via derived mechanisms only. H0 is an honest open problem — all other mechanisms are dead ends. |
| 14 | [14-al-h0-bias.md](14-al-h0-bias.md) | A_L — H0 Degeneracy | A_L pathway shifts H0 DOWNWARD by 0.12 km/s/Mpc (wrong direction). Updated UET H0 = 68.2 — gap remains 4.8σ. All 9 mechanisms exhausted. |
| 15 | [15-dark-sector-thermal-history.md](15-dark-sector-thermal-history.md) | Dark Sector Thermal History | Genesis derives T_D/T_SM = 0.332. Contains factor-of-2 error in ΔNeff (used g_i instead of g_i/2). SUPERSEDED by Test 16. |
| 16 | [16-h0-narrow-prediction.md](16-h0-narrow-prediction.md) | H0 Narrow-Band Prediction | CORRECTED: ΔNeff = 0.107 (not 0.214). H0 = 68.34 ± 0.06 km/s/Mpc. Passes all Neff bounds. Consistent with CMB/BAO. 4.7σ from SH0ES. |
| 17 | [17-wormhole-throat-search.md](17-wormhole-throat-search.md) | Wormhole Throat Search (LIGO O3) | Searched real LIGO O3b data (H1+L1) for throat oscillations. 11 coherent candidates — all instrumental (violin modes + microseismic). Null result sets first upper limits on throat GW emission. |

---

## Key Conclusions Across All Tests

1. **wa match**: UET's effective wa = +0.39 reproduces DESI's wa = +0.36 from first principles (Test 1).
2. **w0 offset**: The w0 gap (-1.05 vs -0.76) is driven by UET preserving near-Lambda-CDM distances, and cannot be closed by D_A tuning (Test 3) or z_t variation (Test 4).
3. **High-z null**: Both CPL reconstruction (Test 5) and non-parametric GP (Test 8) confirm w = -1 at z > 1.5, exactly as UET predicts.
4. **Lya safety**: UET evades standard fuzzy dark matter mass bounds by 8.5 orders of magnitude (Test 7).
5. **Boltzmann validation**: Analytic approximations are accurate to < 0.06%, well below measurement precision (Test 6).
6. **LRG1**: The anomalous DESI LRG1 bin neither supports nor falsifies UET; it is a likely statistical fluctuation (Test 9).
7. **Future discriminator**: ISW cross-correlation at z ~ 0.85 provides a clean 3-sigma test achievable with ACT DR6 + DESI (Test 10).
8. **fσ8 direct test**: UET fits compiled RSD data better than LCDM by Delta-chi2=+2.0 with zero free parameters; suppression amplitude 0.069 independently confirms the S8-derived 0.07 (Test 11).
9. **Model comparison**: UET scores 11/14 on the anomaly scorecard with zero free parameters, second only to IDE (12/14, 3 params). A_L tension reduced from 1.1σ to 0.8σ via the same growth suppression (Test 12).
10. **H0 derived prediction**: Genesis thermal history gives ΔNeff = 0.107 (corrected from 0.214 in Test 15). Final H0 = 68.34 ± 0.06 — consistent with all CMB/BAO at <2σ, 4.7σ from SH0ES. Passes all Neff bounds. H0 tension remains an open problem but with a parameter-free prediction (Tests 13-16).

---

## Image Files

All referenced image files are expected to reside in the same directory as these documentation files:

- `uet_desi_w0wa_contour.png` (Test 1)
- `uet_hubble_deviation.png` (Test 1)
- `uet_desi_multicontour.png` (Test 2)
- `uet_da_scan_sigma.png` (Test 3)
- `uet_da_scan_w0wa.png` (Test 3)
- `uet_da_trajectory.png` (Test 3)
- `uet_zt_scan_sigma.png` (Test 4)
- `uet_zt_scan_w0wa.png` (Test 4)
- `uet_zt_trajectory.png` (Test 4)
- `uet_weff_shape.png` (Test 4)
- `uet_desi_wz_comparison.png` (Test 5)
- `uet_desi_null_test.png` (Test 5)
- `uet_desi_binned_consistency.png` (Test 5)
- `uet_class_validation.png` (Test 6)
- `uet_lya_leakage.png` (Test 7)
- `uet_desi_nonparametric.png` (Test 8)
- `uet_lrg1_analysis.png` (Test 9)
- `uet_isw_prediction.png` (Test 10)
- `uet_fsigma8_comparison.png` (Test 11)
- `uet_model_comparison.png` (Test 12)
- `uet_hubble_analysis.png` (Test 13)
- `uet_al_h0_bias.png` (Test 14)
- `uet_thermal_history.png` (Test 15)
- `uet_h0_narrow_prediction.png` (Test 16)
- `uet_wormhole_search.png` (Test 17)
