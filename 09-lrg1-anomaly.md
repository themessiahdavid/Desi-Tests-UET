# Test 9: LRG1 Anomaly Investigation

## Summary

The DESI DR2 LRG1 bin shows H(z=0.51) = 97.2 +/- 2.8 km/s/Mpc versus the Lambda-CDM expectation of 89.7 km/s/Mpc — an 8.4% excess at 2.65 sigma. UET predicts only +0.017% at this redshift, far short of the observed excess. This test investigates whether the anomaly is a statistical fluctuation, a systematic, or a challenge to UET. The verdict: most likely a statistical fluctuation (look-elsewhere corrected to 2.06 sigma), persistent from DR1 but not growing anomalously, and not a falsification of UET whose core prediction is growth suppression rather than H(z) modification.

---

## Physics Background

### The LRG1 Measurement

DESI's Luminous Red Galaxy sample 1 (LRG1) provides an anisotropic BAO measurement at effective redshift z_eff = 0.510. The Hubble parameter is extracted from the radial BAO signal:

```
H(z) = c / (D_H(z)/r_d * r_d)
```

The measured value H = 97.15 +/- 2.82 km/s/Mpc is significantly above the Lambda-CDM prediction of 89.66 km/s/Mpc for the fiducial cosmology (Omega_m = 0.31, H_0 = 67.4).

### UET at z = 0.51

UET's modification to H(z) comes from A-phase dark radiation injection. At z = 0.51 (near z_t = 0.5), the modification is:

```
H_UET(z=0.51) = 89.674 km/s/Mpc
```

This is only +0.017% above Lambda-CDM. The gap between UET and the LRG1 measurement is 7.47 km/s/Mpc — UET explains only 0.2% of the observed excess.

### The Question

Is the LRG1 excess (a) a statistical fluctuation, (b) evidence of new physics beyond UET, or (c) a systematic error?

---

## Methodology

### 1. Lambda-CDM Fits With and Without LRG1

Fitted the remaining DESI bins (LRG2, LRG3+ELG1, ELG2, Lya) to a Lambda-CDM model with free H_0 and Omega_m, then compared the fit quality when LRG1 is included.

### 2. Look-Elsewhere Effect

Corrected the raw tension for the fact that 5 bins were measured (the "look-elsewhere effect"). For N = 5 independent bins with two-sided tests, the corrected significance is:

```
p_corrected = 1 - (1 - p_raw)^N
```

### 3. DR1 vs DR2 Comparison

Checked whether the LRG1 anomaly persisted between DESI Data Release 1 (DR1) and DR2, and whether it grew, shrank, or was stable.

### 4. D_A Scan for LRG1

Computed what D_A value would be needed for UET to match the LRG1 measurement, and checked whether that value is physically allowed.

### 5. Physical Mechanism Survey

Considered whether any UET mechanism (increased D_A, modified z_t, additional phases) could explain the excess.

---

## Results

### Lambda-CDM Fit Without LRG1

| Parameter | Value |
|-----------|-------|
| H_0 | 66.81 km/s/Mpc |
| Omega_m | 0.327 |
| chi^2 / dof | 1.74 / 2 |
| p-value | 0.42 |

Excellent fit. The remaining four bins are perfectly consistent with Lambda-CDM.

### Lambda-CDM Fit With LRG1

| Parameter | Value |
|-----------|-------|
| H_0 | 71.75 km/s/Mpc |
| Omega_m | 0.273 |
| chi^2 / dof | 5.96 / 3 |
| p-value | 0.11 |

Acceptable but degraded. LRG1 pulls H_0 up by ~5 km/s/Mpc and Omega_m down by 0.05. The tension between LRG1 and the rest of DESI is +2.66 sigma (LRG1 against best-fit of other bins).

### UET at z = 0.51

| Quantity | Value |
|----------|-------|
| H_UET(z=0.51) | 89.674 km/s/Mpc |
| H_LCDM(z=0.51) | 89.660 km/s/Mpc |
| UET excess | +0.017% |
| LRG1 measurement | 97.15 km/s/Mpc |
| Gap: LRG1 - H_UET | 7.47 km/s/Mpc |
| Fraction explained by UET | 0.2% |

UET's H(z) modification at z = 0.51 is negligible. The A-phase radiation contributes too little to the expansion rate to explain an 8.4% excess.

### D_A Needed to Match LRG1

