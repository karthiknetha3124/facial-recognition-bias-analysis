# FAIRVISION AI

**Facial Recognition Fairness Evaluation Platform**

A research-focused, reproducible platform for evaluating demographic and image-quality disparities in pretrained face-verification systems. FAIRVISION AI is an MSc dissertation project, not an identity-surveillance or production access-control product.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Research](https://img.shields.io/badge/Focus-Fairness%20Research-purple)
![Compute](https://img.shields.io/badge/Compute-CPU%20first-green)
![Status](https://img.shields.io/badge/Status-Phase%201%20Foundation-orange)

## Research question
To what extent do pretrained facial recognition systems exhibit demographic performance disparities under varying image conditions, and can fairness-aware techniques reduce these disparities without significantly compromising overall recognition accuracy?

## Objectives
1. Establish reproducible baseline verification performance for two pretrained models.
2. Measure false-match and false-non-match disparities across appropriately labelled benchmark groups.
3. Investigate image-quality effects, including blur, brightness, resolution and pose-related variation.
4. Evaluate threshold sensitivity and selected fairness-mitigation approaches.
5. Quantify fairness–accuracy trade-offs with uncertainty estimates and statistical tests.

## Scope and safeguards
- Demographic attributes come from dataset-provided annotations or documented research labels; the app will not infer race or ethnicity from pixels.
- The app will not claim to infer internal emotional states.
- Face comparisons are experimental verification demonstrations, not proof of identity.
- Webcam and individual uploads are transient demonstrations, not a face database.
- Public datasets and pretrained weights are used only after access terms, licences and research restrictions are documented.
- The researcher reports university ethics approval as confirmed. The approved protocol's scope remains controlling; changes to data, capture, storage or processing must be checked with the university.

## Technical direction

| Layer | Initial choice |
|---|---|
| Runtime | Python 3.11 |
| Face detection | OpenCV YuNet |
| Recognition model A | OpenCV SFace |
| Recognition model B | ArcFace-family candidate; exact checkpoint subject to licence verification |
| Image processing | OpenCV, NumPy |
| Evaluation | pandas, SciPy, scikit-learn |
| Fairness | Fairlearn and custom verification metrics |
| Interface | Streamlit |
| Visualisation | Plotly |
| Tests | pytest |
| Deployment target | Streamlit Community Cloud, lightweight demo |

## Planned application
Overview · Image Lab · Dataset Explorer · Recognition Lab · Fairness Lab · Mitigation Lab · Research Reports.

## Roadmap
1. Research foundation
2. Dataset engineering
3. Two-model recognition engine
4. Verification and fairness evaluation
5. Mitigation experiments
6. Research application
7. Validation and deployment
8. Dissertation and portfolio documentation

## Documentation
- [Research proposal](docs/RESEARCH_PROPOSAL.md)
- [Literature review plan](docs/LITERATURE_REVIEW.md)
- [Dataset assessment](docs/DATASET_ASSESSMENT.md)
- [Model selection](docs/MODEL_SELECTION.md)
- [Experimental methodology](docs/METHODOLOGY.md)
- [Ethics and privacy](docs/ETHICS_AND_PRIVACY.md)
- [System architecture](docs/ARCHITECTURE.md)

## Reproducibility
Each experiment should record dataset version and source, annotation provenance, model/checkpoint identifier and checksum, preprocessing configuration, pair-generation seed, similarity metric, threshold-selection protocol, software versions and outputs. Aggregate results must be traceable to a run configuration.

## Limitations
Results are benchmark- and protocol-dependent. Dataset demographic categories may not represent identity or lived experience. Dataset composition, annotation quality and image conditions affect conclusions. A mitigation may improve one metric while worsening another. The project will report trade-offs and avoid universal fairness claims.

## Academic use
This repository is for supervised academic research and learning. It is not designed for legal, employment, education, housing, policing, medical or other high-impact decisions.

---
**Project status:** Phase 1 foundation. No benchmark results are claimed.
