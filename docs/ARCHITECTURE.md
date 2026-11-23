# System Architecture

## Principles
1. Reproducibility over convenience.
2. CPU-first execution and explicit dependencies.
3. Separation of demonstration uploads and benchmark datasets.
4. Two model adapters behind a common verification interface.
5. Aggregate reporting by default; no persistent biometric database.
6. Dataset and model provenance are first-class metadata.

## Logical flow
~~~mermaid
flowchart TD
    A[Public benchmark datasets] --> B[Dataset manifest and validation]
    C[Single image upload or webcam] --> D[Transient image lab]
    B --> E[Preprocessing and pair protocol]
    D --> F[Face detection and quality checks]
    E --> G[Model A adapter: SFace]
    E --> H[Model B adapter: ArcFace candidate]
    G --> I[Verification scores]
    H --> I
    I --> J[Metrics and subgroup evaluation]
    J --> K[Statistical analysis]
    K --> L[Fairness and mitigation reports]
    F --> M[Transient demonstration output]
    L --> N[Streamlit research dashboard]
    M --> N
~~~

## Proposed repository modules
~~~text
src/
  config/          # validated experiment configuration
  data/            # manifests, validation and pair protocols
  preprocessing/   # image loading, alignment and quality indicators
  detection/       # YuNet detector adapter
  recognition/     # common interface and model-specific adapters
  evaluation/      # verification scores and threshold metrics
  fairness/        # subgroup metrics, gaps and uncertainty
  mitigation/      # controlled mitigation experiments
  reporting/       # aggregate tables, figures and export
  privacy/         # transient upload handling and cleanup
  utils/           # reproducibility utilities
dashboard/
  app.py           # Streamlit entry point
tests/
  unit/
  integration/
notebooks/         # exploration; production logic stays in src/
docs/
~~~

## Runtime paths

### Research benchmark
Dataset manifest → validation → official/custom pair protocol → preprocessing → both model adapters → similarity scores → metrics → subgroup/statistical analysis → aggregate results.

### Individual image
Explicit upload or webcam capture → in-memory image handling → face detection and quality indicators → optional two-image verification demonstration → result → temporary data discarded.

Individual uploads are not part of population-level fairness analysis unless separately collected and labelled under an approved research protocol.

## Model adapter contract
Each adapter exposes model metadata and checkpoint provenance, preprocessing requirements, embedding extraction, normalisation behaviour, similarity scoring and runtime/error reporting. Detector, alignment, colour order and input scaling must never change silently.

## Deployment
Run full research experiments locally on CPU. Streamlit Community Cloud is a lightweight demonstration target, not the guaranteed environment for full benchmark runs. Public hosting should initially show aggregate precomputed results; enable image demonstrations only after privacy and model-licensing checks.

## Configuration and outputs
Use version-controlled configuration files without private paths or credentials. Store aggregate metrics, run metadata and checksums. Never write raw face images or embeddings into ordinary logs or Git.
