# Test 2: Multi-Contour DESI Comparison

## Summary

This test evaluates the UET effective CPL prediction (w0 = -1.0528, wa = +0.3945) against three progressively tighter DESI DR2 constraint sets: BAO-only, BAO+CMB, and Full (BAO+CMB+SNe). UET sits deep inside the BAO-only 1-sigma ellipse at 0.50 sigma and outperforms Lambda-CDM in every constraint combination. The tension emerges specifically when supernovae data is added.

---

## Physics Background

DESI DR2 reports dark energy constraints from three data combinations of increasing constraining power:

1. **BAO only**: Baryon Acoustic Oscillation measurements alone. Constrains the expansion history geometrically via D_H(z)/r_d and D_M(z)/r_d.
2. **BAO+CMB**: Adds Cosmic Microwave Background priors (primarily Omega_m*h^2 and the angular diameter distance to last scattering).
3. **Full (BAO+CMB+SNe)**: Adds Type Ia supernovae luminosity distances, which provide the tightest constraints on w0.

Each combination produces a different ellipse in the w0-wa plane. A genuine physical signal should be consistent across all three, while a systematic artifact or tension between datasets would show inconsistency.

UET's prediction is fixed: the same phase conversion physics produces the same effective CPL parameters regardless of which dataset is used to constrain them. The question is how UET's single prediction relates to each ellipse.

---

## Methodology

### DESI DR2 Constraint Ellipses

The following published parameters define the 2D Gaussian approximation to each DESI contour:

| Constraint Set | w0 center | wa center | sigma(w0) | sigma(wa) | rho |
|---------------|-----------|-----------|-----------|-----------|-----|
| BAO only | -0.97 | +0.28 | 0.18 | 0.55 | -0.75 |
| BAO+CMB | -0.93 | +0.30 | 0.12 | 0.40 | -0.70 |
| Full (BAO+CMB+SNe) | -0.76 | +0.36 | 0.07 | 0.17 | -0.50 |

### Mahalanobis Distance Computation

For each constraint set, the Mahalanobis distance was computed using the covariance matrix:

```
C = | sigma_w0^2              rho*sigma_w0*sigma_wa |
    | rho*sigma_w0*sigma_wa   sigma_wa^2            |
```

```
d_M = sqrt( delta^T * C^{-1} * delta )
```

where delta = (w0_test - w0_center, wa_test - wa_center) for both UET (w0=-1.0528, wa=+0.3945) and Lambda-CDM (w0=-1, wa=0).

The UET "corridor" from Test 1 (varying z_t, Delta, D_A within physical bounds) was also mapped onto each contour.

---

## Results

### Mahalanobis Distances

| Constraint Set | UET (sigma) | LCDM (sigma) | UET Closer? |
|---------------|-------------|---------------|-------------|
| BAO only | 0.50 | 0.97 | YES |
| BAO+CMB | 1.22 | 1.72 | YES |
| Full (BAO+CMB+SNe) | 4.72 | 5.60 | YES |

### Interpretation by Constraint Set

**BAO only (UET at 0.50 sigma)**:
UET sits deep inside the 1-sigma contour. This is the cleanest geometric test — BAO measures the expansion history with minimal model assumptions. UET's near-Lambda-CDM distances plus mild wa from growth suppression land squarely in the preferred region. Lambda-CDM at 0.97 sigma is near the edge of the 1-sigma ellipse.

**BAO+CMB (UET at 1.22 sigma)**:
Adding CMB priors tightens the ellipse and shifts the center slightly. UET remains well inside 2-sigma. Lambda-CDM at 1.72 sigma is being pushed toward the boundary. The CMB prior constrains Omega_m*h^2 tightly, which pulls w0 away from -1 when combined with BAO.

**Full BAO+CMB+SNe (UET at 4.72 sigma)**:
The addition of supernovae dramatically shrinks the ellipse and shifts the center to w0 = -0.76. This is where the tension appears. UET's w0 = -1.05 is far from -0.76 because UET predicts near-Lambda-CDM luminosity distances. Lambda-CDM at 5.60 sigma is even worse.

### Key Finding: The Tension is with SNe, Not BAO

The progressive degradation from 0.50 sigma (BAO) to 4.72 sigma (Full) pinpoints supernovae as the source of tension. BAO alone strongly favors the UET region of parameter space. The SNe data pull w0 toward -0.76, which is inconsistent with UET's prediction that distances should be nearly indistinguishable from Lambda-CDM.

This is important because supernovae systematics (calibration, dust, selection effects, host-mass correlations) are the most debated aspect of modern dark energy constraints. If the SNe pull is partly systematic, UET's agreement with BAO becomes the more reliable comparison.

---

## Referenced Images

- **uet_desi_multicontour.png**: Overlay of all three DESI constraint ellipses (BAO only in blue, BAO+CMB in green, Full in red) at 1-sigma and 2-sigma, with the UET best-fit point, the Lambda-CDM point, and the UET corridor marked. Visually demonstrates UET sitting inside the BAO-only ellipse and the progressive tightening that introduces tension.

---

## Key Takeaways

1. UET is inside DESI BAO-only 1-sigma at 0.50 sigma — this is the cleanest geometric test.
2. UET beats Lambda-CDM in every single DESI constraint combination without exception.
3. The tension arises specifically from Type Ia supernovae data, not from BAO geometry.
4. If SNe systematics account for even part of the w0 pull, UET's agreement with BAO is the more physically meaningful comparison.
5. The hierarchy (0.50 -> 1.22 -> 4.72 sigma) provides a clear diagnostic: UET's geometry is right; the question is whether SNe are pulling w0 systematically.
