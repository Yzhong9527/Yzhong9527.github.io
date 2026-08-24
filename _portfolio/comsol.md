---
title: "Electrothermal Modeling of High-Density Electrode Grids for Transcutaneous Neurostimulation"
order: 2
excerpt: "Finite-element analysis of current distribution and tissue heating in single and small-electrode grid configurations for transcutaneous neurostimulation."
collection: portfolio
permalink: /portfolio/comsol
---

## Overview

This project investigates the electrothermal behavior and safety of high-density-inspired surface electrode configurations for peripheral transcutaneous neurostimulation.

Using coupled electrical–thermal finite-element modeling in COMSOL Multiphysics, I studied how electrode subdivision, active electrode count, total active area, and stimulation parameters influence current distribution, Joule heating, and transient temperature responses in multilayer biological tissue.

The goal was to determine when small-electrode grid configurations can reproduce the thermal behavior of conventional single-electrode stimulation and to identify the geometric and stimulation factors governing electrothermal safety.

---

## Electrothermal Modeling Framework

![Electric potential distribution during high-density neurostimulation](/images/comsol_field_distribution.png)

The computational framework couples electrical conduction with transient bioheat modeling in multilayer biological tissue.

Electrical simulations were used to characterize current-density distributions and Joule heating, which were subsequently incorporated into transient thermal simulations to quantify stimulation-induced temperature rise.

The study compared a conventional single-electrode configuration with HD-inspired grids containing 1–16 active small electrodes.

---

## Parameter-Space Analysis

A systematic parameter sweep was performed across stimulation current, pulse width, and frequency.

For each electrode configuration, 128 stimulation combinations were evaluated to characterize how stimulation settings interact with electrode geometry to determine tissue heating.

![Thermal response under increasing stimulation current](/images/comsol_current_thermal_response.png)

The analysis showed that electrothermal behavior depends not only on stimulation intensity, but also on how the total current is spatially distributed across the active electrode area.

---

## Electrode Geometry and Thermal Behavior

A major focus of the study was separating the effects of electrode subdivision, active electrode count, and total active area.

The simulations revealed distinct electrothermal regimes as the number of active small electrodes increased. Configurations with fewer active electrodes produced stronger current concentration and greater local thermal accumulation, whereas increasing the number of active electrodes progressively distributed the stimulation load over a larger effective area.

The stimulation-side thermal load showed a nonlinear decline with increasing electrode count, with larger grid configurations approaching the thermal behavior of the conventional single-electrode reference.

---

## Control and Numerical Validation

To determine whether these effects were driven primarily by electrode count or total active area, additional area-matched and count-matched control configurations were evaluated.

The computational framework was further assessed using mesh-convergence and numerical robustness analyses to verify that the observed electrothermal trends were not artifacts of spatial discretization or numerical settings.

These controls helped separate geometry-dependent effects and establish the robustness of the simulation results.

---

## Key Findings

- Electrode subdivision strongly influences current concentration and local tissue heating.
- Small grids with limited active area can produce substantially greater stimulation-side thermal accumulation.
- Increasing active electrode count and total active area progressively reduces local thermal load.
- Larger small-electrode grids can approach the electrothermal behavior of conventional single-electrode stimulation.
- Electrothermal safety depends jointly on electrode geometry and stimulation parameters rather than electrode size alone.

---

## Publication

**Yuanshan Zhong & Filip Stefanovic.**  
*Comparative Electrothermal Analysis of Single and Small-Electrode Grid Configurations for HD-Inspired Peripheral Transcutaneous Neurostimulation.*  
**Frontiers in Bioengineering and Biotechnology (2026), Accepted.**

[View article on Frontiers](https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2026.1904885/abstract)

---

## Takeaway

This work establishes a systematic computational framework for evaluating the electrothermal safety of small-electrode grid configurations in transcutaneous neurostimulation. The results show how electrode geometry, active area, and stimulation parameters jointly shape current concentration and tissue heating, providing a physics-based basis for the design of high-density stimulation systems.

## Takeaway

This project demonstrates how finite-element modeling and computational analysis can support the design of safe, scalable, and selective neurostimulation systems for future neuroengineering applications.
