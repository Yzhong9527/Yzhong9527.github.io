---
title: "Multimodal Neural Signal Analysis for Auditory Disorders"
order: 1
excerpt: "Wearable ear-EEG analysis and representation learning for objective biomarker discovery in sound sensitivity disorders."
collection: portfolio
permalink: /portfolio/synapse
---

## Overview

This project investigates objective neural biomarkers for sound sensitivity disorders, including tinnitus, hyperacusis, and misophonia, using wearable ear-EEG and physiological recordings.

The broader SYNAPSE system combines ear-EEG and pupillometry to measure neural activity and physiological arousal during auditory tasks. My work focuses on EEG signal analysis, neural representation learning, and subject-level biomarker discovery.

---

## Research Pipeline

![SYNAPSE EEG analysis pipeline](/images/synapse_pipeline.png)

The analysis pipeline includes EEG preprocessing, task-aligned feature extraction, neural representation learning, embedding analysis, and cross-subject validation.

---

## My Contributions

- Extracted EEG features including ERP components, spectral power, and cross-channel synchronization.
- Built neural representation learning pipelines using EEGNex and LaBraM.
- Analyzed learned embeddings using PCA and UMAP to identify interpretable latent structures.
- Compared neural representations with clinical questionnaire data and subject-level response patterns.
- Evaluated cross-subject generalization using leave-one-subject-out classification and label-shuffle validation.

---

## Representative Results

![Latent representation analysis](/images/synapse_embedding.png)

The learned EEG representations revealed subject-level latent structures related to disease-relevant patterns and trial variability.

![ERP and neural feature analysis](/images/synapse_erp.png)

ERP and spectral analyses were used to examine task-related neural responses and support the interpretation of learned representations.

---

## Key Findings

- Identified latent components associated with disease-related neural patterns and trial variability.
- Achieved approximately 0.81 AUC in cross-subject disorder-related classification.
- Found that robust wearable EEG representations may support objective assessment of auditory disorders.

---

## Takeaway

This project shows that stable neural representations can be extracted from noisy wearable ear-EEG and linked to clinically meaningful auditory disorder patterns. It also motivates future work on multimodal neurotechnology and closed-loop rehabilitation systems.
