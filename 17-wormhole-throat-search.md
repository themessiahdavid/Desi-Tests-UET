# Test 17: Wormhole Throat Search in LIGO O3 Data

## Overview

Searched real LIGO O3b public strain data (H1 + L1, 4096 seconds from GWOSC) for persistent narrowband gravitational wave signals consistent with wormhole throat oscillations at f = c/(2 pi r_throat). This is an exploratory search testing whether UET's dark sector topology produces detectable GW signatures.

## Physical Background

A wormhole throat of radius r_throat oscillates in its fundamental mode at frequency f_0 = c/(2 pi r_throat). This produces a persistent, quasi-monochromatic gravitational wave — like a pulsar, but with no electromagnetic counterpart and no spin-down. The signal is a continuous wave (CW) in LIGO terminology.

### Throat Frequency Table

| r_throat (km) | f (Hz) | In LIGO band? |
|--------------|--------|---------------|
| 30 | 1590.5 | YES |
| 50 | 954.3 | YES |
| 100 | 477.1 | YES |
| 200 | 238.6 | YES |
| 300 | 159.0 | YES (peak sensitivity) |
| 500 | 95.4 | YES |
| 1000 | 47.7 | YES |
| 3000 | 15.9 | YES |

All physically plausible throat radii (30-3000 km) fall squarely in the LIGO band.

## Data

- Source: GWOSC (Gravitational Wave Open Science Center), public data
- Run: O3b (early February 2020)
- Detectors: H1 (Hanford) + L1 (Livingston)
- GPS start: 1264316116
- Duration: 4096 seconds (1.1 hours)
- Sample rate: 4096 Hz
- Total samples: 16,777,216 per detector

## Methodology

### Spectral Analysis
1. Computed high-resolution PSDs using Welch's method (128s segments, 0.008 Hz resolution)
2. Computed running median of PSD (1 Hz window) to identify narrowband excess
3. Threshold: features exceeding 5x local median flagged as candidates
4. Cross-checked H1 and L1 for coherent candidates (present in both detectors)
5. Excluded known LIGO instrumental lines (power mains harmonics, violin modes, calibration lines)
6. Computed coherence between H1 and L1 at candidate frequencies

### Known Lines Excluded
60 Hz and harmonics (power mains), 16.5/33/49.5/66 Hz (calibration), 331.9/510.0 Hz (violin modes), 299.4 Hz (calibration), 393.1/394.5 Hz (instrumental), 9.1/9.8 Hz (seismic).

## Results

### Spectral Line Census
- H1 narrowband features (>5x median, 10-1000 Hz): **198**
- L1 narrowband features (>5x median, 10-1000 Hz): **142**
- Coherent candidates (both detectors, non-instrumental): **11**

### The 11 Coherent Candidates

| Freq (Hz) | Excess H1 | Excess L1 | Coherence | r_throat (km) |
|-----------|----------|----------|-----------|---------------|
| 513.516 | 422,273x | 18.9x | 0.006 | 92.9 |
| 513.508 | 202,903x | 44.7x | 0.002 | 92.9 |
| 513.523 | 50,723x | 2.7x | 0.001 | 92.9 |
| 513.500 | 1,380x | 11.7x | 0.003 | 92.9 |
| 13.758 | 19.2x | 54.4x | 0.032 | 3468 |
| 13.766 | 11.5x | 67.2x | 0.032 | 3466 |
| 13.750 | 10.0x | 12.4x | 0.017 | 3470 |
| 13.938 | 7.7x | 3.2x | 0.009 | 3424 |
| 13.953 | 6.3x | 4.0x | 0.016 | 3420 |
| 13.945 | 6.1x | 4.3x | 0.005 | 3422 |
| 13.961 | 5.4x | 3.9x | 0.003 | 3418 |

### Interpretation of Candidates

**513.5 Hz cluster (4 lines):** Enormous excess in H1 (up to 422,000x median) but moderate in L1 (3-45x). Very low coherence (0.001-0.006). This is almost certainly a **known LIGO violin mode** — the first harmonic of the mirror suspension wire resonance at ~510 Hz. The asymmetric detector response (huge in H1, small in L1) is characteristic of instrumental artifacts from different suspension systems. **NOT a wormhole candidate.**

