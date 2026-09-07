---
title: "Multimodal Neural Signal Analysis for Auditory Disorders (Ongoing and Continuously Updated)"
order: 1
excerpt: "Around-ear EEG analysis, foundation-model representations, rigorous decoding validation, and self-supervised learning for wearable neurotechnology."
collection: portfolio
permalink: /portfolio/synapse
---

## Overview

This project investigates neural representations and potential objective biomarkers associated with auditory disorders, including tinnitus, hyperacusis, and misophonia, using around-ear EEG and physiological recordings.

The broader SYNAPSE platform integrates around-ear EEG and pupillometry to characterize neural activity and physiological responses during auditory tasks. My work has progressed from conventional EEG signal analysis and machine learning toward EEG foundation models, representation analysis, rigorous validation of neural decoding, and transferable representation learning for wearable EEG.

Across these stages, a central question has increasingly shaped my work:

**When a learned neural representation produces high decoding performance, what evidence is needed to determine what information the model is actually using?**

![Experimental setup, cEEGrid configuration, and auditory paradigms](/images/fig1.png)

---

## EEG Analysis and Machine Learning

My initial work focused on establishing an EEG analysis pipeline for characterizing disorder-related neural patterns.

This included:

- signal preprocessing and quality control;
- ERP and spectral feature extraction;
- cross-channel synchronization analysis;
- statistical testing and conventional machine learning; and
- deep-learning architectures including EEGNet and EEGNeX.

These analyses provided a conventional signal-processing and machine-learning baseline for studying neural responses across auditory tasks and disorder groups.

![ERP and neural feature analysis](/images/synapse_erp.png)

This stage also provided the foundation for asking whether pretrained neural representations could capture information beyond conventional EEG features.

---

## EEG Foundation-Model Representations

I subsequently investigated whether pretrained EEG foundation models could extract clinically relevant information from sparse around-ear EEG.

Using LaBraM as the primary model, I systematically analyzed latent representations across:

- auditory tasks;
- electrode channels;
- temporal windows;
- model layers; and
- embedding dimensions.

Additional model comparisons were used to examine whether observed effects were specific to a particular pretrained architecture.

![SYNAPSE EEG analysis pipeline](/images/synapse_pipeline.png)

Rather than treating decoding performance alone as evidence of a meaningful neural biomarker, this work progressively shifted toward understanding **what information the learned representations actually encode and how robust that information is under controlled validation**.

---

## Representation Analysis

To investigate the structure underlying predictive representations, I analyzed how information was organized and transformed within the pretrained model.

The analysis included:

- layer-wise representation analysis;
- frequency decomposition;
- spatial and channel-level analysis;
- temporal decomposition;
- latent feature and embedding analysis; and
- statistical and permutation-based validation.

These analyses were designed to trace where potentially disease-related information emerged in the model and whether it could be associated with interpretable properties of the underlying EEG signal.

![Latent representation analysis](/images/synapse_embedding.png)

This stage motivated a more systematic investigation of whether apparently strong decoding results remained stable under expanded cohorts, alternative controls, and generalization tests.

---

## From Decoding Performance to Interpretation

Using pretrained LaBraM representations, we initially observed strong subject-level decoding of auditory-disorder status in a strict-QC cohort.

However, when the cohort was expanded and the preprocessing pipeline was revised, the corresponding decoding performance decreased substantially.

Rather than treating the original high performance as sufficient evidence for a stable neural biomarker, I used this discrepancy as the starting point for a systematic investigation of the information underlying the learned representations.

Layer-wise analysis localized the strongest representational transition near the interface between temporal patch embedding and the first transformer block. This observation motivated further investigation of temporal structure and directly measurable EEG features.

![Initial decoding, layer-wise localization, and time-domain feature screening](/images/fig2.png)

---

## Stress-Testing the Interpretation

High decoding performance alone does not establish the physiological source of a learned representation. I therefore developed a battery of controlled analyses targeting alternative explanations for the observed decoding.

The controls examined:

- **decoding floor** using white-noise inputs;
- **subject identity** retained within learned representations;
- **channel handling** and interpolation;
- **temporal displacement** of EEG input;
- **model initialization** using randomly initialized networks; and
- **phase structure** using phase-randomized surrogate signals.

I subsequently re-evaluated these controls across repeated resampling, multiple downstream classifiers, stochastic realizations, and model initializations.

This broader evaluation changed the interpretation of several initially promising results. Temporal displacement primarily affected transfer between representation spaces rather than eliminating decodable information; randomly initialized models could retain substantial decoding ability; and phase-randomized signals preserved part of the original effect.

![Six-control battery and distributional re-evaluation](/images/fig3.png)

These analyses highlighted the importance of evaluating mechanistic controls as **distributions rather than isolated experimental outcomes**.

---

## Subject Identity and Neural Generalization

Because subject identity remained detectable in the foundation-model representations, I further investigated whether the observed disease-related structure could be separated from participant-specific information.

