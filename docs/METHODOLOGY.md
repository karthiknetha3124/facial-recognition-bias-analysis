# Experimental Methodology

## Study design
A quantitative paired benchmark evaluation of two pretrained face-verification models. Evaluate both on the same eligible identities, comparison pairs and split wherever technically valid.

## Unit of analysis
A face-image pair with a binary ground-truth relationship:
- Genuine: both images belong to the same dataset identity.
- Impostor: images belong to different dataset identities.

Follow the benchmark's official protocol where available. Pair manifests should use pseudonymous image references and labels, not copied image content or unnecessary personal data.

## Scores and decisions
Each model generates embeddings. A documented similarity function (initially cosine similarity where compatible) produces a comparison score. A threshold converts scores into accept/reject decisions. Verify score direction and normalisation for each implementation.

Select thresholds using a development/validation split and freeze them before final test evaluation. Report threshold-free ROC/AUC alongside threshold-dependent metrics.

## Metrics
- FMR: impostor comparisons incorrectly accepted divided by eligible impostor comparisons.
- FNMR: genuine comparisons incorrectly rejected divided by eligible genuine comparisons.
- TAR: genuine comparisons correctly accepted at a stated threshold.
- EER: operating point where FMR and FNMR are equal or closest.
- ROC/AUC: discrimination across thresholds.
- Disparity: explicitly defined absolute differences or ratios between dataset-defined groups for a named metric.

State threshold and denominator for threshold-dependent metrics.

## Experiments
### E1 — Overall baseline
Evaluate both models on the primary benchmark. Report FMR, FNMR, TAR at predeclared operating points, EER, ROC/AUC and runtime.

### E2 — Subgroup performance
Repeat by dataset-provided demographic subset/label. Report group sample sizes, pair counts, uncertainty intervals and absolute gaps. A disparity alone does not establish its cause.

### E3 — Image-quality sensitivity
Measure available quality indicators and/or apply controlled blur, brightness and resolution perturbations. Preserve traceability to original images and report perturbation strength.

### E4 — Threshold sensitivity
Plot subgroup FMR/FNMR across thresholds. Compare a global threshold with any separately calibrated strategy as a distinct policy experiment. Do not tune on test data.

### E5 — Mitigation
Evaluate pre-specified approaches such as permitted balanced sampling during model adaptation, validation-based threshold calibration or quality-aware evaluation. Distinguish retraining from post-hoc calibration. Do not assume mitigation improves fairness before measurement.

### E6 — Ablation and robustness
Remove one component at a time (for example alignment, quality filtering or mitigation) and examine its contribution. Test sensitivity to pair sampling and random seeds where feasible.

## Statistical analysis
Use confidence intervals for rates and subgroup gaps. Account for dependence when pairs share identities, using identity-aware bootstrap resampling or another justified method. Predefine primary outcomes, report effect sizes and sample sizes, and correct for multiple comparisons where needed.

## Reproducibility record
Each run should save a unique run ID, dataset version, pair-manifest checksum, model/checkpoint checksum, preprocessing configuration, threshold protocol, random seed, package versions, hardware and aggregate metrics. Do not store raw face images in experiment logs.

## Interpretation
A reduction in one disparity metric is not sufficient to establish fairness. Discuss accuracy, error rates, uncertainty, subgroup sample sizes, intersectional limitations, dataset bias and trade-offs. Do not make universal fairness claims from a small number of benchmarks.
