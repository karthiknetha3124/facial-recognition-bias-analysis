# Dataset Assessment

## Selection principles
A dataset is eligible only after its official source, access route, licence or terms, annotation provenance, identity structure, permitted research use and redistribution restrictions have been reviewed. Dataset archives and face images must not be committed to this repository.

## Candidate datasets

| Dataset | Intended role | Verification suitability | Required checks |
|---|---|---|---|
| RFW | Primary demographic face-verification benchmark | Identity-labelled comparisons are central to its design | Official protocol, subset definitions, access terms and licence |
| FairFace | Demographic representation and label distributions | Not the primary identity-pair benchmark | Annotation definitions, licence and source-image terms |
| UTKFace | Supplementary attribute distribution and image-condition exploration | Do not assume identity-pair suitability | Official terms and label provenance |
| LFW | General face-verification reference | Established identity-labelled verification benchmark | Official protocol, licence and comparability |

## Dataset register
For every dataset record:
- Name, version, official URL and download date.
- Licence/terms URL and reviewed interpretation.
- Commercial use, modification, redistribution and hosted-deployment permissions.
- Identity labels and official pair protocol.
- Demographic fields, category definitions and annotation provenance.
- Identities, images and eligible pairs after filtering.
- Missing labels, exclusions and group counts.
- Known collection, sampling and representation limitations.
- Local storage location (never a personal path in a public commit) and checksums.

## Pair protocol
A verification benchmark requires genuine pairs (two images of the same identity) and impostor pairs (different identities). Follow the official protocol where available. If custom pairs are necessary, document deterministic generation, random seed, sampling rules and identity-disjoint splits. Avoid identity leakage between development and evaluation.

## Fairness constraints
Use demographic labels supplied by dataset documentation or a documented research annotation process. Do not infer race, ethnicity or gender from pixels. Do not treat dataset categories as universal identities. Report group sample sizes and uncertainty; qualify estimates with insufficient samples.

## Gate before use
No dataset enters the benchmark pipeline until its official terms and suitability are documented. Public availability alone does not establish permission for every research, redistribution or hosted-demo use.
