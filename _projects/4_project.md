---
layout: page
title: Backward Monte‑Carlo Ray Tracing for Radiative Transfer
description: A statistical photon-tracking solver for accurate radiative transfer in harsh combustion environments
img: assets/img/RTE_BMC.png
importance: 1
category: work
related_publications: true
---

### Overview

The **Backward Monte‑Carlo Ray‑Tracing Radiative Transfer Solver** is a custom numerical tool developed to solve the full **Radiative Transfer Equation (RTE)** in complex, high‑pressure, soot‑laden combustion environments.

Traditional optical diagnostics (extinction, emission, two‑color pyrometry) often fail in high‑pressure flames because:

- Soot clouds become **optically thick**  
- **Self‑absorption** distorts measured signals  
- **Multiple scattering** alters apparent temperature and soot volume fraction  
- Line‑of‑sight measurements cannot recover local fields  

This solver overcomes these limitations by statistically tracing **virtual photons backward** from the detector through the flame, accounting for:

- Absorption  
- Emission  
- In‑scattering  
- Multi‑particle interactions  
- Spatially varying soot properties  

It provides corrected, physically accurate estimates of **true flame temperature** and **soot volume fraction**, even in harsh optical environments.

---

## Methodology

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/RTE_BMC.png" caption="Monte Carlo Ray Tracing methodology implemented for solving the RTE for an axisymmetric counterflow diffusion flame" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

The solver uses:

- **Backward photon tracking**  
  Photons are launched from the detector and traced through the flame volume.

- **Stochastic sampling of optical paths**  
  Each photon interacts with soot particles according to local absorption/emission coefficients.

- **Full RTE solution**  
  Incorporates absorption, emission, and scattering without simplifying assumptions.

- **Correction of raw optical signals**  
  Converts measured line‑of‑sight intensities into local temperature and soot fields.

This method is particularly effective in **high‑pressure counterflow diffusion flames**, where optical thickness makes conventional diagnostics unreliable.

---

## Key Scientific Contributions

Using this solver, several important findings were achieved:

- Raw optical measurements **significantly underestimate** true flame temperature in optically thick regions.  
- Soot volume fraction retrieved from extinction/emission alone can be **off by more than an order of magnitude**.  
- Multi‑particle in‑scattering plays a major role at pressures above 4–5 bar.  
- Corrected fields reveal **true chemical and thermal structure** of high‑pressure flames.  
- The solver enables validation of soot models under engine‑relevant conditions.

These results were published in the **Journal of Quantitative Spectroscopy and Radiative Transfer (2025)**.
<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/RTE_output.jpg" caption="Effects of finite and disparate spatial resolution: (a) and (c) show the measured effective extinction coefficient and radiance for flame case A and B, respectively, compared to their actual values; (b) and (d) illustrate the uncorrected and corrected temperatures for flame cases A and B, respectively, compared to the actual temperature." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
---

## Applications

This solver is directly applicable to:

- **High‑pressure combustion diagnostics**  
- **Soot‑laden flames with strong self‑absorption**  
- **Validation of optical diagnostics (MAE, LII, emission)**  
- **CFD model validation**  
- **Alternative fuel studies (SAF, hydrogen blends)**  

It provides a robust numerical foundation for interpreting optical measurements in extreme environments.

---

## Publications & References

Sawanni, R., Güllder, Ö. L. (2025). Retrieval of temperature and extinction coefficient from modulated absorption emission technique: Effects of practical light collection, self-absorption, in-scattering, and finite spatial resolution. Journal of Quantitative Spectroscopy and Radiative Transfer, 347, 109662.
