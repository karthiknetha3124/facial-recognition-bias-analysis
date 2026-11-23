# FAIRVISION AI — Research Proposal

## Working title
Evaluating Demographic and Image-Quality Disparities in Pretrained Face-Verification Systems.

## Research question
To what extent do pretrained facial recognition systems exhibit demographic performance disparities under varying image conditions, and can fairness-aware techniques reduce these disparities without significantly compromising overall recognition accuracy?

## Aim
Build a reproducible research pipeline comparing two pretrained face-verification models, measuring subgroup performance differences and testing selected mitigation strategies.

## Objectives
1. Review face-verification benchmarks, demographic evaluation and fairness literature.
2. Select public datasets with suitable identity relationships and documented demographic annotations.
3. Select two pretrained models with verified checkpoint provenance and permitted use.
4. Establish a common evaluation protocol and baseline metrics.
5. Measure subgroup disparities and image-quality effects.
6. Evaluate mitigation against fairness and overall verification performance.
7. Publish reproducible configurations, aggregate results and limitations.

## Working hypotheses
- H1: Verification error rates differ across at least some dataset-defined demographic subsets.
- H2: Image-quality degradation affects verification performance, potentially differently across subsets.
- H3: Threshold selection materially changes subgroup error rates and fairness–accuracy trade-offs.
- H4: At least one pre-specified mitigation reduces a selected disparity measure, while potentially introducing other trade-offs.

These are hypotheses, not pre-claimed findings.

## Research design
A quantitative benchmark-based experimental study. Two pretrained models will be evaluated on the same eligible identity-labelled benchmark protocol. Analyses include overall and subgroup metrics, controlled image-quality perturbations, confidence intervals, sensitivity analysis and mitigation comparisons.

## Scope
- Face verification (same-person versus different-person comparison), not open-set identity search or surveillance.
- Public research datasets only, subject to terms and approvals.
- Dataset-supplied labels only for demographic fairness analysis.
- No inference of race or ethnicity from pixels.
- No claims about emotion, personality, health or other internal traits.
- Webcam and single-image uploads are demonstrations, not population-level evidence.

## Expected contribution
A reproducible comparative evaluation with transparent pair construction, subgroup metrics, image-quality analysis, threshold sensitivity and mitigation trade-offs. The contribution is the experimental design and evidence, not merely a user interface.

## Approval and change control
The researcher reports that university ethics approval is confirmed. Verify that the approved protocol covers each named dataset, image upload, webcam capture, storage, model inference and deployment. Any activity outside the approved scope requires university guidance or amendment before proceeding.