Using linear concept erasure, I removed linearly accessible subject-identity information and evaluated whether the remaining representations generalized across non-overlapping pre-stimulus windows.

I further evaluated generalization:

- across pre-stimulus windows;
- across auditory tasks;
- under fold-wise identity removal; and
- across a second pretrained EEG architecture.

Cross-window transfer remained above the permutation-null mean but did not reach the prespecified significance threshold. Extending the analysis across multiple temporal windows likewise did not establish a statistically supported temporal-generalization structure.

![Identity-controlled temporal and task generalization](/images/fig4.png)

Overall, the evidence did not establish a stable representation that generalized consistently across windows, tasks, and models.

---

## Cohort and Pipeline Sensitivity

The difference between the original and expanded-cohort decoding results raised another question:

**Was the change driven by different participants, changes in the analysis pipeline, or both?**

To investigate this, I compared the original and revised pipelines using the same overlapping participant set and performed repeated paired subsampling analyses.

The results suggested sensitivity to analysis configuration, although uncertainty in the paired comparison prevented attribution of the performance change to a single factor. The original high-performing combined-task representation was also not reproduced by any individual auditory task.

![Cohort and pipeline sensitivity analysis](/images/fig5.png)

Together, these analyses emphasize how cohort composition, preprocessing, model configuration, and analytical choices can influence conclusions drawn from neural decoding.

---

## Current Manuscript

### *From Decoding Performance to Interpretation in EEG Foundation-Model Representations*

**Yuanshan Zhong\***, Anarghya Das\*, Elizabeth Rivera Rosario, Wei Sun, and Wenyao Xu  
\*Co-first authors

**Manuscript in preparation — submission planned for early September 2026.**

This work examines the distinction between **detecting decodable information** and **establishing what that information represents**.

Across selection-aware permutation testing, repeated mechanistic controls, identity removal, temporal and task generalization, cross-model analysis, and cohort sensitivity analysis, the study examines how the interpretation of apparently strong decoding results changes as additional levels of validation are introduced.

---

## Around-Ear EEG Representation Learning

In parallel, I am developing a self-supervised pretraining framework specifically for around-ear EEG.

Unlike conventional scalp EEG, publicly available around-ear EEG datasets are limited and often use sparse, heterogeneous electrode layouts. This project investigates how multiple public datasets can be harmonized for pretraining and how foundation-model representation learning can be adapted to non-standard wearable electrode configurations.

The long-term goal is to learn transferable around-ear EEG representations that generalize across subjects, datasets, and downstream tasks.

---

## Current Research Directions

- Conventional and foundation-model-based EEG analysis.
- Neural representation analysis and interpretation.
- Layer-wise, frequency, spatial, and temporal analysis of learned features.
- Robust validation of neural decoding.
- Subject-specific information and cross-subject generalization.
- Temporal, task, and cross-model generalization.
- Self-supervised learning for sparse and heterogeneous around-ear EEG.
- Cross-subject and cross-dataset representation learning.

---

## Takeaway

This project has progressed from **conventional EEG signal analysis**, through **foundation-model representation learning and interpretation**, toward a broader investigation of **what information supports neural decoding, how robust that information is, and under what conditions it generalizes**.

The experience has also motivated my interest in studying neural representations at finer spatial and physiological scales, including higher-resolution electrophysiological recordings and neural population activity. I am particularly interested in understanding how neural information is represented and transformed across neurons, circuits, and behavior, and how this understanding can ultimately support robust decoding and adaptive closed-loop neural systems.

---

## Latest Results: Building the Evidence Step by Step

The latest study uses a fixed cohort of 43 participants (28 with experimental auditory conditions and 15 controls) and four tasks spanning auditory and visual-control conditions. Rather than presenting the strongest decoding score in isolation, I organized the analysis as a sequence of increasingly demanding questions: **Where is the signal? Does it survive broad statistical correction? Could it be explained by nuisance variables or implementation choices? Does it depend on the pretrained representation? Is the same pattern visible in conventional features or models trained from scratch?**

### 1. Locating the overall auditory-condition signal

The initial 24-configuration family did not yield a result that survived family-wise correction. Expanding the analysis to post-stimulus windows identified a reproducible overall auditory-condition decoding site in the HLT task from **2 to 6 seconds after stimulus onset**. A frozen LaBraM representation with an LDA readout achieved a subject-level AUC of **0.869** (family-wise \(p=0.008\)).

A separate dense temporal scan of 89 configurations localized the strongest short interval to **[4,5] seconds** (AUC = **0.874**, family-wise \(p=0.026\)); the **[3,5]-second** interval also survived correction (AUC = **0.860**, family-wise \(p=0.044\)). Finally, the principal post4/HLT result remained significant in a broader **111-configuration campaign-wide max-T audit** (global \(p=0.022\)). The 89- and 111-configuration analyses were treated as separate statistical families.

### 2. Testing alternative explanations

I then stress-tested the post4/HLT result against potential nuisance and protocol effects:

