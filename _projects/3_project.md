---
layout: page
title: Soot Chemistry as a Network
description: Using graph theory to see which reaction pathways actually make soot
img: assets/img/cards/networks.jpg
importance: 1
category: Modeling and analysis tools
related_publications: false
---

## The idea

A detailed combustion mechanism can have hundreds of species and thousands of reactions, which makes it hard to tell which pathways actually lead to soot. So I built an in-house framework that treats the chemistry as a directed graph: species are the nodes, and the carbon flowing between them forms the edges. Once the chemistry is a network, tools from graph theory can pick out the main pathways, measure how influential each species is, and follow how the whole network changes through the flame and with pressure.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/networks_output.png" alt="Carbon-flux graphs and dominant soot-formation pathways across flame location and pressure" caption="(a) Turning local reaction chemistry into an element-flux graph and picking out the main pathways between two species. (b) How the dominant pathways change across the flame and with pressure in soot-forming counterflow flames. (c) The influence of each species, measured by the normalized flux that passes through it. (d) How the network's structure evolves through the soot production zone (right to left): the carbon delivery network organizes itself before the carbon flux rises." class="img-fluid rounded z-depth-1" %}
  </div>
</div>

## How it works

- **Element-flux graphs** are built from the local reaction rates: species are nodes and edges carry carbon flux.
- **Dominant pathways** are the largest flux-carrying routes from the fuel to soot precursors to soot.
- **Influence** measures how much carbon passes through each species on its way to soot.
- **Network evolution** follows how all of this changes from one point in the flame to the next.

## What we found

Applied to high-pressure counterflow flames and checked against the soot measurements:

- Acetylene acts as a hub in the soot-forming network, and its influence grows with pressure.
- As soot forms, the network organizes itself in a percolation-like way: it assembles and strengthens its carbon delivery routes before soot nucleation actually begins.
- Carbon reaches soot through a few hub species, acetylene above all, along many parallel pathways that narrow to a single chain near the peak of soot production.

## Papers

- Sawanni, R., and Gülder, Ö. L. (2026). Effects of pressure on the chemical sooting structure of equi-diffusive counterflow diffusion flames. _Proceedings of the Combustion Institute_, 42, 106528. [doi:10.1016/j.proci.2026.106528](https://doi.org/10.1016/j.proci.2026.106528)
- Sawanni, R., and Gülder, Ö. L. (2026). Influence of pressure on the structure and chemistry of counterflow diffusion flames from 1 to 6 bar. _Combustion and Flame_, 286, 114873. [doi:10.1016/j.combustflame.2026.114873](https://doi.org/10.1016/j.combustflame.2026.114873)
