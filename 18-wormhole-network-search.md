# Test 18: Closed Wormhole Network Search — Topological Signatures in PTA Data

## Overview

Searches for the signature of a distributed network of CLOSED topological handles (not oscillating open throats) in the NANOGrav 15-year pulsar timing angular correlations. This is the corrected search strategy — Test 17 looked for individual sources; this test looks for the network.

## The Key Insight

Closed inflation-era wormhole throats don't oscillate. They don't emit GWs. They just sit as topology. The right observable is not individual source power — it is the ANGULAR CORRELATION of the stochastic GW background, which deviates from the Hellings-Downs (HD) curve if spacetime is multiply connected.

A closed handle network adds a scalar component to the metric perturbation that produces excess correlation at SHORT angular separations between pulsar pairs — specifically at angles theta ~ d_network / D_pulsar, where d_network is the handle spacing.

## Physical Model

### Network Parameters
- Handle spacing: ~30 pc (following DM distribution in local volume)
- Typical PTA pulsar distance: ~1 kpc
- Correlation angle: theta_network = 1.72 degrees
- UET k_{1/2} = 5.1 h/Mpc → lambda_{1/2} = 1.83 Mpc → theta at z=0.3: 0.12 degrees (ell ~ 1547)

### Topological Deviation Model
```
C_total(zeta) = C_HD(zeta) + A_topo × [1 + P_2(cos zeta)] × exp(-zeta/theta_c)
```
where C_HD is the standard Hellings-Downs correlation, A_topo is the topological amplitude (unknown), P_2 is the Legendre polynomial, and theta_c = 1.72 degrees is the network coherence angle.

The scalar (topological) component is concentrated at small angles and decays exponentially beyond the network coherence scale. It adds to HD at zeta < theta_c and is negligible at large angles.

## NANOGrav 15-Year Data

Used approximate angular correlation values extracted from Agazie et al. 2023 Figure 2 (NANOGrav 15-year dataset). 18 angular bins from 5 to 175 degrees.

### Result

The HD-only fit gives chi2 = 4.80 for 18 bins — already an excellent fit. Adding the topological component does NOT improve the fit (Delta chi2 = 0.0). The small-angle bins (zeta < 30 degrees) show the data sitting slightly BELOW HD, not above: mean excess = -0.053 +/- 0.026 (2.0 sigma below HD).

This means the current data shows no evidence for excess small-angle correlation from a handle network. The data is consistent with pure Hellings-Downs (standard GR prediction for an isotropic stochastic GW background).

### Caveats

1. The NANOGrav correlation values used here are approximate (extracted from published figures, not from the actual chain data). The real analysis requires the published posterior samples.

2. The small-angle deficit (data below HD) may be an artifact of the approximate extraction, or may reflect real physics (e.g., pulsar noise modeling effects at small separations).

3. The network model assumes a specific correlation angle (1.72 degrees) which is smaller than the first NANOGrav bin (5 degrees). The data simply cannot resolve the network scale yet.

## Cross-Correlation Prediction

If handles follow the dark matter distribution, then:
- Galaxy overdensity (DESI) has power suppression at k > k_{1/2} = 5.1 h/Mpc
- GW background anisotropy should show the SAME characteristic angular scale
- Cross-correlation: DESI galaxy map x GW anisotropy map at ell ~ 1547

This is currently NOT testable:
- PTA sky maps have ~10 degree resolution (too coarse for 0.1 degree features)
- LIGO stochastic anisotropy has better resolution but lower sensitivity
- Future: LISA (2035) + Euclid will enable this cross-correlation

## Verdict

**No evidence for a closed wormhole network in current PTA data.** The NANOGrav 15-year angular correlations are consistent with the standard Hellings-Downs curve. The network coherence angle (1.72 degrees) is below the resolution of current PTA angular bins.

This is not a null result in the same sense as Test 17 — the data simply cannot yet resolve the angular scale where the network signal would appear. The test is PREMATURE with current instruments, not FAILED.

### Timeline to Decisiveness
- NANOGrav 20yr (2025-26): 40% smaller errors, more pulsar pairs at small angles
- IPTA DR3 (2026-27): combined PTAs, ~2x more pairs
- SKA-era PTAs (2030s): sub-degree angular resolution → definitive test
- LISA + Euclid (2035+): cross-correlation of GW and galaxy maps

## Comparison: Test 17 vs Test 18

| Aspect | Test 17 (LIGO) | Test 18 (PTA) |
|--------|---------------|---------------|
| Target | Open oscillating throats | Closed network topology |
| Observable | Narrowband CW power | Angular correlation deviation |
| Data | LIGO O3b strain (H1+L1) | NANOGrav 15yr correlations |
| Result | Null (all candidates instrumental) | Null (HD consistent, resolution too coarse) |
| Limitation | Sensitivity (need M > 10^16 kg) | Angular resolution (need theta < 2 degrees) |
| Future | Einstein Telescope | SKA PTA |

## Figures

- **uet_network_search.png** (2x2):
  - Top-left: HD curve + topological deviations + NANOGrav 15yr data points
  - Top-right: Small-angle zoom showing where the network signal should appear
  - Bottom-left: Chi2 vs topological amplitude A_topo
  - Bottom-right: Summary verdict
