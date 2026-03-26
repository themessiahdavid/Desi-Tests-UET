# Test 3: A-Phase Drag Parameter D_A Scan

## Summary

This test scans the A-phase dark radiation drag parameter D_A across its full range (0.005 to 0.15) to determine whether tuning D_A can bring UET into the DESI Full contour. The answer is definitively NO: D_A barely moves the effective w0, and no value simultaneously satisfies the Delta-N_eff bound, the theory-preferred range, and BAO+CMB 1-sigma.

---

## Physics Background

### The D_A Parameter

When dark matter undergoes X-to-U phase conversion, the process releases energy into an A-phase dark radiation component. The parameter D_A controls the amplitude of this radiative drag on the expansion rate:

```
H^2(z) = H^2_LCDM(z) + D_A * (radiative contribution from A-phase)
```

D_A directly modifies H(z) and therefore affects the geometric observables (D_M, D_H) that BAO measures. Larger D_A means more dark radiation, more expansion, and potentially a different effective w0.

### Constraints on D_A

1. **Theory preferred range**: D_A in [0.01, 0.05], motivated by the energetics of phase conversion.
2. **Delta-N_eff bound**: Additional radiation is constrained by CMB + BBN via the effective number of neutrino species. The relation is:

```
Delta-N_eff = 0.09 * (D_A / 0.02)
```

The current bound is Delta-N_eff <= 0.3, which implies D_A <= 0.067.

3. **Current fiducial**: D_A = 0.02.

### The Question

Can increasing D_A shift w0 from -1.05 toward -0.76 (DESI Full center) while remaining within physical bounds?

---

## Methodology

### D_A Scan

50 logarithmically-spaced values of D_A from 0.005 to 0.15 were tested. For each value:

1. Recomputed H(z) with the modified radiative term.
2. Recomputed D_M(z) via numerical integration.
3. Applied the standard 7% growth suppression (unchanged by D_A — growth suppression comes from the phase conversion itself, not the radiation).
4. Performed a CPL fit on a vectorized 150 x 150 grid in the w0-wa plane.
5. Computed Mahalanobis distances to all three DESI constraint sets.

### UET Lane Corridor

The UET "lane" was computed by varying all three parameters (z_t, Delta, D_A) within their physical ranges to map out the accessible region of the w0-wa plane.

---

## Results

### w0 and wa vs D_A

| D_A | w0 | wa | Delta-N_eff |
|-----|-----|----|-------------|
| 0.005 | -1.057 | +0.39 | 0.023 |
| 0.010 | -1.054 | +0.39 | 0.045 |
| 0.020 | -1.053 | +0.39 | 0.090 |
| 0.050 | -1.039 | +0.38 | 0.225 |
| 0.067 | -1.030 | +0.37 | 0.300 |
| 0.100 | -1.019 | +0.36 | 0.450 |
| 0.150 | -1.010 | +0.35 | 0.675 |

**D_A barely moves the needle.** Across a factor of 30 in D_A (0.005 to 0.15), w0 shifts by only 0.047 (from -1.057 to -1.010). The wa parameter is nearly constant at 0.35-0.39.

### Mahalanobis Distances vs D_A

**BAO only**:
- UET is inside 1-sigma at ALL D_A values tested.
- Range: 0.35 sigma to 0.51 sigma.
- D_A does not matter for BAO-only consistency.

**BAO+CMB**:
- UET enters 1-sigma only at D_A = 0.129.
- At D_A = 0.129: Delta-N_eff = 0.58 — this is EXCLUDED by a factor of 2.
- At the Delta-N_eff boundary (D_A = 0.067): UET is at approximately 1.4 sigma.

**Full (BAO+CMB+SNe)**:
- UET never enters 2-sigma at any D_A value tested.
- Minimum distance: approximately 4.5 sigma at D_A = 0.15 (itself excluded).

### Delta-N_eff Implications

| D_A | Delta-N_eff | Status |
|-----|-------------|--------|
| 0.02 (fiducial) | 0.090 | Well within bound |
| 0.05 (theory max) | 0.225 | Within bound |
| 0.067 (N_eff limit) | 0.300 | At boundary |
| 0.129 (BAO+CMB 1-sigma) | 0.580 | EXCLUDED |
| 0.150 (scan max) | 0.675 | EXCLUDED |

### The Critical Question: Can D_A Close the Gap?

**NO.** No value of D_A simultaneously satisfies all three requirements:

1. Delta-N_eff <= 0.3 (CMB+BBN bound) — requires D_A <= 0.067
2. D_A in [0.01, 0.05] (theory-preferred range)
3. BAO+CMB 1-sigma — requires D_A >= 0.129

These three constraints are mutually exclusive. The minimum D_A needed for BAO+CMB 1-sigma exceeds the maximum D_A allowed by Delta-N_eff by a factor of ~2.

---

## Physical Interpretation

### Why D_A Barely Moves w0

The effective CPL parameters are determined by a joint fit to distances (D_M) and growth (f*sigma_8). The key insight is:

- **D_A controls H(z) modification**, which affects D_M. But the D_M residuals between UET and Lambda-CDM are already tiny (< 0.1%), so even large D_A changes produce small D_M shifts.
- **Growth suppression dominates the CPL fit.** The 7% f*sigma_8 suppression is what drives wa away from zero. Growth suppression is set by the phase conversion physics, not by D_A.

Since the CPL fitter's chi-squared is dominated by the growth term (w_g = 3.0), and D_A does not affect growth, D_A has minimal leverage on the best-fit w0 and wa.

### Implications for UET

This result is actually a strength of UET: the model's predictions are robust to the least-constrained free parameter. The effective equation of state is determined by the conversion redshift z_t and the growth suppression amplitude, both of which are better motivated theoretically than D_A.

---

## Referenced Images

- **uet_da_scan_sigma.png**: Mahalanobis distance to each DESI contour as a function of D_A. Shows the BAO-only curve staying flat below 1-sigma, BAO+CMB slowly descending but not reaching 1-sigma within the allowed range, and Full staying above 4-sigma throughout.

- **uet_da_scan_w0wa.png**: w0 and wa as functions of D_A. Shows the near-flat wa and the very gradual w0 drift from -1.057 to -1.010. Vertical dashed lines mark the theory range [0.01, 0.05] and the Delta-N_eff boundary at 0.067.

- **uet_da_trajectory.png**: The trajectory traced by (w0, wa) as D_A varies, overlaid on the DESI constraint ellipses. Shows the trajectory running roughly parallel to the DESI Full ellipse rather than toward its center, explaining why increased D_A cannot close the gap.

---

## Key Takeaways

1. D_A has minimal leverage on the effective CPL parameters: a factor of 30 variation shifts w0 by only 0.047.
2. Growth suppression, not dark radiation, dominates the effective equation of state.
3. No physically allowed D_A value brings UET into BAO+CMB 1-sigma.
4. The fiducial D_A = 0.02 gives Delta-N_eff = 0.09, safely within the 0.3 bound.
5. This robustness is a feature: UET's predictions do not depend sensitively on its least-constrained parameter.
