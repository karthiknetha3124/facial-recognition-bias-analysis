# Ethics, Privacy and Data Governance

## Approval status
The researcher has stated that university ethics approval is confirmed. The approved application, conditions and amendments govern the work. This repository does not contain confidential approval paperwork or approval reference numbers.

Verify that approval covers each activity actually undertaken:
- Each named public dataset and its terms.
- Individual image uploads.
- Webcam capture and participant-facing consent wording.
- Local processing and any cloud-hosted inference.
- Temporary storage, derived embeddings, logs and retention periods.
- Public demonstration and publication of aggregate results.

If an activity falls outside the approved scope, pause it and seek university guidance or an amendment before proceeding.

## Data minimisation
- Use only images and metadata required for the experiment.
- Keep benchmark datasets outside Git.
- Do not collect names, contact details or unrelated personal information.
- Avoid persistent storage of uploads and webcam captures.
- Do not retain face embeddings by default; embeddings are biometric-derived data and must be treated as sensitive.
- Keep logs free of image bytes, embeddings, identity labels and personal identifiers.

## Upload and webcam design
Explain purpose before image selection or capture. Request camera permission only after explicit user action. Make capture optional with clear stop/retake controls. Process images transiently, discard temporary files and do not send images to third-party APIs. Captured images must not silently enter benchmark or training datasets.

## Research safeguards
Use dataset-provided demographic annotations; do not infer race or ethnicity from pixels. Do not infer emotion, personality, health or internal traits. Similarity scores are not identity proof. Present the platform as a research evaluation tool, not an operational identity or surveillance system.

## Security and deployment
Keep secrets out of source control. Restrict access to local research data. Review hosting logs, storage and retention behaviour before enabling public uploads or webcam capture. The public demo should default to aggregate precomputed results if the hosting environment cannot guarantee the approved privacy model.

## Incident and change process
If sensitive data is retained, exposed or committed unintentionally, stop the affected workflow and follow university incident procedures. Any material change to collection, retention, model use or hosting must be checked against the approved protocol before release.
