# Roadmap

Legend: [x] done, [~] in progress or partially done, [ ] not started

The aim is to make this repository a coherent, verifiable collection in which any parameter represented in an agreed LMS format can be consumed by a compatible growth-chart engine. Standards will be proposed and tested here before existing references are migrated or automated checks become mandatory.

## Reference Standard

- [ ] **REF-1 - Define the reference taxonomy.** Compare organisation by author or method, physiological measurement, condition, population, publication, and other useful facets. Choose one canonical directory hierarchy that remains clear when a reference spans several facets. Define lowercase slug-case identifiers, required directory levels, treatment of aliases, and rules for preserving upstream filenames. Done when an accepted specification includes worked mappings for every existing top-level reference directory and at least three plausible future references.
- [ ] **REF-2 - Define the canonical JSON representation.** Specify a versioned, engine-independent JSON structure for parameters represented using the LMS method, including units, sex or population dimensions, age domains, interpolation assumptions, and explicit handling of parameters that do not fit a simple LMS table. Done when a published schema and representative fixtures can express existing WHO, UK-WHO, condition-specific, and spirometry examples without loss of meaning.
- [ ] **REF-3 - Define required human-readable context.** Specify the Markdown document stored with each standardised reference, including intended population, parameter, source citation, source version, licence, transformation, limitations, verification status, and links to accompanying source documents. Done when a template has been tested against representative references from different categories.
- [ ] **REF-4 - Define provenance and source-document metadata.** Decide how canonical JSON, context documents, and upstream source-of-truth files identify one another; distinguish exact upstream files from transcriptions and derived representations; and record checksums where useful. Done when every artefact's origin, rights, transformation history, and verification state can be determined without relying on Git history alone.
- [ ] **REF-5 - Prototype before standardising.** Build small competing format proposals against representative references, including awkward cases, and document what each experiment demonstrates. Do not migrate the collection while the format is exploratory. Done when evidence supports the selected taxonomy and schema and rejected alternatives are briefly recorded.
- [ ] **REF-6 - Plan the legacy migration.** Map every existing directory and file to the accepted taxonomy, identify downstream path dependencies, and separate moves from data transformations so reviews remain intelligible. Existing reference data must not be deleted or replaced. Done when an approved migration plan accounts for every tracked reference artefact and provides a reversible sequence of changes.

## Validation And Tooling

- [ ] **VAL-1 - Define conformance rules.** After REF-1 through REF-4 are accepted, specify which structural, schema, provenance, checksum, and cross-file consistency rules can be checked automatically and which require expert review.
- [ ] **VAL-2 - Add local validation commands.** Implement the accepted checks behind discoverable `s/` scripts and update `agent-instructions.md` with exact before-commit commands. Done when a fresh checkout can run all checks using documented prerequisites.
- [ ] **VAL-3 - Add CI after local checks stabilise.** Run the same accepted checks for pull requests using least-privilege, SHA-pinned GitHub Actions, then add Dependabot for the ecosystems actually introduced. Do not add placeholder CI before there is a meaningful repository contract to enforce.

## Documentation And Presentation

- [~] **DOC-1 - Establish repository guidance.** `agent-instructions.md`, `SAFETY.md`, and this specification now state the repository's purpose and current change controls. Complete this task when accepted taxonomy, format, provenance, and validation specifications replace the remaining future-facing guidance.
- [ ] **DOC-2 - Rebuild the README around the accepted standard.** Explain who the collection is for, how references are organised, how canonical JSON relates to upstream sources, how to consume or contribute a reference, current validation status, and all licensing boundaries. Align the GitHub description, documentation link, and topics with the revised README.

## House-Style Audit

Audit date: 2026-09-06

Applicable standards reviewed: RCPCH agent guidance, clinical safety, licensing, security, repository scaffold, scripts, specifications, testing, and CI; personal house-style repository presentation guidance.

The repository has a deliberately narrow purpose, preserves source material, states that storage is not clinical validation, uses a signed conventional commit for the current migration, and now has explicit clinical and regulatory boundaries.

### P1 - Rights And Data Governance

- [~] **HS-1 - Make licensing boundaries explicit.** The root `LICENSE` and `README.md` now apply CC-BY-SA-4.0 only to material for which RCPCH holds the necessary rights and explicitly exclude reproduced third-party works. Complete this by implementing the provenance and per-reference rights model in REF-3 and REF-4, then assess whether `REUSE.toml` can accurately encode the mixed licensing.
- [~] **HS-2 - Make data-change controls enforceable.** `agent-instructions.md` defines interim manual controls, while REF-1 through REF-4 define the contract required before automation. Complete through VAL-1 to VAL-3 after the reference standard is accepted.

### P2 - Assurance And Maintenance

- [x] **HS-3 - Record the clinical and regulatory boundary.** `SAFETY.md` records the CSO and medical-device expert determination that this informational collection is neither clinical software nor a medical device and that DCB0129 and medical-device regulation do not apply.
- [~] **HS-4 - Provide exact agent validation guidance.** `agent-instructions.md` records interim manual validation and explains why automated checks are deferred. Complete when VAL-2 supplies commands for the accepted standard.
- [x] **HS-5 - Provide a concrete private security contact.** `SECURITY.md` directs reports to the shared `incubator@rcpch.ac.uk` mailbox and describes the limited credible concerns for this repository.

### P3 - Consistency And Presentation

- [~] **HS-6 - Keep `.gitignore` relevant and complete.** The generated Python template has been pruned and common local agent artefacts are ignored. Revisit entries when validation tooling introduces actual build or test artefacts.
- [ ] **HS-7 - Improve repository presentation.** Complete DOC-2 after the reference standard is sufficiently clear to document honestly.

### Deliberate Exceptions And Non-Applicable Standards

- Existing reference directory and upstream filenames do not follow current naming conventions. They remain unchanged until REF-1 and REF-6 are approved because preserving source data and downstream compatibility takes precedence over cosmetic consistency.
- Automated tests, CI, and Dependabot are deliberately deferred until there is an accepted repository contract to enforce. This exception must be revisited through VAL-1 to VAL-3.
- DCB0129 and medical-device regulation are not applicable because this repository is an informational collection, not clinical software or a medical device. Reassess if it gains calculation, interpretation, or end-user functionality.
- Docker, deployment, service architecture, application dependency management, and user-interface standards are not applicable.
