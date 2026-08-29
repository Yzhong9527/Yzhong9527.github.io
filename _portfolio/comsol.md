---
title: "Electrothermal Modeling of High-Density Electrode Grids for Transcutaneous Neurostimulation"
order: 2
excerpt: "Finite-element modeling of current distribution, tissue heating, electrode geometry, and stimulation safety in high-density transcutaneous neurostimulation."
collection: portfolio
permalink: /portfolio/comsol
---

## Overview

This project investigates how electrode geometry and stimulation parameters shape current distribution and tissue heating in high-density-inspired peripheral transcutaneous neurostimulation.

Using coupled electrical–thermal finite-element modeling in COMSOL Multiphysics, I systematically compared a conventional single electrode with small-electrode grids containing 1–16 active electrodes.

The study combines **multiphysics modeling, parameter-space analysis, geometric controls, thermal safety analysis, and numerical validation** to address a central design question:

**How does subdividing a stimulation electrode into multiple smaller electrodes change current concentration and electrothermal behavior?**

![Computational model and representative electrode configurations](/images/Fig01_model_schematic.jpg)

---

## Multiphysics Modeling Framework

The computational model represents transcutaneous stimulation through multilayer biological tissue, including superficial skin, dermis, subcutaneous fat, and muscle.

Electrical conduction was first modeled to characterize spatial current-density distributions and Joule heating. These electrical solutions were then coupled with transient thermal simulations to quantify stimulation-induced temperature rise over time.

A family of small-electrode configurations from **grid1 to grid16** was evaluated and compared with a conventional single-electrode reference, allowing electrode geometry, electrical loading, and thermal response to be analyzed within the same computational framework.

![Representative current-density distributions](/images/Fig03_current_density_maps.jpg)

---

## Electrode Count and Current Concentration

A major focus of the study was determining how current concentration changes as stimulation is distributed across increasing numbers of small electrodes.

Sparse configurations produced strongly concentrated stimulation-side current, whereas increasing the number of active electrodes progressively distributed current over a larger region.

To test whether this trend depended on the definition of peak current density, I compared the raw nodal maximum \(J_{max}\) with percentile-based \(J_{p99}\) measures using both nodal and area-weighted calculations.

Across these metrics, increasing electrode count consistently reduced stimulation-side current concentration.

![Current-density sensitivity to electrode count](/images/Fig_Jp99_robust_metrics.jpg)

---

## Electrothermal Scaling with Electrode Count

The thermal response showed a similarly strong dependence on electrode count.

Under a representative stimulation condition, sparse small-electrode configurations produced substantially greater local heating than the conventional single-electrode reference. Temperature rise decreased rapidly as additional electrodes were activated.

Across the grid1–grid16 series, stimulation-side temperature rise followed a strong nonlinear decline with increasing electrode count. A transition occurred around **8–9 active electrodes**, after which stimulation-side heating approached or fell below the thermal contribution associated with the fixed return electrode.

Grid9 closely reproduced the thermal response of the conventional single-electrode reference under the representative stimulation condition.

![Electrode-count dependence of stimulation-side temperature rise](/images/Fig05_merged.jpg)

---

## Stimulation Parameter Space

Electrothermal behavior was systematically evaluated across stimulation parameters including:

- current amplitude,
- pulse width, and
- stimulation frequency.

For each electrode configuration, a broad parameter sweep was used to examine how stimulation intensity interacts with electrode geometry to determine tissue heating.

Sparse grids showed substantially stronger sensitivity to increasing stimulation load, whereas configurations with larger active electrode counts distributed the load more effectively and exhibited lower local temperature rise.

![Electrothermal response across stimulation parameters](/images/Fig_sweep_combined.jpg)

To further characterize the operating space, I mapped stimulation-side thermal transition boundaries across combinations of current amplitude, pulse width, and frequency.

These boundaries illustrate how the stimulation conditions associated with modeled temperature-rise thresholds shift as electrode geometry changes.

![Stimulation-side thermal transition boundaries](/images/Fig11_transition_boundary.jpg)

---

## Spatial and Temporal Thermal Dynamics

In addition to peak temperature rise, I examined both the spatial distribution and temporal evolution of stimulation-induced heating.

Temperature maps showed that the strongest thermal accumulation remained localized near the stimulation electrode and was concentrated primarily in superficial tissue.

![Representative temperature-rise distributions](/images/Fig07_temperature_maps.jpg)

Transient simulations further showed that stimulation-side heating depended strongly on electrode configuration, while temperature responses near the fixed return electrode were much less sensitive to changes in the stimulation grid.

![Transient temperature response across electrode configurations](/images/Fig06_dT_vs_time.jpg)

---

## Separating Electrode Count from Active Area

Because increasing electrode count in the primary grid series also increases total active electrode area, I designed additional geometric controls to examine whether the observed thermal trends could be explained by active area alone.

Area-matched configurations were constructed to compare different electrode arrangements while controlling total active area.

The results showed that electrode subdivision and spatial distribution can influence stimulation-side heating even when active area is controlled, indicating that electrothermal behavior depends on more than electrode area alone.

Together, these analyses support a joint role for **electrode count, active area, and spatial configuration** in determining local electrothermal loading.

![Area-matched geometric control](/images/Fig_area_matched_control.jpg)

---

## Numerical Validation

I also evaluated whether the observed electrothermal trends were robust to numerical discretization.

Mesh-refinement analysis compared electrical and thermal predictions across multiple COMSOL mesh levels.

Temperature-rise estimates remained highly stable with mesh refinement, while raw peak current density showed greater sensitivity to local spatial discretization. This motivated the use of percentile-based current-density measures alongside raw nodal maxima.

Overall, the mesh analysis supported the numerical robustness of the principal electrothermal trends.

![Mesh-convergence analysis](/images/Fig12_mesh_convergence.jpg)

---

## Key Findings

- Electrode subdivision produces strongly nonlinear changes in current concentration and tissue heating.
- Sparse small-electrode grids can generate substantially greater local electrothermal loading than a conventional single electrode.
- Increasing active electrode count progressively reduces stimulation-side current concentration and temperature rise.
- A transition occurs around **8–9 active electrodes**, after which the fixed return electrode becomes an important thermal constraint.
- Grid9 closely reproduces the representative thermal response of the conventional single-electrode configuration.
- Electrode count, total active area, and spatial configuration jointly influence electrothermal behavior.
- Thermal response depends strongly on the interaction between electrode geometry and stimulation parameters.
- Geometric controls, robust current-density metrics, and mesh-convergence analyses support the main modeling trends.

---

## Publication

### *Comparative Electrothermal Analysis of Single and Small-Electrode Grid Configurations for HD-Inspired Peripheral Transcutaneous Neurostimulation*

**Yuanshan Zhong & Filip Stefanovic**

*Frontiers in Bioengineering and Biotechnology*, 2026.

**Published August 28, 2026.**

DOI: **10.3389/fbioe.2026.1904885**

[View published article](https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2026.1904885/full)

---

## Takeaway

This project demonstrates how **finite-element and multiphysics modeling can be used to systematically investigate the physical design space of a neurostimulation system**, rather than only simulate a single configuration.

By combining electrical-field modeling, transient thermal simulation, parameter sweeps, geometric controls, robust current-density metrics, and numerical validation, I investigated how electrode architecture translates into current concentration and thermal constraints.

More broadly, this work motivates my interest in integrating **computational modeling with neural recording, stimulation, and closed-loop control**, using physics-based models to guide the design and optimization of future neural interfaces.
