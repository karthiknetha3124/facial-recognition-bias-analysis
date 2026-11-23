# Phase 1 — Foundation Status

## Decisions confirmed
- Audience: academic research.
- Compute: zero-cost, CPU-first.
- Dataset strategy: public research datasets, subject to terms and access restrictions.
- Inputs: individual image uploads and webcam capture for transient demonstrations.
- Model comparison: two pretrained face-verification models.
- Ethics: researcher reports university approval as confirmed; implementation must remain within the approved protocol.

## Foundation committed
- Research question, aim, objectives and working hypotheses.
- Literature review plan and initial source list.
- Candidate dataset assessment and eligibility gates.
- Model governance plan: SFace baseline and ArcFace-family second-model candidate.
- Verification metrics, experiments and statistical methodology.
- Ethics, privacy and data-minimisation requirements.
- Logical architecture and module boundaries.
- Initial Python project configuration and CPU-first dependency list.
- Git ignore rules for datasets, checkpoints, embeddings and generated artefacts.

## Open gates before Phase 2
- [ ] Verify the university approval covers the exact datasets, webcam/upload flow, processing, storage and intended deployment.
- [ ] Review and record the current official terms for each candidate dataset.
- [ ] Confirm the primary benchmark and obtain access under its permitted terms.
- [ ] Verify exact SFace checkpoint provenance, checksum and licence.
- [ ] Verify an ArcFace-family checkpoint's exact weight licence; choose a permitted alternative if needed.
- [ ] Confirm pair protocol, identity split and sample-size feasibility.
- [ ] Complete the literature review with primary-source citations.
- [ ] Run a clean Python 3.11 dependency installation on the target Mac and resolve any platform conflicts.

## Phase 1 exit decision
The documentation and repository foundation are in place, but Phase 1 is not academically complete until the open gates above are evidenced. No model results or fairness findings are claimed yet.
