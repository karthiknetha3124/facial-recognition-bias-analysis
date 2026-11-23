# Model Selection and Governance

## Comparison design
Compare two pretrained face-verification models under one documented protocol. This is not a claim that either model is state of the art or suitable for real-world identity decisions.

## Model A — SFace
- Initial baseline: OpenCV SFace.
- Integration: OpenCV face-recognition API and a pinned ONNX checkpoint.
- Role: CPU-friendly baseline for embeddings and similarity-based verification.
- Verify exact checkpoint provenance, source URL, checksum, model documentation and licence before use or deployment.

## Model B — ArcFace-family candidate
- Candidate family: an ArcFace-based pretrained embedding model.
- Exact implementation and checkpoint are not yet approved.
- Selection gate: identify official source, exact checkpoint, architecture/input requirements, checksum and explicit licence/use conditions.
- Do not confuse source-code licensing with pretrained-weight licensing. Some distributed pretrained weights have research-only or non-commercial restrictions.
- If a suitable ArcFace checkpoint cannot meet free-use and licensing constraints, select another documented model and update this decision record.

## Fair comparison record
For each model record architecture, implementation version, checkpoint source and SHA-256, model and weight licences separately, preprocessing, input dimensions, alignment, normalisation, embedding dimensions, similarity function, threshold protocol, runtime and known training-data/overlap concerns.

Use the same eligible pair list and evaluation split for both models wherever valid. Preserve and document model-specific preprocessing. Never tune thresholds on the final test set.

## CPU-first constraints
Run small batches, cache only permitted derived artefacts, avoid GPU requirements in the core path, and benchmark CPU runtime. Keep full benchmark runs local; the hosted app should use a small demonstration subset or precomputed aggregate results.

## Release gate
Do not commit model weights unless redistribution is explicitly permitted. Prefer documented download instructions and checksums. Do not deploy a checkpoint until its exact licence permits the intended hosted demonstration.
