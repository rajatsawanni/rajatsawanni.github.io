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

For my Ph.D. I designed and built a counterflow burner, housed inside a high-pressure chamber at UTIAS, built for stable diffusion flames up to 10 bar. My experiments so far have covered 1 to 6 bar.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/counterflow_facility.jpg" alt="High-pressure chamber housing the counterflow burner, its diagnostics and flames at several pressures" caption="Left: flames at atmospheric and high pressure for different fuel mixtures. Middle: the high-pressure chamber that houses the burner, with the diffuse-light absorption–emission diagnostic in front. Right: a rendering of the burner. Each of the two opposed nozzles has its own central and shroud (coflow) streams and a water-cooling jacket; X-Y and tip-tilt stages align them, a linear actuator sets their separation, and a glow plug on a motorized arm lights the flame remotely." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## Experiments and diagnostics

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/counterflow_schematic_proci2024.png" alt="Schematic of the counterflow burner nozzle and assembly, the flame between the nozzles, and the gas-handling system" caption="(a) One burner nozzle and the full burner assembly. (b) The counterflow flame between the two nozzles, with the gas and particle stagnation planes. (c) The gas-handling system. Figure from Sawanni and Gülder, Proc. Combust. Inst. 40 (2024) 105745 (CC BY-NC-ND 4.0)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>


So far I have mostly used it for soot-forming ethylene flames, changing the strain rate, residence time, pressure and dilution one at a time. It can also run soot formation–oxidation and non-sooting flames, and other fuels such as propane and hydrogen blends.

To measure soot, I developed a diffuse-light modulated absorption–emission imaging technique at several wavelengths, which maps soot concentration, soot maturity and temperature across the flame. An open-source 1D detailed-chemistry solver (OpenSMOKE++) then reproduces the flame chemistry and fills in what the experiments can't measure, with 2D OpenFOAM simulations of the flow setting its inflow conditions.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/counterflow_output.png" alt="Pressure scaling of soot production and the sooting structure of a counterflow flame" caption="(a) Reconciling the pressure scaling of soot formation for flames of different fuel mixtures designed with constant residence time or mass flux. (b) The sooting structure of a counterflow diffusion flame, and how pressure changes the measured soot volume fraction and soot maturity." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## What we found

- I designed two families of flames from 1 to 6 bar, one at constant residence time and one at constant carbon flux. Concentration-based measures of soot give different pressure trends depending on the design, which helps explain why earlier studies disagreed. Normalizing the mean soot production rate by the acetylene and pyrene concentrations gives a soot yield parameter that scales as about _p_<sup>1.7</sup> in every case.
- We measured how both soot volume fraction and soot maturity change with pressure in these flames.
- Pressure also changes the chemistry of soot formation, with acetylene becoming more and more important (more on the [reaction-network page](/projects/3_project/)).

## Papers

- Sawanni, R., and Gülder, Ö. L. (2024). A tractable methodology for assessing the pressure scaling of sooting processes in a counterflow diffusion flame from 1 to 6 bar. _Proceedings of the Combustion Institute_, 40(1-4), 105745. [doi:10.1016/j.proci.2024.105745](https://doi.org/10.1016/j.proci.2024.105745)
- Sawanni, R., and Gülder, Ö. L. (2026). Influence of pressure on the structure and chemistry of counterflow diffusion flames from 1 to 6 bar. _Combustion and Flame_, 286, 114873. [doi:10.1016/j.combustflame.2026.114873](https://doi.org/10.1016/j.combustflame.2026.114873)
- Sawanni, R., and Gülder, Ö. L. (2026). Effects of pressure on the chemical sooting structure of equi-diffusive counterflow diffusion flames. _Proceedings of the Combustion Institute_, 42, 106528. [doi:10.1016/j.proci.2026.106528](https://doi.org/10.1016/j.proci.2026.106528)
