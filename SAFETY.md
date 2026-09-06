# Clinical Safety

## Purpose And Scope

This repository stores growth-reference datasets and supporting source publications for use by downstream RCPCH Digital Growth Charts software. It does not calculate centiles, provide clinical advice, make diagnoses, or determine treatment.

## Intended Users And Environment

The intended users are maintainers and developers of RCPCH Digital Growth Charts systems. The data must be consumed only by software that has its own clinical-safety, validation, and regulatory governance.

## Safety Status

The repository is a source-data store. Data files and transcriptions must not be treated as clinically validated solely because they are committed here. In particular, the Bayley-Pinneau data were transcribed manually and require independent validation before clinical use.

## Change Control

Changes to reference data require documented provenance, applicable licence, source version or publication, transformation details, and independent validation evidence. Review changes to tabular data as carefully as code changes. Downstream systems must assess whether a change affects clinical behaviour and update their safety documentation where required.

## Medical-Device Applicability

On 2026-09-06, the team's Clinical Safety Officer and medical-device expert determined that this repository is an informational collection, not clinical software and not a medical device. It has no calculation, interpretation, decision-support, or end-user clinical function. DCB0129 and medical-device regulation therefore do not apply. This determination is based on the repository's stated purpose and current contents and must be reassessed if it gains calculation, interpretation, executable clinical behaviour, or end-user functionality.

Medical-device classification and clinical-risk management are separate assessments. Neither is transferred from this repository to downstream software. Downstream Digital Growth Charts products determine their own medical-device applicability and clinical-safety obligations.

## Responsible Role

The RCPCH Digital Growth Charts Clinical Safety Officer and technical and clinical governance leads are responsible for reviewing changes that could alter this boundary.
