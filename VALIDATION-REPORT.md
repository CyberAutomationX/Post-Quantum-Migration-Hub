# Validation report - PQC Hub v2.0.0

Author: Ankit Gupta | Reviewed: 2026-09-29

This report records artifact checks. It does not certify native Excel behavior or production cryptographic deployments.

## Workbook package checks

| File | Sheets | Formulas | Validation rules | Excel tables | Result |
|---|---:|---:|---:|---:|---|
| [secureazcloud-crypto-agility-assessment-template-v2.0.xlsx](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.xlsx) | 8 | 607 | 25 | 1 | No archive/XML, cached error or broken reference findings |
| [secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx) | 7 | 42 | 9 | 6 | No archive/XML, cached error or broken reference findings |
| [secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx) | 9 | 3007 | 27 | 7 | No archive/XML, cached error or broken reference findings |
| [secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx) | 6 | 41 | 10 | 5 | No archive/XML, cached error or broken reference findings |

Formula builders tested representative live input changes, restoration to the delivered state, blank-versus-zero handling and missing-evidence conditions. Worksheet ranges were rendered and visually reviewed. Native Microsoft Excel desktop was unavailable.

## Companion and link checks

All four current workbook families include XLSX, CSV and PDF. Local relative-link validation checked 224 links with zero unresolved targets. PDF pages were rendered and visually reviewed. Historical download content is preserved; attribution metadata is standardized to Ankit Gupta.

## SHA-256 for current downloads

| File | Bytes | SHA-256 |
|---|---:|---|
| [secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx) | 456872 | `242e25d17f88bec3a919664f6abebdc31872ca9a5e07257547595f6803777137` |
| [secureazcloud-pqc-crypto-inventory-template-v2.0.csv](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.csv) | 7088 | `e7ca2de79b4060dfa30c124ea66e932ee773d9409dbc32d131be467414603145` |
| [secureazcloud-pqc-crypto-inventory-template-v2.0.pdf](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.pdf) | 111745 | `50e16d51df1d1ee5470f0a5a3f27b6ae3518c0b765478d31bb60164e4685af3b` |
| [secureazcloud-crypto-agility-assessment-template-v2.0.xlsx](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.xlsx) | 56591 | `ab0b2a6fceaf708683ac8c679d20ce2d28a2acb3bdee638ad3373e90454da75e` |
| [secureazcloud-crypto-agility-assessment-template-v2.0.csv](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.csv) | 5449 | `4cb264098af1cc558d4ce6f760e3f55bc3079b444d511b2ad6517505cff680bc` |
| [secureazcloud-crypto-agility-assessment-template-v2.0.pdf](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.pdf) | 98803 | `8caf555dd1a201f613a30b80580e58389b40020bb0c5ec207813929762023af2` |
| [secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx) | 39555 | `90491f7f8cf21130af9462abcac966cdbb22c1ccc44689df5664a6189729d731` |
| [secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.csv](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.csv) | 17063 | `5d7c2f76c119b57f00afd71b9563d20892d69e750d9c7c94d4e463ad60f7d7c9` |
| [secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.pdf](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.pdf) | 101760 | `12e0480636f169a3972816694686786b7a2ab47012dc0b5fe86d0547ad4b6fea` |
| [secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx) | 35603 | `669dca7740e2067d252ad10b2bd4d3f5bac13c5f2bb346322f17fe2ea3942474` |
| [secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.csv](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.csv) | 13367 | `a9cfcc76b56ba168eadb8c1d93e154cd01044ccc75a3b552c72ea0eaf0820c59` |
| [secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.pdf](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.pdf) | 94568 | `c236a33544d8f725995f38ec8dd5737ed9bab96978fc59374709d6224b9912ff` |

## Source review

Official NIST sources were checked as of 2026-09-29. Final, draft, preliminary and selected-for-standardization statuses are distinguished. Annual roadmap phases, review cadence and score weights are Hub planning choices. See the [source/status guide](resources/nist-2026-and-beyond.html).

## Scope boundaries

No production systems were scanned, no real-world cryptographic migration was performed, and no native Excel certification is asserted. GitHub Pages build status is verified separately after the repository commit.
