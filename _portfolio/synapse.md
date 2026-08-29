---
title: "Multimodal Neural Signal Analysis for Auditory Disorders"
order: 1
excerpt: "Around-ear EEG, foundation-model representations, rigorous decoding validation, and self-supervised learning for wearable neurotechnology."
collection: portfolio
permalink: /portfolio/synapse
---

## Overview

This project investigates neural representations associated with auditory disorders using around-ear EEG and physiological recordings.

The broader SYNAPSE platform integrates around-ear EEG and pupillometry during auditory paradigms involving hearing loudness, listening effort, and aversive sounds. My work has progressed from conventional EEG analysis and machine learning toward EEG foundation models, representation analysis, rigorous validation of neural decoding, and transferable representation learning for wearable EEG.

A central question emerging from this work is:

**When a learned neural representation produces high decoding performance, what evidence is needed to determine what information the model is actually using?**

![Experimental setup, cEEGrid configuration, and auditory paradigms](/images/fig1.png)

---

## From Decoding Performance to Representation Analysis

Using pretrained LaBraM representations extracted from around-ear EEG, we initially observed strong subject-level decoding of auditory-disorder status in a strict-QC cohort.

However, when the cohort was expanded and the preprocessing pipeline was revised, the corresponding decoding performance decreased substantially. Rather than treating the original high performance as sufficient evidence for a stable neural biomarker, I used this discrepancy as the starting point for a systematic investigation of the information underlying the learned representations.

I examined:

- pre-stimulus and stimulus-containing neural representations;
- layer-wise changes across the foundation-model hierarchy;
- temporal properties of the underlying EEG signal;
- feature-selection effects on statistical significance; and
- the stability of candidate representations under controlled validation.

Layer-wise analysis localized the strongest representational transition near the interface between temporal patch embedding and the first transformer block, motivating further investigation of temporal structure and directly measurable EEG features.

![Initial decoding, layer-wise localization, and time-domain feature screening](/images/fig2.png)

---

## Stress-Testing the Interpretation

High decoding performance alone does not establish the physiological source of a learned representation. I therefore developed a battery of controlled analyses targeting alternative explanations for the observed decoding.

These controls examined:

- **decoding floor** using white-noise inputs;
- **subject identity** retained within learned representations;
- **channel handling** and interpolation;
- **temporal displacement** of the EEG input;
- **model initialization** using randomly initialized networks; and
- **phase structure** using phase-randomized surrogate signals.

I subsequently re-evaluated these controls across repeated resampling, multiple downstream classifiers, stochastic realizations, and model initializations.

This broader evaluation changed the interpretation of several initially promising results. Temporal displacement primarily affected transfer between representation spaces rather than eliminating decodable information; randomly initialized models could retain substantial decoding ability; and phase-randomized signals preserved part of the original effect.

These analyses highlighted the importance of evaluating mechanistic controls as distributions rather than relying on individual control runs.

![Six-control battery and distributional re-evaluation](/images/fig3.png)

---

## Subject Identity and Neural Generalization

Because subject identity remained detectable in the foundation-model representations, I further investigated whether the observed disease-related structure could be separated from participant-specific information.

Using linear concept erasure, I removed linearly accessible subject-identity information and evaluated whether the remaining representations generalized across non-overlapping pre-stimulus windows.

Cross-window transfer remained above the permutation-null mean but did not reach the prespecified significance threshold. Extending the analysis across multiple temporal windows likewise did not identify a statistically supported temporal-generalization structure.

I further evaluated generalization:

- across pre-stimulus windows;
- across auditory tasks;
- under fold-wise identity removal; and
- across a second pretrained EEG architecture.

Overall, the evidence did not establish a stable representation that generalized consistently across windows, tasks, and models.

![Identity-controlled temporal and task generalization](/images/fig4.png)

---

## Cohort and Pipeline Sensitivity

The difference between the original and expanded-cohort decoding results raised an additional question: **was the change driven by different participants, changes in the analysis pipeline, or both?**

To investigate this, I compared the original and revised pipelines using the same overlapping participant set and performed repeated paired subsampling analyses.

The results suggested sensitivity to analysis configuration, although uncertainty in the paired comparison prevented attribution of the performance change to a single factor. The original high-performing combined-task representation was also not reproduced by any individual auditory task.

Together, these analyses emphasize how cohort composition, preprocessing, model configuration, and analytical choices can influence conclusions drawn from neural decoding.

![Cohort and pipeline sensitivity analysis](/images/fig5.png)

---

## Current Manuscript

### *From Decoding Performance to Interpretation in EEG Foundation-Model Representations*

**Yuanshan Zhong\***, Anarghya Das\*, Elizabeth Rivera Rosario, Wei Sun, and Wenyao Xu  
\*Co-first authors

**Manuscript in preparation — submission planned for early September 2026.**

This work examines the distinction between **detecting decodable information** and **establishing what that information represents**. Across selection-aware permutation testing, repeated mechanistic controls, identity removal, temporal and task generalization, cross-model analysis, and cohort sensitivity analysis, the study examines how the interpretation of apparently strong decoding results changes as additional levels of validation are introduced.

---

## Around-Ear EEG Representation Learning

In parallel, I am developing a self-supervised pretraining framework specifically for around-ear EEG.

Existing EEG foundation models are primarily pretrained on conventional scalp EEG, whereas wearable around-ear datasets use sparse and heterogeneous electrode layouts. I am investigating how multiple public datasets can be harmonized for pretraining and how foundation-model representation learning can be adapted to non-standard wearable electrode configurations.

The long-term goal is to learn transferable around-ear EEG representations that generalize across subjects, datasets, and downstream tasks.

---

## Current Research Directions

- EEG foundation models and neural representation analysis.
- Robust validation and interpretation of neural decoding.
- Subject-specific information and cross-subject generalization.
- Temporal, task, and cross-model generalization.
- Self-supervised representation learning for wearable EEG.
- Neural signal modeling across recording scales.

---

## Takeaway

This project has evolved from asking **whether neural information can be decoded** to asking **what information supports that decoding, how robust it is, and under what conditions it generalizes**.

More broadly, this experience motivates my interest in studying neural representations at finer spatial and physiological scales, including higher-resolution electrophysiological recordings and neural population activity. I am particularly interested in understanding how neural information is represented and transformed across neurons, circuits, and behavior, and how this understanding can ultimately support robust decoding and adaptive closed-loop neural systems.
## Takeaway

This project has evolved from conventional EEG signal analysis toward a broader investigation of how neural representations are learned, interpreted, and validated in wearable EEG systems. The long-term goal is to develop robust and transferable neural representations that can support objective assessment and future adaptive neurotechnology.
