---
title: "Multimodal Neural Signal Analysis for Auditory Disorders"
order: 1
excerpt: "Around-ear EEG analysis, foundation-model representations, and self-supervised learning for objective biomarker discovery in auditory disorders."
collection: portfolio
permalink: /portfolio/synapse
---

## Overview

This project investigates neural representations and potential objective biomarkers associated with auditory disorders, including tinnitus, hyperacusis, and misophonia, using around-ear EEG and physiological recordings.

The broader SYNAPSE platform integrates around-ear EEG and pupillometry to characterize neural activity and physiological responses during auditory tasks. My work spans conventional EEG analysis, machine learning, EEG foundation models, representation analysis, and the development of transferable representations for wearable EEG.

---

## EEG Analysis and Machine Learning

My initial work focused on establishing an EEG analysis pipeline for characterizing disorder-related neural patterns.

This included signal preprocessing, ERP and spectral feature extraction, cross-channel synchronization analysis, statistical testing, and conventional machine-learning approaches. I also evaluated deep-learning architectures including EEGNet and EEGNex for neural pattern classification and representation learning.

![ERP and neural feature analysis](/images/synapse_erp.png)

These analyses provided a conventional signal-processing and machine-learning baseline for subsequent investigation of pretrained EEG representations.

---

## EEG Foundation-Model Representations

I subsequently investigated whether pretrained EEG foundation models can extract clinically relevant neural information from around-ear EEG.

Using LaBraM as the primary model, I systematically analyzed latent representations across auditory tasks, electrode channels, temporal windows, and embedding dimensions, with additional model comparisons used to evaluate the generality of observed effects.

![SYNAPSE EEG analysis pipeline](/images/synapse_pipeline.png)

Rather than treating decoding performance alone as evidence of a meaningful biomarker, this work examines what information pretrained models actually encode and whether apparent disease-related representations remain robust under controlled validation.

---

## Understanding What the Model Encodes

A major focus of the current work is interpreting the behavior of pretrained EEG representations.

The analysis combines:

- layer-wise representation analysis to trace how disease-related information emerges and transforms through the model;
- frequency, spatial, and temporal decomposition to characterize the structure underlying predictive representations;
- statistical and permutation-based validation;
- controlled analyses across cohorts, temporal windows, channels, and representation components.

This framework is designed to distinguish robust neural structure from representations that may arise from subject-specific, temporal, or other confounding factors.

![Latent representation analysis](/images/synapse_embedding.png)

---

## Around-Ear EEG Pretraining

In parallel, I am developing a self-supervised pretraining framework specifically for around-ear EEG.

Unlike conventional scalp EEG, publicly available around-ear EEG datasets are limited and often use sparse, heterogeneous electrode layouts. This project therefore investigates how multiple public datasets can be harmonized for pretraining and how foundation-model representation learning can be adapted to non-standard wearable electrode configurations.

The long-term goal is to learn transferable around-ear EEG representations that generalize across subjects, datasets, and downstream tasks.

---

## Current Research Directions

- Objective neural biomarker discovery for auditory disorders.
- Interpretation and validation of EEG foundation-model representations.
- Layer-wise and frequency/spatial/temporal analysis of learned neural features.
- Self-supervised pretraining for sparse and heterogeneous around-ear EEG.
- Cross-subject and cross-dataset generalization of wearable EEG representations.

---

## Takeaway

This project has evolved from conventional EEG signal analysis toward a broader investigation of how neural representations are learned, interpreted, and validated in wearable EEG systems. The long-term goal is to develop robust and transferable neural representations that can support objective assessment and future adaptive neurotechnology.