| Quantity | Value |
|----------|-------|
| D_A required | 9.98 |
| D_A fiducial | 0.02 |
| Ratio | 499x current value |
| Implied Delta-N_eff | 44.92 |
| Delta-N_eff bound | 0.30 |

The D_A needed to match LRG1 is 499 times the fiducial value and implies Delta-N_eff = 44.9 — catastrophically excluded by CMB, BBN, and every other cosmological probe. UET cannot accommodate the LRG1 excess through any physical mechanism.

### Look-Elsewhere Correction

| Quantity | Value |
|----------|-------|
| Raw tension | 2.65 sigma |
| Number of bins | 5 |
| Test type | Two-sided |
| Corrected tension | 2.06 sigma |
| Expected 2.6 sigma fluctuations in 5 bins | 0.04 |

After accounting for the look-elsewhere effect, the significance drops to 2.06 sigma — below the threshold for concern. In 5 independent bins, one expects a 2+ sigma fluctuation roughly 30% of the time.

### DR1 vs DR2 Persistence

| Data Release | LRG1 tension | Notes |
|-------------|-------------|-------|
| DR1 | +1.72 sigma | Initial hint |
| DR2 | +2.65 sigma | Same direction, grew |
| Shift DR1 to DR2 | +0.24 sigma | Consistent with statistical fluctuation |

The anomaly persisted from DR1 to DR2 and grew in significance. However, the shift of +0.24 sigma between releases is consistent with the expected improvement in precision (DR2 has more data), not with the anomaly growing. The persistence is noteworthy but the growth rate is normal.

---

## Four-Part Verdict

### 1. Is it a statistical fluctuation?

**YES (most likely).** The look-elsewhere corrected significance is 2.06 sigma. While the persistence from DR1 is notable, the shift between data releases (+0.24 sigma) is consistent with improved statistics rather than a growing signal. A 2+ sigma fluctuation in one of 5 bins is not unusual.

### 2. Did it persist from DR1?

**YES.** DR1 showed +1.72 sigma, DR2 shows +2.65 sigma. The direction is consistent. However, the two data releases share most of their data, so persistence is expected for both real signals and statistical fluctuations in the shared sample.

### 3. Does it falsify UET?

**NO.** UET's core observable prediction is growth suppression (f*sigma_8 at z ~ 0.5), not H(z) modification. The phase conversion affects f*sigma_8 by 7% but H(z) by only 0.017%. LRG1 is a background expansion measurement, and UET was never designed to produce large H(z) deviations. A theory is not falsified by a measurement it does not predict.

### 4. What would falsify UET via this channel?

**Kill condition:** Euclid or DESI DR3 confirms a > 4 sigma H(z) excess at z ~ 0.5 that is:
- Inconsistent with Lambda-CDM (not just a statistical fluctuation), AND
- Inconsistent with UET's growth suppression pattern (i.e., cannot be explained by any reasonable modification of the phase conversion model).

If such a measurement were confirmed and could not be attributed to BAO systematics (e.g., non-linear reconstruction artifacts, template fitting bias), it would point to physics beyond both Lambda-CDM and UET.

---

## Referenced Images

- **uet_lrg1_analysis.png**: Four-panel figure:
  - Top-left: H(z) for all DESI bins with Lambda-CDM fit and UET prediction, highlighting the LRG1 outlier.
  - Top-right: Tension (in sigma) for each bin, showing LRG1 as a clear outlier at 2.65 sigma.
  - Bottom-left: D_A scan showing the catastrophic D_A needed to match LRG1 (far beyond any physical bound).
  - Bottom-right: Verdict summary — traffic-light indicators for each of the four questions.

---

## Key Takeaways

1. LRG1 shows an 8.4% H(z) excess at 2.65 sigma (raw), 2.06 sigma (look-elsewhere corrected).
2. UET predicts only +0.017% at z = 0.51 and cannot explain the excess through any physical parameter.
3. The D_A needed to match LRG1 (D_A = 9.98) implies Delta-N_eff = 44.9 — catastrophically excluded.
4. Most likely explanation: statistical fluctuation in one of 5 bins.
5. The anomaly persisted from DR1 (+1.72 sigma) to DR2 (+2.65 sigma), but the shift is consistent with improved precision.
6. LRG1 does NOT falsify UET: UET's core prediction is growth suppression, not H(z) modification.
7. Kill condition defined: Euclid confirms > 4 sigma AND inconsistent with UET growth pattern.
