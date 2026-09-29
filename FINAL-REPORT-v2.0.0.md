# PQC Hub final update report

Author: Ankit Gupta

Release v2.0.0 | Workbooks v2.0 | Source review: September 29, 2026

## Outcome

All four current workbook families have been refreshed against the relevant NIST publications available on the review date. The release includes new Excel workbooks, CSV companions, readable PDF guides, updated web pages and source maps, and a 2026 through 2036+ planning framework. Existing download filenames remain available as historical versions so previously shared links continue to work. Current navigation points to v2.0. Historical workbook content is preserved; attribution metadata is standardized to Ankit Gupta.

The release addresses cryptographic inventory, quantum and implementation threats, crypto agility, cloud identity, supplier dependencies, and operational continuity. Annual phases, checklist controls, and scoring are Hub implementation aids. They are not additional NIST mandates or a certification of compliance. Unpublished future guidance cannot be incorporated in advance; standards-watch and reassessment instructions support subsequent updates.

## Current downloads

| Workbook | Version | Files |
|---|---|---|
| Cryptographic Inventory | v2.0 | [XLSX](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx) / [CSV](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.csv) / [PDF](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.pdf) |
| Crypto-Agility Assessment | v2.0 | [XLSX](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.xlsx) / [CSV](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.csv) / [PDF](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.pdf) |
| Cloud and Workload Identity | v2.0 | [XLSX](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx) / [CSV](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.csv) / [PDF](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.pdf) |
| SCADA/ICS Continuity | v2.0 | [XLSX](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx) / [CSV](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.csv) / [PDF](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.pdf) |

CSV files are flat exports of the primary inventory or checklist. Excel contains the complete multi-sheet working template. PDFs are static reading companions and do not perform workbook calculations.

## What changed

| Area | Updated coverage |
|---|---|
| Inventory | Discovery provenance, observation dates and evidence, cryptographic functions and parameters, software and firmware versions, dependencies and trust boundaries, data and signature lifetimes, vendor support and migration constraints. Example records remain clearly identified. |
| Crypto agility | Replaceable implementations, policy and negotiation controls, supplier evidence, interoperability, emergency replacement, rollback, lifecycle management and evidence-based assessment. Local risk heuristics are identified as local rather than NIST-defined scores. |
| Cloud identity | Token and assertion protection, issuers and validators, federation and workload identities, key lifecycle, trust distribution, algorithm restrictions, token size and parser limits, compromise recovery and end-to-end test evidence. |
| OT/ICS | Safety and change authorization, passive discovery, firmware and boot verification, hardware and protocol limits, latency and resource testing, vendor-supported changes, failover, backup restoration, rollback and replacement planning. |
| Threats | Harvest-now/decrypt-later, future signature forgery, immutable or long-lived verification dependencies, downgrade and fallback, key compromise, unsupported algorithms, supply-chain and implementation failures, incomplete discovery and operational disruption. |
| Assurance | Source status and review dates, algorithm versus module validation, exact module/version/configuration evidence, owner and evidence fields, and treatment of missing or unknown information. |

## Material NIST updates and corrections

- **CSWP 39-upd1:** use the final June 29, 2026 update for crypto-agility planning rather than the superseded original publication.
- **SP 800-227:** incorporate final KEM implementation and usage recommendations, including the distinction between key establishment and bulk encryption.
- **IR 8587:** incorporate the September 15, 2026 final token/assertion guidance, including PQC migration considerations. Transport PQC does not automatically protect token signatures.
- **SP 800-228-upd1:** use the March 13, 2026 update for cloud API lifecycle considerations.
- **SP 1339:** incorporate June 17, 2026 OT backup and recovery guidance.
- **SP 800-82 Rev. 4:** track the September 21, 2026 initial public draft while retaining Rev. 3 as the final OT baseline.
- **IR 8547:** retain its initial-public-draft status. Its proposed post-2030 deprecation applies to specified 112-bit classical uses; it is not a blanket 2030 prohibition on all RSA/ECC. The draft proposes post-2035 disallowance for the covered quantum-vulnerable uses. Apply current final and application-specific requirements when making deployment decisions.
- **Algorithm watch:** FIPS 203/204/205 are final. HQC and Falcon/FN-DSA standardization and additional signature candidates remain watch items, not interchangeable approved production standards. An anticipated 2027 milestone is not a guaranteed publication date.
- **Draft watch:** SP 800-57 Part 1 Rev. 6, SP 800-131A Rev. 3, SP 800-230 and SP 800-133 Rev. 3 are labeled drafts. SP 1800-38 remains preliminary demonstration guidance.

Publication links and exact status details are maintained in the [2026 and beyond guide](resources/nist-2026-and-beyond.html) and the workbook source registers.

## Planning horizons

These phases are recommendations for organizations adopting the Hub. They do not establish universal NIST deadlines.

| Period | Focus |
|---|---|
| 2026 | Establish accountable ownership, reconcile inventory and unknowns, prioritize long-lived confidential data and verification dependencies, obtain supplier evidence and define test acceptance criteria. |
| 2027 | Pilot high-risk supported paths, validate cloud identity and PKI interoperability, test OT recovery, and include agility and lifecycle evidence in procurement. |
| 2028-2030 | Expand proven migrations, reduce avoidable legacy dependencies and reconcile planning assumptions with then-current final standards and applicable requirements. |
| 2031-2035 | Close remaining long-lived and vendor-constrained gaps, fund replacements, manage exceptions and remove obsolete fallback paths. |
| 2036+ | Continue inventory refresh, standards and errata review, emergency substitution exercises, supplier checks and retention/verification lifecycle management. |

The recommended review cadence is quarterly and after significant standards, errata, cryptanalytic, product, incident or architecture changes. This release documents the cadence; it does not activate an automated monitoring service.

## Validation and practical limits

- Four XLSX packages passed archive/XML integrity checks. Across 30 worksheets, the saved files contained no cached Excel error cells or broken `#REF!` formula references.
- Workbook builders recalculated formulas, exercised representative input changes and missing-data boundaries, exported the final files, and reviewed rendered worksheet ranges.
- PDF guides were rendered for page-level visual review. CSV companions and current download paths were checked.
- Local validation checked 224 relative HTML/Markdown links with no missing file or HTML-fragment targets.
- Native Microsoft Excel desktop behavior was not tested in this environment. Formula evaluation and file inspection do not establish product certification, production interoperability or deployment readiness.
- No organization-specific discovery or real migration testing was performed. The templates require users to supply actual inventory, evidence, approvals, engineering thresholds and supplier support details.

See the [validation report](VALIDATION-REPORT.md) for file-level checks and hashes, and [release notes](release-notes-v2.0.0.md) for the release summary.
