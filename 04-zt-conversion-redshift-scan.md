# Test 4: Conversion Redshift z_t Scan

## Summary

This test varies the X-to-U conversion redshift z_t from 0.2 to 0.8 in 60 steps, recomputing all observables and the effective CPL fit at each step. Within the physically preferred corridor z_t in [0.3, 0.5], wa is stable (sigma = 0.045), UET moves monotonically toward DESI as z_t increases, but never reaches BAO+CMB 1-sigma. The w_eff(z) shape analysis reveals UET's unique observational fingerprint: a sigmoid cutoff that distinguishes it from smooth dynamical dark energy.

---

## Physics Background

### The Conversion Redshift z_t

The conversion redshift z_t is the epoch at which the X-to-U phase transition is half-complete. It is the most important single parameter in UET's dark sector phenomenology because it sets:

1. **When the growth suppression peaks**: The f*sigma_8 suppression is a Gaussian centered at z_t with width sigma_g = 0.15.
2. **When H(z) is modified**: The A-phase radiation injection peaks near z_t.
3. **The shape of w_eff(z)**: The effective equation of state deviates from -1 only at z < z_t + 2*Delta, creating a redshift-dependent signature.

### Physical Constraints on z_t

The preferred corridor is z_t in [0.3, 0.5], motivated by:
- z_t < 0.3: Conversion happens too late, insufficient growth suppression at measurable redshifts.
- z_t > 0.5: Conversion overlaps with higher-z BAO bins and risks violating Lya constraints.
- z_t = 0.5 is the fiducial value, coinciding with the epoch where DESI sees the strongest dynamical DE signal.

---

## Methodology

For each of 60 linearly-spaced z_t values from 0.2 to 0.8:

1. **Sigmoid recomputation**: f_U(a) updated with new a_t = 1/(1+z_t).
2. **H(z) recomputation**: Friedmann equation with z_t-dependent A-phase radiation.
3. **D_M(z) integration**: Comoving distance recomputed.
4. **Growth suppression**: Gaussian centered at z_t with width 0.15.
5. **CPL fit**: 200 x 200 grid search for best-fit w0 and wa.
6. **Mahalanobis distances**: To all three DESI constraint sets.
7. **w_eff(z) computation**: The effective equation of state as a function of redshift for each z_t.

---

## Results

### Effective CPL Parameters in the Physical Corridor

| z_t | w0 | wa | BAO only (sigma) | BAO+CMB (sigma) | Full (sigma) |
|-----|------|--------|-------------------|------------------|--------------|
| 0.30 | -1.00 | +0.02 | 0.90 | 1.63 | 5.45 |
| 0.35 | -1.00 | +0.02 | 0.89 | 1.61 | 5.42 |
| 0.40 | -1.00 | +0.07 | 0.80 | 1.52 | 5.26 |
| 0.45 | -1.01 | +0.12 | 0.72 | 1.43 | 5.12 |
| 0.50 | -1.02 | +0.16 | 0.68 | 1.41 | 5.06 |

### Key Question Answers

**Q1: Is wa stable across the physical corridor?**

YES. Within z_t in [0.3, 0.5], wa ranges from +0.02 to +0.16 with sigma = 0.045. The variation is monotonic: wa increases with z_t as later conversions produce more pronounced effective time variation in the dark energy equation of state.

Note: The wa = +0.39 value from Test 1 (fiducial z_t = 0.5 with D_A = 0.02) is higher than the +0.16 shown here because the full fiducial computation includes additional effects (growth weighting w_g = 3.0 in the joint fit). The z_t scan isolates the z_t dependence with other parameters at their scan baseline.

**Q2: Does any z_t value reach BAO+CMB 1-sigma?**

NO. The minimum BAO+CMB distance within the corridor is 1.41 sigma at z_t = 0.495. Even extending to z_t = 0.8 (outside the preferred range), the minimum is approximately 1.3 sigma.

**Q3: Which direction does UET move as z_t increases?**

TOWARD the DESI Full contour center. The Full Mahalanobis distance decreases monotonically from 5.45 sigma (z_t = 0.30) to 5.06 sigma (z_t = 0.50). Higher z_t means the conversion coincides better with the redshift range where DESI sees its strongest signal.

### w0 Behavior

w0 is remarkably stable: it stays between -1.00 and -1.02 across the entire corridor. This confirms that w0 is anchored near -1 by UET's near-Lambda-CDM distances, independent of z_t.

---

## w_eff(z) Shape Analysis — The UET Fingerprint

### The Sigmoid Cutoff

The most physically distinctive result of this test is the w_eff(z) shape (Plot 4). For each z_t value, w_eff(z) was computed as the effective equation of state that a CPL fitter would reconstruct.

Key features:

1. **All curves collapse to w = -1 at z > z_t + 2*Delta.** There is no deviation from Lambda-CDM before the conversion begins.
2. **Deviation onset tracks z_t.** The point where w_eff(z) first departs from -1 shifts with z_t.
3. **No deviation before conversion.** This is the critical distinction from smooth dynamical dark energy models (quintessence, etc.), which typically have w(z) varying continuously across all redshifts.
4. **The sigmoid cutoff is UET's unique signature.** A future binned w(z) reconstruction that shows w = -1 at z > 1 but w != -1 at z < 0.5-0.7 would be a smoking gun for UET over quintessence.

### Observational Implications

This shape makes a clear, falsifiable prediction:

- **Quintessence/k-essence**: w(z) varies smoothly. High-z deviations expected.
- **UET**: w(z) = -1 exactly at z > z_t + 2*Delta. Sharp transition at z ~ z_t.
- **Discriminator**: A non-parametric w(z) reconstruction (see Test 8) at z > 1.5 cleanly separates these hypotheses.

---

## Referenced Images

- **uet_zt_scan_sigma.png**: Mahalanobis distances to each DESI contour as a function of z_t. Shows the monotonic decrease toward DESI as z_t increases, with the physical corridor [0.3, 0.5] shaded.

- **uet_zt_scan_w0wa.png**: w0 and wa as functions of z_t. Demonstrates the stability of w0 near -1 and the monotonic growth of wa with z_t.

- **uet_zt_trajectory.png**: The trajectory traced by (w0, wa) as z_t varies, overlaid on the DESI constraint ellipses. Shows UET sweeping through the BAO-only ellipse along a characteristic diagonal.

- **uet_weff_shape.png**: w_eff(z) curves for z_t = 0.3, 0.4, 0.5, 0.6. The sigmoid cutoff is clearly visible: each curve departs from w = -1 at a redshift determined by z_t and returns to w = -1 at z = 0. This is the "fingerprint" plot distinguishing UET from smooth dynamical DE.

---

## Key Takeaways

1. wa is monotonically increasing with z_t but remains stable (sigma = 0.045) across the physical corridor.
2. w0 is pinned near -1 regardless of z_t — the distance constraint is robust.
3. UET moves toward the DESI Full center as z_t increases, but does not reach BAO+CMB 1-sigma within the allowed range.
4. The w_eff(z) sigmoid cutoff is UET's unique observational fingerprint, cleanly distinguishable from smooth dynamical dark energy.
5. Future binned w(z) reconstruction at z > 1 is the decisive test.
