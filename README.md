# Growth References

This repository preserves growth-reference datasets and supporting publications used by RCPCH Digital Growth Charts. It is a source-data library, not a clinical calculation service, clinical decision-support tool, or substitute for clinical judgement.

## Included References

- UK-WHO, including the UK90 preterm reference
- WHO
- CDC, including extended BMI data
- Trisomy 21 references for the UK and United States
- Turner syndrome
- Bayley-Pinneau predicted adult-height tables
- Spirometry

## Data Quality And Provenance

Each dataset remains subject to its original source, terms, and licensing restrictions. In particular, the UK references are available only under their applicable MRC licence, while WHO and CDC data are published as open data. Do not redistribute or reuse data beyond the permissions granted by the relevant source.

The Bayley-Pinneau data were transcribed manually from the accompanying publication and have not been independently validated in this repository. Validate them independently before any clinical use.

For changes to reference data, record the source, licence, source version or publication, transformation, and validation evidence in the same change. See [SAFETY.md](SAFETY.md) for the clinical-use boundary and change controls.

## Documentation

Growth-reference documentation is available at [growth.rcpch.ac.uk](https://growth.rcpch.ac.uk/clinician/growth-references/). Documentation about LMS methodology and calculations is available at [How the API works](https://growth.rcpch.ac.uk/clinician/how-the-api-works/).

## Contributing

Read [AGENTS.md](AGENTS.md) and [SAFETY.md](SAFETY.md) before proposing a data change. Do not replace or alter source data without provenance and independent validation evidence.

The directory taxonomy, canonical JSON representation, contextual metadata, and validation approach are being designed. See the [repository specification](spec/README.md) and [roadmap](spec/roadmap.md). Existing directories are legacy organisation and should not be treated as the future naming standard.

## Licence

Material in which the Royal College of Paediatrics and Child Health holds the necessary rights is licensed under [Creative Commons Attribution-ShareAlike 4.0 International](LICENSE).

The repository also reproduces datasets and publications created by others. RCPCH asserts no copyright in those works. All copyright, attribution requirements, licensing terms, and usage restrictions remain with their original authors and rights holders and take precedence over the repository licence. In particular, the UK references remain subject to their applicable MRC licence.
