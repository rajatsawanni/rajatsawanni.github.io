---
layout: page
title: High-Pressure Counterflow Flames
description: A burner for finding out how pressure changes soot formation
img: assets/img/cards/counterflow.jpg
importance: 2
category: Facilities and experiments
related_publications: false
---

## Why high pressure?

Engines run at high pressure, and soot forms very differently there than in a flame on a lab bench. Yet earlier studies didn't agree on how fast soot production grows with pressure, partly because the flames' residence time and carbon flux changed along with the pressure.

For my Ph.D. I designed and built a counterflow burner, housed inside a high-pressure chamber at UTIAS, that holds stable, symmetric diffusion flames up to 10 bar.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/counterflow_facility.jpg" alt="High-pressure chamber housing the counterflow burner, its diagnostics and flames at several pressures" caption="Left: flames at atmospheric and high pressure for different fuel mixtures. Middle: the high-pressure chamber that houses the burner, with the diffuse-light absorption–emission diagnostic in front. Right: a rendering of the burner. Each of the two opposed nozzles has its own central and coflow streams and a water-cooled shroud; X-Y and tip-tilt stages align them, a linear actuator sets their separation, and a glow plug on a motorized arm lights the flame remotely." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Experiments and diagnostics

The burner runs soot-forming flames, soot formation–oxidation flames and non-sooting flames, and lets us change the fuel (ethylene, propane, hydrogen blends), strain rate, residence time, pressure and oxidizer one at a time.

To measure soot, I developed a diffuse-light modulated absorption–emission imaging technique at several wavelengths, which maps soot concentration, soot maturity and temperature across the flame. Open-source 1D and 2D detailed-chemistry flame solvers then reproduce the flow and chemistry and fill in what the experiments can't measure.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/counterflow_output.png" alt="Pressure scaling of soot production and the sooting structure of a counterflow flame" caption="(a) Reconciling the pressure scaling of soot formation for flames of different fuel mixtures designed with constant residence time or mass flux. (b) The sooting structure of a counterflow diffusion flame, and how pressure changes the measured soot volume fraction and soot maturity." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## What we found

- With flames designed at constant residence time and carbon flux from 1 to 6 bar, concentration-based measures of soot turn out to be misleading, while soot production rates collapse onto a single soot yield parameter that scales roughly as _p_<sup>1.7</sup>. This helps explain why earlier studies disagreed.
- We measured how both soot volume fraction and soot maturity change with pressure in these flames.
- Pressure also changes the chemistry of soot formation, with acetylene becoming more and more important (more on the [reaction-network page](/projects/3_project/)).

## Papers

- Sawanni, R., and Gülder, Ö. L. (2024). A tractable methodology for assessing the pressure scaling of sooting processes in a counterflow diffusion flame from 1 to 6 bar. _Proceedings of the Combustion Institute_, 40(1-4), 105745. [doi:10.1016/j.proci.2024.105745](https://doi.org/10.1016/j.proci.2024.105745)
- Sawanni, R., and Gülder, Ö. L. (2026). Influence of pressure on the structure and chemistry of counterflow diffusion flames from 1 to 6 bar. _Combustion and Flame_, 286, 114873. [doi:10.1016/j.combustflame.2026.114873](https://doi.org/10.1016/j.combustflame.2026.114873)
- Sawanni, R., and Gülder, Ö. L. (2026). Effects of pressure on the chemical sooting structure of equi-diffusive counterflow diffusion flames. _Proceedings of the Combustion Institute_, 42, 106528. [doi:10.1016/j.proci.2026.106528](https://doi.org/10.1016/j.proci.2026.106528)
