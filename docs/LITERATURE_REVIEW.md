# Literature Review Plan

## Purpose
Establish the scholarly foundation for face-verification disparities and mitigation. Distinguish demographic performance evaluation, dataset representation, image-quality effects, threshold policy and algorithmic mitigation.

## Core strands
1. Face verification: detection, alignment, embeddings, genuine/impostor protocols, ROC curves and operating thresholds.
2. Demographic evaluation: NIST demographic-effects work, Racial Faces in the Wild (RFW), annotation provenance and category limitations.
3. Image quality: illumination, blur, pose, occlusion, resolution, face size and their interaction with subgroup performance.
4. Fairness: group-wise FMR, FNMR and TAR; threshold calibration; sampling; representation learning; fairness–accuracy trade-offs.
5. Governance: biometric privacy, consent, data minimisation, retention, dataset licensing and intended-use restrictions.

## Initial sources to verify and cite
- NIST Face Recognition Technology Evaluation (FRTE), demographic effects: https://pages.nist.gov/frvt/html/frvt_demographics.html
- RFW original paper and official dataset documentation: locate and cite primary sources.
- FairFace paper and official repository: https://github.com/joojs/fairface
- OpenCV face recognition and SFace documentation: https://docs.opencv.org/
- Fairlearn documentation: https://fairlearn.org/
- Original papers for the exact second recognition model and selected mitigation methods.

## Review protocol
For every source record full citation, year, research question, dataset, model, protocol, metrics, findings, limitations and relevance. Prefer original papers, official benchmark documentation and standards-body reports. Confirm bibliographic details before citation.

## Questions
- What does each benchmark actually measure?
- Are subgroup comparisons based on comparable protocols and sample sizes?
- How are demographic labels defined and sourced?
- How are thresholds selected?
- Which image-quality factors are measured or controlled?
- What does a mitigation improve, and what does it worsen?
- Which findings generalise beyond a particular dataset or model?
