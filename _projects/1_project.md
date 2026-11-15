---
layout: page
title: Contrails in a Lab
description: Recreating how contrails form behind a jet engine, in a wind tunnel at cruise-like conditions
img: assets/img/cards/contrails.jpg
importance: 1
category: Facilities and experiments
related_publications: false
---

## Why contrails?

The white trails behind aircraft can spread into cirrus clouds that trap heat, and they are one of the largest and most uncertain parts of aviation's climate impact. They are also hard to study. In flight you can't control anything, and in simulations the physics of ice forming on soot in a turbulent jet is still uncertain.

So we decided to make contrails in the lab. At UTIAS, in a project with Pratt & Whitney Canada and NSERC, we co-designed and built a facility that mixes a hot, humid exhaust jet with a cold, low-pressure flow, roughly the conditions at cruise altitude, and lets us watch contrails form through large optical windows. In our first experiments the exhaust left the nozzle at about 560 K into ambient air at about 190 K and 0.2 bar.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/contrail_facility.jpg" alt="Contrail tunnel with its instrumentation, soot generator and model combustors" caption="The contrail facility. Left: the inverted coflow soot generator and the model combustors that produce the exhaust. Middle: the tunnel and its diagnostics in the lab. Right: a rendering of the tunnel, with the central exhaust jet, the bypass tube and the ambient flow. Three windows give a clear view of the contrail as it forms, and the fourth wall carries temperature, pressure and humidity sensors and sampling probes." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## What we can do with it

The exhaust can come from an inverted coflow soot generator or from model gas-turbine combustors burning Jet-A1, sustainable aviation fuels or hydrogen, and the bypass flow can be run mixed or unmixed. That lets us change one thing at a time (the fuel, the amount of soot, the water vapor) and see what it does to the contrail.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="lazy" path="assets/img/contrail_schematic_proci2026.png" alt="Schematic of the contrail experiment: soot generator, heated core flow, tunnel, laser sheet, camera and sampling system" caption="How an experiment runs: exhaust from the soot generator is heated and fed through the core nozzle into the cold, low-pressure ambient flow. A laser sheet and a polarization-resolved camera image the contrail, and sampling lines take the soot to electron microscopy and a mobility sizer. Figure from Roy, Sawanni et al., Proc. Combust. Inst. 42 (2026) 106485 (CC BY-NC-ND 4.0)." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

So far we have imaged the contrails with 2D elastic light scattering and Stokes polarimetry, and characterized the soot with mobility sizing and electron microscopy. The facility also integrates laser-induced incandescence, multi-angle light scattering, shadowgraphy and diffraction-based particle sizing, and a wavelength-modulated laser absorption (TDLAS) sensor for water vapor is being developed. Turning scattering images into ice number and size is not yet possible, so we pair the measurements with simulations to see where in the jet the air becomes supersaturated.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/contrail_output.png" alt="Laboratory contrail images and comparisons of measured and predicted scattering intensities" caption="(a) Snapshots of laboratory contrails, imaged by elastic light scattering: soot scatters weakly and ice strongly. (b) Measured mean scattering intensities compared with simulations for ethylene exhausts at different equivalence ratios. (c) The probability of finding ice along the mixing lines of different exhausts, which is controlled by the local supersaturation. (d) Mean scattering intensities of contrails from ethylene and propane exhausts with different amounts of water vapor and soot." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## What we have found so far

- Local supersaturation, set by how the exhaust mixes with the cold air, controls whether ice forms at all, while the size of the ice crystals depends on how many soot particles there are.
- Contrails get brighter with more water vapor much more than they do with more soot.
- Ethylene and propane exhausts carry different amounts of soot and water vapor and give noticeably different contrails, and the ice in propane contrails also looked more irregular in shape.
- These are among the first laboratory measurements of how contrails start, made under known and controlled conditions, and our colleagues are using them to test simulations of contrail formation.

## Papers

- Roy, A.\*, Sawanni, R.\*, Rajan, Y. T., Jahncke, I., Taddesse, T., Groth, C. P. T., Chaudhuri, S., Gülder, Ö. L. (2026). Effects of fuel and soot concentrations on the inception and development of contrails. _Proceedings of the Combustion Institute_, 42, 106485. [doi:10.1016/j.proci.2026.106485](https://doi.org/10.1016/j.proci.2026.106485)
- Jahncke, I., Chelem Mayigue, C., Taddesse, T., Groth, C. P. T., Roy, A., Sawanni, R., Rajan, Y. T., Chaudhuri, S., Gülder, Ö. L. (2026). FANS-based predictions of jet-regime contrail formation using a two-equation soot/ice aerosol transport model. _AIAA SciTech 2026 Forum_, 2026-1021. [doi:10.2514/6.2026-1021](https://doi.org/10.2514/6.2026-1021)
- Chelem Mayigue, C., Jahncke, I., Taddesse, T., Groth, C. P. T., Roy, A., Sawanni, R., Rajan, Y. T., Chaudhuri, S., Gülder, Ö. L. (2025). Contrail formation simulation via FANS-based turbulence modelling combined with two-equation soot/ice particle transport modelling. _AIAA SciTech 2025 Forum_, 2025-0600. [doi:10.2514/6.2025-0600](https://doi.org/10.2514/6.2025-0600)

\* equal contributions
