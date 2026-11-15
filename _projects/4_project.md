---
layout: page
title: Monte Carlo Radiative Transfer
description: Checking, and correcting, optical soot measurements in dense high-pressure flames
img: assets/img/cards/radiation.jpg
importance: 2
category: Modeling and analysis tools
related_publications: false
---

## The problem

Measuring soot and temperature with light, through extinction and emission, usually leans on a few simplifications: the soot doesn't reabsorb its own emission (signal trapping), scattered light doesn't reach the camera (in-scattering), and the optics collect light along perfect straight lines with perfect resolution. In dense, high-pressure flames, those assumptions start to break down.

To find out by how much, I wrote a backward Monte Carlo ray-tracing solver. It traces rays from the camera back through the collection optics and the flame, which is treated as a non-homogeneous medium that absorbs, emits and scatters light anisotropically, and adds up what the camera would really see.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/RTE_BMC.png" alt="Optical layout and flowchart of the backward Monte Carlo ray-tracing solver" caption="(a) The optical layout traced by the solver, from the camera sensor through the lenses and the attenuating, emitting flame to the light source. (b) The ray-tracing algorithm." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## What we found

For high-pressure counterflow flames:

- **Light collection matters.** Collecting light over too wide an angle gives errors above 5%, while choosing telecentric or non-telecentric optics makes little difference.
- **In-scattering is significant.** At short wavelengths, the measured extinction ends up close to the absorption alone.
- **Signal trapping is large.** In the most heavily sooting flame it cuts the recovered radiance by more than 50% and makes the flame look about 150 K cooler than it is. I proposed a correction that recovers the true signal, overshooting the temperature by only about 25 K.
- **Resolution matters too.** Finite spatial resolution lowers the peak extinction by up to 23%, and differences in resolution between wavelengths can push the temperature up by about 50 K.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/RTE_output.jpg" alt="Measured and corrected extinction, radiance and temperature for two flames" caption="Effects of finite and wavelength-dependent spatial resolution. (a) and (c): measured effective extinction coefficient and radiance for flames A and B, compared with the actual values. (b) and (d): uncorrected and corrected temperatures for the same flames, compared with the actual temperature." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Paper

- Sawanni, R., and Gülder, Ö. L. (2025). Retrieval of temperature and extinction coefficient from modulated absorption emission technique: Effects of practical light collection, self-absorption, in-scattering, and finite spatial resolution. _Journal of Quantitative Spectroscopy and Radiative Transfer_, 347, 109662. [doi:10.1016/j.jqsrt.2025.109662](https://doi.org/10.1016/j.jqsrt.2025.109662)