- **Unequal HLT trial counts:** repeatedly fixing the number of trials produced a median AUC of **0.833**.
- **Age and channel availability:** fold-wise age residualization yielded an AUC of **0.786**, while joint age and usable-channel residualization yielded **0.750**.
- **Sex composition:** the female-only AUC was **0.948**, and a sex-stratified permutation test gave \(p=0.0002\).
- **Filtering choices:** a high-pass-equivalent pipeline yielded an AUC of **0.862**, with participant scores closely matching the reference pipeline (\(r=0.934\)).
- **Phase structure:** phase-randomized surrogate inputs reduced performance to a mean AUC of **0.620**.
- **Pretraining dependence:** randomly initialized LaBraM encoders produced near-chance results (mean AUC = **0.506**, maximum = **0.514**).
- **Task specificity:** no PMT visual-control configuration survived the corresponding post-stimulus family correction.

Component analyses further showed that the overall-condition information was not attributable to a single ear, second, or conventional frequency band. Performance was reduced most strongly when beta or gamma activity was removed, but these ablations were treated as characterization rather than independent significance tests.

### 3. Comparing representations and learning approaches

The same analysis was repeated with alternative representations and learning strategies. The overall-condition effect did **not** reproduce with the tested BIOT families, and targeted tests at the winning site yielded AUCs of **0.612** for CBraMod and **0.467** for SignalJEPA. Thus, the observed effect was **LaBraM-specific among the pretrained encoders tested**, rather than a generic property of every EEG foundation model.

Conventional spectral summaries also did not recover the effect. At post4/HLT, spectral logistic regression achieved an AUC of **0.521**, compared with **0.869** for frozen LaBraM probing; the paired AUC difference was **0.348** (95% CI: **0.183–0.527**). Across 168 univariate spectral tests, none passed Benjamini–Hochberg correction.

End-to-end networks trained from scratch—including EEGNet, ShallowFBCSPNet, Deep4Net, and EEGConformer—reached approximately **0.63** at best under subject-independent evaluation and remained below the frozen LaBraM result. Random trial splits produced inflated estimates and were retained only as a leakage demonstration.

### 4. Separating overall status from condition-specific signatures

The analysis then moved beyond the overall experimental-versus-control contrast. Each participant's trial embeddings were converted into a single cross-validated stimulus-differentiation score, allowing condition effects to be tested without treating trials as independent participants.

For **hyperacusis (HQ)**, differentiation between 3-dB and 40-dB HLT trials during **[0,2] seconds** distinguished HQ-positive from HQ-negative participants within the experimental group (\(n=28\), AUC = **0.864**, absolute \(z=2.84\), six-test family-wise \(p=0.022\)). The result remained stable across independent random-number streams, leave-one-participant-out checks, repeated five-trial subsampling, and an analysis restricted to participants with hearing loss. The same HQ effect was not reproduced with BIOT embeddings.

For **hearing loss (HL)**, five-trial representation blocks from post4/HLT yielded a full-cohort subject-level AUC of **0.819** (12-test family-wise \(p=0.036\)) and an EXP-only AUC of **0.828** (family-wise \(p=0.032\)). Tinnitus and HQ labels did not survive correction in this block-level family. Linear participant identity was explicitly measured and erased as an implementation control, while label-orthogonalized identity removal was used to assess whether label information persisted beyond unrelated subject-specific variation.

### 5. Validating interpretation methods

I also tested whether attribution maps genuinely reflected the trained decision function. Gradient-based maps remained highly similar after model and label randomization, so they did not meet the prespecified validity criterion and were not interpreted mechanistically. Occlusion profiles passed the randomization-similarity check, but no individual channel or one-second segment exceeded the corrected 20-element threshold. The largest temporal change occurred for **[3,4] seconds** (\(\Delta\mathrm{AUC}=0.202\)), below the family-wise threshold of 0.286.

## Current Conclusions

- **Overall auditory-condition status:** the strongest reproducible signal occurred in HLT after stimulus presentation, particularly within **[3,5] seconds** and the broader **[2,6]-second** window.
- **Hyperacusis:** HQ was associated with a within-person intensity-differentiation signature during the **[0,2]-second** tone interval, rather than with a direct high-dimensional HQ classifier.
- **Hearing loss:** HL information was detectable from post-stimulus HLT representation blocks after scores were aggregated to the participant level.
- **Representation dependence:** among the tested approaches, the principal overall-condition and HQ results depended on pretrained LaBraM representations. They were not recovered by conventional spectral features, the tested alternative foundation encoders, randomly initialized encoders, or end-to-end models trained from scratch.
- **Validation:** the principal findings were evaluated with subject-level cross-validation, family-wise and campaign-wide permutation correction, nuisance residualization, protocol-matched subsampling, negative controls, representation randomization, and independent computational reruns.

Together, these results support **distinct representation-level signatures for overall auditory-condition status, hyperacusis-related intensity differentiation, and hearing loss**, while also defining the limits of their current physiological and cross-model interpretation.
