# Test 19: Local Topology Search — Moon, Solar System, and Beyond

## Overview

Systematic assessment of whether closed wormhole handles can be detected locally — on the Moon, in the solar system, or in the galaxy. Tests GRAIL lunar gravity residuals, geodesic deviation for laser interferometry, and ranks 7 detection methods by feasibility.

## The Fundamental Problem

At the UET-predicted handle spacing of ~30 pc (from DM correlation function):
- **Moon**: P(handle inside) = 10⁻³⁵ — essentially zero
- **Solar system (1 AU)**: P(handle inside) = 10⁻²⁰ — still zero
- **Milky Way**: N(handles) ~ 10⁸ — detectable as collective topology

Even if a handle existed locally, a closed throat with radius r_h ~ 0.02 m (Compton wavelength of m_Phi = 10⁻²² eV) produces geodesic deviation that decays as exp(-d/r_h) — identically zero beyond ~1 meter. Only the dark matter condensate around the handle has gravitational reach, and local DM density is ~5×10⁻²² kg/m³.

## Test A: GRAIL Lunar Gravity

GRAIL mapped the Moon's gravity to spherical harmonic degree 1200+ with ~5 km resolution. After subtracting the geological model (topography + mascons + crustal density), residuals are ~15 mGal RMS.

### Signal Size

A DM condensate (local DM density × volume) anchored by a handle:
- r = 1 km: M = 2.2×10⁻¹² kg
- r = 100 km: M = 2.2×10⁻⁶ kg
- Detectable mass at 100 km depth: 6.7×10¹⁶ kg (needs 10²² times more than local DM provides)

**Sensitivity gap: ~10¹⁰.** GRAIL cannot detect handle-anchored DM condensates.

### Power Spectrum Analysis

A handle at depth d produces a gravity signal at harmonic degree l ~ pi R_moon/d:
- 10 km deep → l = 546
- 100 km deep → l = 55
- 1000 km deep → l = 5

Even the most optimistic scenario (1 handle with 10¹⁵ kg at 100 km) produces C_topo/C_geo = 10⁻⁵ at l=54 — far below geological signal.

## Test B: Geodesic Deviation

Metric perturbation from local DM at Earth-Moon distance: δg ~ 10⁻⁴⁸. Path length change: ~10⁻³⁹ m. LISA sensitivity: 10⁻¹² m.

**Sensitivity gap: ~10²⁷.** No current or planned interferometer can detect this.

## Test C: Ranked Detection Methods

| Rank | Method | Feasibility | Gap | When |
|------|--------|-------------|-----|------|
| 1 | Stochastic GW background (LIGO cross-correlation) | POSSIBLE | Unknown | O5+ (2027) |
| 2 | PTA angular correlations (Test 18) | MARGINAL | 2-5x | SKA (2030s) |
| 3 | CMB B-mode topology (LiteBIRD) | MARGINAL | 10-100x | 2030s |
| 4 | GRAIL gravity residuals | No | 10¹⁰ | Never with current physics |
| 5 | Lunar Laser Ranging | No | 10²⁴ | Never |
| 6 | Gaia astrometric wobble | No | 10⁶ | 2040s successor maybe |
| 7 | Quantum gravity interferometry | No | 10²⁰ | No foreseeable technology |

## The Moon's Real Role

The Moon is the wrong TARGET but potentially the right PLATFORM. A lunar GW detector (LGWA or GLOC proposals) operating at 0.1-1 Hz would bridge the gap between LISA (mHz) and LIGO (100 Hz). The handle network stochastic background may peak in this "decihertz gap" where no current instrument operates.

## Verdict

**You cannot find wormhole handles on the Moon.** The probability of a handle existing inside the Moon is 10⁻³⁵. Even if one existed, its gravitational signature (via DM condensate) would be ~10¹⁰ times below GRAIL sensitivity.

The detectable signatures are all GALACTIC-scale, not local: collective topology modifying pulsar timing correlations, stochastic GW background anisotropy, and CMB B-mode patterns. These require galaxy-spanning baselines, not lunar measurements.

## Figures

- **uet_local_topology_search.png** (2x2):
  - Top-left: Synthetic lunar gravity power spectrum with topological contributions
  - Top-right: Sensitivity gap chart for all 7 detection methods
  - Bottom-left: Handle count vs network spacing for Moon, solar system, and galaxy
  - Bottom-right: Summary verdict
