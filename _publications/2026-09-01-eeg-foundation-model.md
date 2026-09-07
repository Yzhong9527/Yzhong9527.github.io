---
title: >-
  Distinct Auditory-Condition Signatures in Foundation-Model
  Representations of Around-Ear EEG
  (formerly: From Decoding Performance to Interpretation in EEG
  Foundation-Model Representations)
collection: publications
category: inpreparation
permalink: /publication/2026-eeg-foundation-model
excerpt: "Distinct overall-condition, hyperacusis, and hearing-loss signatures identified in around-ear EEG foundation-model representations and evaluated through subject-level inference, robustness testing, and campaign-wide multiplicity control."
date: 2026-09-01
venue: "Manuscript in preparation"
citation: 'Zhong, Y.*, Das, A.*, Rivera Rosario, E., Sun, W., & Xu, W. (2026). "Distinct Auditory-Condition Signatures in Foundation-Model Representations of Around-Ear EEG." <i>Manuscript in preparation</i>. *Co-first authors.'
---

This study investigates whether pretrained EEG foundation-model representations contain reproducible information about overall auditory-condition status and specific clinical labels in sparse around-ear EEG.

Using a fixed cohort of 43 participants, the analysis identified an overall auditory-condition signal in the HLT task during the post-stimulus period. Frozen LaBraM representations achieved a subject-level AUC of **0.869** in the [2,6]-s window, and the result remained significant under a 111-configuration campaign-wide correction.

Within the experimental group, a cross-validated measure of neural differentiation between 3-dB and 40-dB tones distinguished participants with and without hyperacusis (**AUC = 0.864**). Separately, post-stimulus HLT representation blocks contained hearing-loss information at the participant level (**AUC = 0.819**).

The findings were evaluated through subject-level cross-validation, family-wise permutation testing, nuisance residualization, fixed-trial subsampling, demographic and preprocessing controls, phase-randomized inputs, random encoders, negative-control tasks, participant-identity analyses, and independent computational reruns.

Among the representations tested, the principal overall-condition and hyperacusis results were specific to pretrained LaBraM representations. They were not recovered by conventional spectral features, the tested alternative foundation encoders, randomly initialized encoders, or end-to-end models trained from scratch.

**Manuscript in preparation — submission planned for September 2026.**

[View the complete project and validation story](/portfolio/synapse)
