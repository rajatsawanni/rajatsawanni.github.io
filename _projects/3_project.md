---
layout: page
title: Graph-Based Chemical Reaction Network Analysis
description: A graph-theoretic toolkit for analyzing chemical pathways in reacting flows
img: assets/img/networks_output.png
importance: 1
category: work
related_publications: true
---

### Overview

The **Graph-Based Chemical Reaction Network Analysis Toolkit** is an in-house numerical framework that represents complex chemical mechanisms as **directed graphs**, enabling new insights into reaction topology, dominant pathways, and species influence in combustion environments.

This toolkit was developed to address a central challenge in combustion chemistry:  
large reaction mechanisms contain **hundreds of species and thousands of reactions**, making it difficult to identify which pathways actually govern pollutant formation — especially soot.

By converting chemistry into graph structures, the toolkit allows:

- Extraction of **dominant carbon flux pathways**  
- Identification of **high‑influence species**  
- Visualization of **network evolution across pressure, strain rate, and flame location**  
- Reduction of chemical mechanisms while preserving predictive accuracy  

---

## Methodology

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/networks_output.png" caption="(a) Representation and creation of local reaction chemistry as an element flux graph, highlighting the dominant pathways that carry element flux between two species. (b) The evolution of dominant pathways across flame locations and pressure in soot forming counterflow diffusion flames, (c) The evolution of influence of a specie, measured in terms of total normalized flux transferred through the specie that reach a certain node, (d) Evolution of the soot chemical reaction network topology as it evolves through the soot production zone (from right to left), highlighting the pre-emptive organization of carbon delivery network before carbon flux increases." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

The toolkit constructs:

- **Element flux graphs**  
  Species are nodes; edges carry carbon flux between them.

- **Dominant pathway maps**  
  Extracts the largest flux-carrying path from fuel → soot precursors → soot.

- **Influence metrics**  
  Quantifies how much carbon flux passes through each species.

- **Local network evolution**  
  Tracks how the soot network organizes itself before soot actually forms.

These capabilities reveal hidden structure in chemical mechanisms that traditional sensitivity analysis cannot capture.

---

## Key Scientific Insights

Using this toolkit, several important findings were uncovered:

- **Acetylene** emerge as dominant soot precursors, with influence increasing strongly with pressure.  
- The soot network **pre-organizes itself** before measurable soot appears — a previously unreported phenomenon.  
- Different starting nodes (fuel, intermediates, PAHs) converge to shared pathways, revealing **network-level robustness**.  
- Pressure alters not only soot quantity but also **network topology**, changing how carbon is routed through the mechanism.

These insights were applied to high-pressure counterflow diffusion flames and supplemented1 using experimental soot measurements.

---

## Applications

This toolkit is directly applicable to:

- **Soot formation studies**  
- **Alternative fuel chemistry (SAF, hydrogen blends)**  
- **Mechanism reduction for CFD simulations**  
- **Pollutant formation pathway analysis**  
- **High-pressure combustion environments**

It provides a new paradigm for understanding complex chemistry in reacting flows.

---

## Publications & References

- Sawanni, R., and Gulder, O. L. Effects of pressure on the chemical sooting structure of equi-diffusive counterflow diffusion flame. Proceedings of the Combustion Institute. (accepted)
- Sawanni, R., and Gulder, O. L. (2026). Influence of pressure on the structure and chemistry of soot formation counterflow diffusion flame. Combustion and Flame. 286, 114873.
