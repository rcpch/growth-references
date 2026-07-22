# Agent Instructions

This repository preserves source growth-reference data and supporting publications used by RCPCH Digital Growth Charts. It is a reference-data library, not a clinical calculation service or a substitute for clinical judgement.

Read this file before changing anything.

## Read First

- [README.md](README.md) - repository scope, provenance, and licensing.
- [SAFETY.md](SAFETY.md) - clinical-use boundary and change controls.
- [~/code/rcpch/rcpch-house-style/AGENTS.md](../rcpch-house-style/AGENTS.md) - cross-repository RCPCH standards.

## Core Invariants

- Preserve source data and publications. Do not alter a dataset without recording its provenance, source, licence, and validation evidence.
- The data are not independently validated merely by being stored here. Do not claim they are clinically validated.
- Respect third-party licences and restrictions, especially the UK references distributed under their applicable licence.
- Do not add patient-identifiable data, credentials, or other secrets.

## Workflow

- Review `git diff` carefully, including data-file changes.
- For a data update, document source, version or publication, licence, transformation, and independent validation evidence in the same change.

## Approval Required

Ask before deleting or replacing reference data, relicensing content, publishing data externally, or taking other externally visible actions.
