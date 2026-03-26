# Test 7: Lyman-alpha Forest Leakage Analysis

## Summary

This test determines whether standard Lyman-alpha forest constraints on fuzzy dark matter (FDM) masses apply to UET. Standard bounds require m > 2 x 10^-20 eV because they assume dark matter was always fuzzy at z = 2-5. UET's sigmoid has f_U(z >= 2) effectively zero — dark matter was CDM-like at those redshifts. The result: UET is 8.5 orders of magnitude safer than standard FDM at the same mass, and standard Lya bounds DO NOT APPLY.

---

## Physics Background

### Standard FDM Lya Constraints

The Lyman-alpha forest probes the matter power spectrum at small scales (k ~ 1-10 h/Mpc) and high redshifts (z = 2-5). Fuzzy dark matter (FDM) with ultralight mass m_Phi suppresses power below a characteristic half-mode scale:

```
k_{1/2} = 5.1 * (m / 10^{-22} eV)^{4/9} h/Mpc
```

(from Schive et al. 2016). Standard analyses fit the Lya flux power spectrum and exclude masses below m ~ 2 x 10^{-20} eV at 95% confidence.

### Why Standard Bounds Assume "Always Fuzzy"

The standard constraint assumes the FDM component has been present with its wave-like behavior since early times. At z = 3, the matter power spectrum has already been suppressed by the FDM quantum pressure for billions of years. The accumulated suppression is what the Lya forest measures.

### UET's Crucial Difference

In UET, dark matter starts as X-phase (CDM-like) and converts to U-phase (wave-like) via the sigmoid f_U(a). At high redshifts:

```
f_U(z) = (1/2) * [1 + tanh((ln(a) - ln(a_t)) / Delta)]
```

Since a_t = 1/(1 + z_t) = 1/1.5 = 0.667 and Delta = 0.1, at z = 3 we have a = 0.25, ln(a) = -1.386, ln(a_t) = -0.405, so (ln(a) - ln(a_t))/Delta = -9.81, and tanh(-9.81) = -1.000000. Thus f_U(z=3) is exponentially small.

The power spectrum suppression is proportional to f_U^2, so UET's suppression at Lya redshifts is negligible regardless of the U-phase particle mass.

---

## Methodology

### Step 1: Compute f_U Leakage at Lya Redshifts

Evaluated the sigmoid at z = 2, 3, 4, 5 to quantify the conversion fraction during the Lya-relevant epoch.

### Step 2: FDM Transfer Function

Used the standard FDM transfer function from the literature:

```
T(k) = cos(x^3) / (1 + x^8)
```

where x = k / k_{1/2}, applied at the half-mode scale k_{1/2} = 5.1 * (m / 10^{-22} eV)^{4/9} h/Mpc.

### Step 3: UET Power Spectrum Suppression

The UET matter power spectrum is a mixture of CDM and U-phase components:

```
P_UET(k) = [(1 - f_U) + f_U * T(k)]^2 * P_CDM(k)
```

The relative suppression is:

```
|Delta-P / P| = |P_UET / P_CDM - 1|
```

### Step 4: Mass Scan

Scanned m_Phi from 10^{-24} to 10^{-18} eV to find the mass at which UET suppression exceeds the Lya sensitivity threshold (taken as 5%).

---

## Results

### f_U Leakage at Lya Redshifts

| Redshift | f_U | Description |
|----------|-----|-------------|
| z = 2.0 | 9.5 x 10^{-7} | Less than one part per million |
| z = 3.0 | 3.0 x 10^{-9} | Three parts per billion |
| z = 4.0 | 3.5 x 10^{-11} | 35 parts per trillion |
| z = 5.0 | 9.1 x 10^{-13} | Sub-trillion |

The conversion fraction at Lya redshifts is negligibly small. Even at z = 2 (the lowest Lya redshift), only one millionth of the dark matter has converted.

### Power Spectrum Suppression at k_{1/2} = 5.1 h/Mpc, z = 3

| Model | m_Phi | |Delta-P / P| | Status |
|-------|-------|-------------|--------|
| Standard FDM | 10^{-22} eV | 19.0% | RULED OUT by Lya |
| UET | 10^{-22} eV | 6 x 10^{-10} | SAFE |

**Ratio: 3.14 x 10^8** — UET is 8.5 orders of magnitude safer than standard FDM at the same mass.

### Mass Scan Result

| Quantity | Standard FDM | UET |
|----------|-------------|-----|
| Lya lower bound on m_Phi | m > 7 x 10^{-22} eV | NONE |
| Suppression at m = 10^{-22} eV | 19% (excluded) | 6 x 10^{-10} (undetectable) |
| Suppression at m = 10^{-24} eV | ~100% (excluded) | < 10^{-6} (undetectable) |

At no mass does UET's suppression at Lya redshifts exceed the 5% detection sensitivity. The Lya constraint simply does not apply.

### UET Preferred Mass m = 10^{-22} eV: ALLOWED

The UET-preferred U-phase mass of 10^{-22} eV is excluded by standard FDM Lya bounds (19% suppression) but is fully allowed in UET (6 x 10^{-10} suppression). This resolves what would otherwise be a severe tension.

---

## Physical Interpretation

### Why the Sigmoid Makes All the Difference

Standard FDM assumes the wave-like component has been present since the early universe. At z = 3, billions of years of quantum pressure have accumulated, suppressing structure at small scales.

UET's sigmoid ensures that at z = 3, essentially zero dark matter has converted to the wave-like U-phase. The small scales probed by the Lya forest were built entirely from CDM-like X-phase dark matter. By the time conversion begins (z ~ 0.7), the Lya-epoch structure is long established.

This is not fine-tuning — it is a natural consequence of the fact that phase conversion happens at z_t = 0.5, which is cosmologically recent. The exponential suppression of the sigmoid tail does the rest.

### Resolving the Mass Tension

Without this analysis, one might object that UET requires ultralight bosons (m ~ 10^{-22} eV) which are excluded by Lya data. This test shows that objection is based on applying constraints derived under assumptions that UET violates. The standard bounds assume "always fuzzy"; UET's dark matter was "recently converted."

This is analogous to applying solar neutrino bounds derived assuming no oscillations — the bounds are correct given their assumptions but do not apply when the underlying physics differs.

---

## Referenced Images

- **uet_lya_leakage.png**: Six-panel figure:
  - Panel 1: The sigmoid f_U(z) showing the exponential suppression at z > 1.
  - Panel 2: P(k) suppression for standard FDM vs UET at z = 3, showing 8.5 orders of magnitude difference.
  - Panel 3: T^2(k) — the FDM transfer function squared, showing the characteristic oscillatory suppression.
  - Panel 4: Mass scan — |Delta-P/P| vs m_Phi for standard FDM and UET, with the 5% detection threshold marked.
  - Panel 5: Bar chart comparing suppression amplitudes for standard FDM vs UET at key masses.
  - Panel 6: Summary panel with key numerical results.

---

## Key Takeaways

1. UET's f_U at Lya redshifts is negligible: 10^{-7} at z = 2, 10^{-9} at z = 3.
2. Power suppression at z = 3 is 8.5 orders of magnitude below standard FDM at the same mass.
3. Standard Lya mass bounds (m > 2 x 10^{-20} eV) DO NOT APPLY to UET.
4. UET's preferred mass m = 10^{-22} eV is ALLOWED — the apparent tension with Lya bounds is resolved.
5. This is not fine-tuning; it is a natural consequence of late-time (z_t = 0.5) phase conversion.
6. This result definitively resolves the Lya constraint concern raised in Test 1.
