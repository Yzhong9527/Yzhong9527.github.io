---
title: "Hybrid Learning for Closed-Loop Neural Control"
order: 2
excerpt: "Compact EEG representations for robust closed-loop neural control in BCI systems."
collection: portfolio
permalink: /portfolio/closed_loop
---

## Overview

This project investigates how noisy EEG signals can be transformed into stable control states for closed-loop brain–computer interface (BCI) systems.

The work focuses on combining neural representation learning with reinforcement learning to improve robustness and stability in EEG-driven sequential control tasks. The long-term goal is to develop adaptive neural control systems that remain reliable under noisy and variable neural conditions.

---

## Hybrid Closed-Loop Framework

![Hybrid closed-loop neural control framework](/images/closed_loop_framework.png)

*Proposed hybrid framework combining supervised neural decoding, compact latent representations, and reinforcement learning for EEG-driven cursor control.*

The framework integrates EEG feature extraction, latent representation compression, supervised directional decoding, and reinforcement learning-based sequential control into a unified closed-loop pipeline.

A compact low-dimensional neural state representation was designed to improve reinforcement learning stability while preserving task-relevant neural information.

---

## Robustness and Generalization Analysis

![Robustness and OOD generalization results](/images/closed_loop_results_table.png)

*Summary of control performance under in-distribution (ID) and out-of-distribution (OOD) conditions across different control strategies.*

Results showed that compact latent representations significantly improved training stability and robustness compared with high-dimensional hybrid control strategies. The proposed low-dimensional hybrid framework achieved stable performance under noisy EEG conditions and improved generalization behavior in simulated cursor-control environments.

---

## Approach

- Designed an EEG-driven 2D cursor-control framework using the BCI Competition IV-2a dataset.
- Combined supervised neural decoding with reinforcement learning-based sequential decision-making.
- Proposed compact latent neural representations for robust control-state construction.
- Integrated neural embeddings, decoder outputs, and task geometry into a structured low-dimensional state representation.
- Evaluated robustness under noisy and out-of-distribution control conditions.

---

## Current Findings

- Compact latent representations improved reinforcement learning stability and convergence behavior.
- Low-dimensional hybrid state representations improved robustness to noisy EEG conditions.
- Hybrid supervised + reinforcement learning strategies achieved more stable closed-loop control behavior than conventional approaches.
- Ongoing work investigates cross-dataset generalization across multiple BCI datasets and more realistic continuous-control environments.

---

## Takeaway

This project demonstrates that structured and compact neural representations are critical for building stable, robust, and generalizable closed-loop neural control systems for future neuroengineering applications.
