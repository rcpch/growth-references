# Agent Instructions

This repository preserves growth-reference data and supporting publications used by RCPCH Digital Growth Charts. It is an informational reference collection, not clinical software, a clinical calculation service, a medical device, or a substitute for clinical judgement.

This file is the entry point for AI coding agents. Read it before changing anything.

## Read First

- [README.md](README.md) - repository scope, provenance, and licensing.
- [SAFETY.md](SAFETY.md) - the clinical and regulatory boundary.
- [spec/README.md](spec/README.md) - repository standards and design work.
- [spec/roadmap.md](spec/roadmap.md) - current priorities and unresolved standards.
- [RCPCH house style](../rcpch-house-style/AGENTS.md) - cross-repository RCPCH standards.

## Core Invariants

- Preserve upstream data and source-of-truth publications. Do not delete, replace, modify, or redistribute them without explicit approval and a review of their original terms.
- Do not imply that RCPCH owns copyright in reproduced third-party work. The original authors' rights and licensing terms continue to apply.
- Do not alter reference data without recording its provenance, source version or publication, applicable licence, transformation, and independent verification evidence.
- Storage in this repository is not evidence that data are clinically validated. Do not describe a reference as clinically validated without independent evidence.
- Do not add patient-identifiable data, credentials, or other secrets.
- Treat existing directory and file names as legacy source organisation until a canonical taxonomy and migration plan are approved. Do not rename reference directories merely for consistency.

## Target Repository Model

- Every reference will eventually use one documented directory taxonomy, regardless of whether it is commonly identified by author, physiological measurement, condition, population, or publication.
- Every standardised reference will eventually include a canonical JSON representation and human-readable Markdown context.
- The canonical representation should allow any parameter expressed in an agreed LMS format to be loaded by a compatible growth-chart engine without embedding engine-specific behaviour in this repository.
- Upstream source-of-truth documents may be stored beside the canonical representation for ready verification, subject to their original licence and distribution terms.
- The taxonomy, JSON schema, metadata requirements, and migration rules are design work tracked in [spec/roadmap.md](spec/roadmap.md). Do not invent a competing format in an individual data contribution.

## Workflow

- Review `git diff` carefully, including binary and tabular data changes.
- Keep exploratory format proposals under `spec/` or in clearly marked fixtures until a format is accepted.
- For a data change, include provenance, applicable licence, source version or publication, transformation details, and independent verification evidence in the same change.
- Preserve exact upstream files. Put transformations in separate files and document how they were produced.
- Use lowercase slug-case for new repository-authored file and directory names unless an adopted schema requires another convention. Do not rename upstream files solely to satisfy this convention.

## Validation

The repository does not yet have an automated validation suite. Until the canonical structure and data format are agreed:

- run `git diff --check`;
- inspect every changed data file and its provenance documentation;
- verify that upstream source files remain byte-for-byte unchanged unless their replacement was explicitly approved; and
- record manual verification performed in the pull request.

Automated schema, integrity, and provenance checks will be introduced after the standards they enforce are accepted.

## Assurance

- Agent-generated content and tests are not independent evidence that reference data are correct.
- Validate transcriptions and transformations against authoritative upstream material, and record who performed the independent verification.
- Downstream clinical software is responsible for its own clinical-safety, validation, and regulatory governance.

## Approval Required

Ask before deleting or replacing reference data, relicensing content, publishing or redistributing data externally, adopting or changing the canonical schema, migrating existing reference directories, or taking other externally visible actions.