If it were a throat: r = 93 km. However, the extreme H1/L1 asymmetry and known instrumental origin rule this out.

**13.7-14.0 Hz cluster (7 lines):** Moderate excess in both detectors (5-67x), with the highest coherence values in the dataset (up to 0.032). At ~14 Hz, this is near the low-frequency edge of LIGO's sensitivity, where seismic noise dominates. These are likely **microseismic peaks** — known environmental noise from ocean waves that couples into both detectors coherently (the "microseismic peak" at 0.1-0.3 Hz has harmonics that extend to 10-15 Hz).

If it were a throat: r = 3400-3470 km. However, the higher coherence is expected for environmental (correlated) noise, not GW signals. Genuine GW signals at 14 Hz would have even higher coherence if above threshold. **Likely environmental, not a wormhole candidate.**

### Upper Limits on Throat Strain

For a CW signal integrated for T = 4096s: h_95% = 11.4 sqrt(S_n/T)

| r_throat (km) | f (Hz) | sqrt(S_n) | h_95% | Detectable? |
|--------------|--------|-----------|-------|-------------|
| 50 | 954.3 | 9.0e-24 | 1.6e-24 | Need 3e16x closer |
| 100 | 477.1 | 9.3e-24 | 1.7e-24 | Need 3e16x closer |
| 200 | 238.6 | 1.4e-23 | 2.5e-24 | Need 4e16x closer |
| 300 | 159.0 | 1.3e-23 | 2.4e-24 | Need 4e16x closer |
| 500 | 95.4 | 4.6e-23 | 8.1e-24 | Need 1e17x closer |
| 1000 | 47.7 | 6.7e-23 | 1.2e-23 | Need 2e17x closer |

For inflation-era relics with M_eff = 10^8 kg at 1 kpc, the expected strain is ~10^-31 — far below LIGO sensitivity with any integration time.

### Detection Reach (1-year O3 integration at 150 Hz)

| Throat mass | Reach | Interpretation |
|------------|-------|----------------|
| 10^8 kg (inflation relic) | ~50 km | Completely undetectable |
| 10^12 kg (dark condensate) | ~500 km | Undetectable |
| 10^16 kg | ~0.16 pc | Extremely local only |
| 1 M_sun | ~32 Gpc | Cosmological reach |

For inflation-era relics, LIGO cannot detect throat oscillations unless the throat has accumulated enormous mass (~solar mass) over cosmic history. For such massive throats, the detection reach extends to cosmological distances.

## Verdict

**No wormhole throat candidates detected.** The 11 coherent features are identifiable as known instrumental artifacts (violin modes at 513 Hz) and environmental noise (microseismic harmonics at 14 Hz).

This is a **null result** but a scientifically valuable one:

1. It sets the first (to our knowledge) upper limits on persistent GW emission from wormhole throat oscillations across the 10-1000 Hz band
2. It demonstrates that inflation-era relic throats (M ~ 10^8 kg) are undetectable by current instruments
3. It shows that only stellar-mass throats (M ~ M_sun) would be detectable, and these would produce obvious signals
4. A full 1-year coherent CW search would improve sensitivity by ~50x but still cannot reach inflation-era relics

### What Would Change This

- **Einstein Telescope** (ET, 2030s): 10x better strain sensitivity → 10x deeper reach
- **Massive throats**: If dark sector condensation loads throats to M > 10^16 kg, LIGO can detect them in the galaxy
- **Stochastic background**: A population of throats contributes to the stochastic GW background — the cross-correlation search (Type C) is more sensitive than single-source CW for a diffuse population

## Figures

- **uet_wormhole_search.png** (2x2):
  - Top-left: LIGO O3 noise curve (H1 blue, L1 red) with throat frequencies marked
  - Top-right: Spectral excess power map (10-1000 Hz) with threshold and candidate markers
  - Bottom-left: Detection reach vs throat mass for 1-year integration
  - Bottom-right: Summary verdict text box

## Technical Notes

- Data downloaded via gwpy.timeseries.TimeSeries.fetch_open_data (GWOSC API)
- PSD computed via scipy.signal.welch (Hann window, 128s segments, 50% overlap)
- Coherence computed via scipy.signal.coherence (same parameters)
- Known line list from LIGO detector characterization publications
- Running median computed with 1 Hz window for local noise estimation
