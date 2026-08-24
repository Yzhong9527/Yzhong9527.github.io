---
title: "Hybrid Learning for Adaptive Closed-Loop Neural Control"
order: 4
excerpt: "EEG-driven neural control integrating compact representations, supervised decoding, reinforcement learning, and adaptive closed-loop control."
collection: portfolio
permalink: /portfolio/closed_loop
---

## Overview

This project investigates how noisy and variable EEG signals can be translated into stable control states for adaptive brain–computer interface (BCI) systems.

The initial phase develops a proof-of-concept EEG-driven 2D cursor-control environment using the BCI Competition IV-2a dataset. The framework combines supervised neural decoding with reinforcement learning (RL), allowing neural representations, decoder outputs, and task information to jointly guide sequential control.

The broader goal is to extend this framework from fixed proof-of-concept tasks toward adaptive closed-loop neural control, in which neural representations, task states, goals, and control policies continuously evolve through interaction and feedback.

---

## Hybrid Neural Control Framework

![Hybrid closed-loop neural control framework](/images/closed_loop_framework.png)

*Hybrid framework combining supervised neural decoding, compact neural representations, and reinforcement learning for EEG-driven sequential control.*

The framework integrates EEG feature extraction, neural representation construction, supervised directional decoding, and reinforcement learning into a unified control pipeline.

Rather than using the high-dimensional EEG representation directly as the reinforcement-learning state, the system constructs a compact structured control representation combining:

- neural features;
- supervised decoder outputs;
- current control state;
- task geometry.

This representation provides the RL controller with neural information relevant to intended movement while retaining the spatial information required for sequential decision-making.

---

## Compact Neural Control Representations

A central question in this project is how neural information should be represented for downstream control.

High-dimensional EEG representations may preserve more neural information, but they can also introduce noise and instability into reinforcement-learning optimization. The current framework therefore compresses neural information into a structured low-dimensional state before policy learning.

The goal is not simply dimensionality reduction, but the construction of a representation that preserves task-relevant neural information while providing a stable interface between neural decoding and sequential control.

---

## Robustness and Cross-Subject Generalization

![Robustness and OOD generalization results](/images/closed_loop_results_table.png)

*Control performance under in-distribution (ID) and out-of-distribution (OOD) conditions across different neural-control strategies.*

The initial framework was evaluated using strict subject-level ID/OOD splits and EEG perturbation experiments.

Current results indicate that compact neural-control representations can improve:

- reinforcement-learning convergence;
- training stability;
- robustness to noisy EEG inputs;
- cross-subject generalization;
- stability of sequential control behavior.

These experiments suggest that the interface between neural representation and control policy can be as important as the choice of decoder or reinforcement-learning algorithm itself.

---

## From Static Tasks to Dynamic Closed-Loop Control

The current 2D cursor environment provides a controlled proof-of-concept for studying the interaction between neural decoding and sequential decision-making.

The next stage extends this framework toward a more dynamic closed-loop formulation.

Instead of treating the decoded neural state and task goal as effectively fixed inputs to a control episode, the extended framework will investigate systems in which:

- EEG representations are continuously updated over time;
- task states and control goals can change during interaction;
- recent neural and control history can influence the current control state;
- environmental feedback is incorporated into subsequent decisions;
- the control policy adapts to changing neural and task conditions.

Conceptually, the system evolves from a simple mapping of

**EEG → neural state → controller → action**

toward an iterative closed-loop architecture:

**EEG → neural representation → adaptive controller → environment → feedback → updated neural/control state**

This formulation more closely reflects the time-varying nature of real neural-control systems.

---

## Current Research Directions

- Compact representation learning for neural control.
- Hybrid supervised and reinforcement learning for EEG-driven BCI.
- Robustness to neural noise and subject variability.
- Cross-subject and cross-dataset generalization.
- Time-varying neural and task-state representations.
- Feedback-driven policy adaptation.
- Dynamic and continuous-control environments.

---

## Long-Term Direction

The long-term goal is to develop neural control systems that can continuously adapt to variability in neural signals, users, tasks, and environments.

Rather than treating neural decoding and control as separate problems, this project investigates how representation learning, decoding, sequential decision-making, and feedback can be integrated into a unified adaptive closed-loop architecture.
