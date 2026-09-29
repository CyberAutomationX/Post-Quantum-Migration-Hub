# SecureAzCloud Post-Quantum Migration Hub

Author and maintainer: Ankit Gupta

Public, vendor-neutral planning aids for cryptographic discovery, crypto-agility assessment, cloud and identity migration, and safety-first OT/ICS transition planning.

[Live Resource Hub](https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/) |
[Current Release Notes: v2.0.0](release-notes-v2.0.0.md) |
[Final Update Report](FINAL-REPORT-v2.0.0.md) |
[Validation Report](VALIDATION-REPORT.md) |
[MIT License](LICENSE)

**Current repository version:** v2.0.0, dated 2026-09-29. **All four current workbooks:** v2.0. **NIST source review:** 2026-09-29.

> This independent hub provides planning and implementation-support artifacts. It does not claim external adoption, production deployment, certification, compliance, or endorsement by NIST, CISA, or another government agency. Recommendations published after the review date are not assumed to be known.

## Current Downloads

| Workbook | Purpose | Current files |
|---|---|---|
| Cryptographic Inventory Template | Catalog cryptographic roles, owners, lifetimes, dependencies, evidence, risks, and migration decisions. | [XLSX v2.0](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx), [CSV v2.0](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.csv), [PDF v2.0](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.pdf) |
| Crypto-Agility Assessment Template | Assess discovery, replaceability, supplier readiness, implementation, testing, and migration priorities. | [Overview](resources/crypto-agility-assessment-template.html), [XLSX v2.0](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.xlsx), [CSV v2.0](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.csv), [PDF v2.0](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.pdf) |
| PQC Cloud and Workload Identity Migration Checklist | Map certificates, issuers/verifiers, token/assertion signing, workload identities, KMS/HSM, APIs, and provider dependencies. | [Overview](resources/pqc-cloud-workload-identity-migration-checklist.html), [XLSX v2.0](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx), [CSV v2.0](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.csv), [PDF v2.0](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.pdf) |
| SCADA/ICS PQC Migration Continuity Checklist | Assess OT cryptography, trust lifetimes, constrained-device performance, vendor support, backups, rollback, and safe transition. | [Overview](resources/scada-ics-pqc-migration-continuity-checklist.html), [XLSX v2.0](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx), [CSV v2.0](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.csv), [PDF v2.0](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.pdf) |

CSV files are focused import/export companions. They do not preserve all workbook tabs, formulas, validation, formatting, or instructions. PDF companions explain usage and review controls; the XLSX files are the editable working artifacts.

## Guides and Source Maps

| Resource | Available formats |
|---|---|
| NIST 2026 and Beyond Planning Guide | [HTML](resources/nist-2026-and-beyond.html), [Markdown](resources/nist-2026-and-beyond.md) |
| PQC Readiness Checklist | [HTML](resources/pqc-readiness-checklist.html), [Markdown](resources/pqc-readiness-checklist.md) |
| Cloud/IAM Migration Playbook | [HTML](resources/cloud-iam-migration-playbook.html), [Markdown](resources/cloud-iam-migration-playbook.md) |
| SCADA/ICS PQC Readiness Checklist | [HTML](resources/scada-ics-pqc-checklist.html), [Markdown](resources/scada-ics-pqc-checklist.md) |
| NIST Source Status Register | [HTML](resources/reference-map.html), [JSON](source-map.json) |
| Artifact-to-Source Crosswalk | [HTML](resources/source-map-addendum.html), [JSON](source-map-addendum.json) |

## Standards Basis and Currency

The verified source register distinguishes final publications, drafts, project outputs, validation programs, and candidates. Source IDs provide traceability across the release.

- **Final baseline:** FIPS 203/204/205, SP 800-227, CSWP 39 Update 1 (updated 2026-06-29), IR 8587 (2026-09-15), SP 800-228 Update 1 (2026-03-13), SP 1339 (2026-06-17), SP 800-82 Rev. 3, and relevant key-management, service-mesh, supply-chain, and security-control guidance.
- **Draft watch:** IR 8547, SP 800-57 Part 1 Rev. 6, SP 800-131A Rev. 3, SP 800-82 Rev. 4, preliminary SP 1800-38, CSWP 48, SP 800-230, and SP 800-133 Rev. 3. Drafts do not become final requirements automatically.
- **Algorithm watch:** HQC and Falcon/FN-DSA standardization and additional-signature evaluation. A forecast 2027 milestone is not current approval or a guaranteed publication date.
- **Validation boundary:** algorithm standardization, CAVP algorithm validation, CMVP module validation, and deployment assurance are distinct. Record exact module/version/environment, certificate status, covered services, and applicable policy.

IR 8547 remains an initial public draft. Its transition tables propose deprecation after 2030 for the **112-bit classical public-key rows**, and disallowance after 2035; the 128-bit-and-higher rows do not carry the same 2030 deprecation entry. These are draft proposals, not universal legal deadlines or a quantum-computer arrival prediction. Earlier work may be warranted by long data or signature lifetimes and system constraints.

“Mapped” means a public source informed an artifact field, control, or workflow. It does not mean that NIST or another agency has reviewed, approved, certified, or endorsed the artifact.

## 2026, 2027, and Later Planning

| Period | Hub planning emphasis |
|---|---|
| 2026 | Evidence-backed inventory, ownership, data/trust lifetimes, threats, supplier readiness, and current source status. |
| 2027 | Supported high-risk pilots, identity/PKI interoperability, OT recovery tests, procurement, and approved staged rollout. |
| 2028–2030 | Scale proven migrations, retire avoidable legacy dependencies, and reassess proposed transition dates against then-current publications. |
| 2031–2035 | Resolve remaining lifecycle/supplier constraints in time for applicable final requirements. |
| 2036 and later | Continue discovery, cryptographic replacement capability, errata/module-status review, tests, and long-term verification obligations. |

These periods are organization-adaptable planning targets, not NIST-imposed annual requirements. Assign a review owner and review quarterly or on material changes to standards, errata, threats, protocols, supplier commitments, or validation status. **Next planned review: 2026-12-29.** This repository documents the review process; it does not provide an automated monitoring service.

## Validation and Limitations

The [validation report](VALIDATION-REPORT.md) records the release checks performed. File-integrity and usability checks are not independent technical validation, live-system tests, or proof of compliance.

- Example data is synthetic and redacted. Never publish operational inventories, hostnames, IP addresses, internal architecture, credentials, private keys, or certificate key material.
- Default scores, priority thresholds, annual phases, and review cadence are hub-defined planning heuristics.
- Unknown or unassessed data needs an owner and evidence; it must not be treated as proof of readiness.
- Organizations must approve controls, scoring, procurement, migration sequencing, and exceptions for their architecture, sector, safety obligations, and applicable requirements.
- Protocol support, product support, supplier assurances, and cryptographic validation must be verified for the actual deployment.
- External adoption, production outcomes, accessibility conformance, and compliance certification have not been established.

## Historical Downloads

Historical workbook content is preserved for link compatibility and provenance; attribution metadata has been standardized to Ankit Gupta. Use the current version 2.0 files for new assessments. Earlier workbook content has not been updated to the current guidance baseline.

| Earlier artifact | Historical files |
|---|---|
| Inventory template, original unversioned filename | [XLSX](downloads/secureazcloud-pqc-crypto-inventory-template.xlsx), [CSV](downloads/secureazcloud-pqc-crypto-inventory-template.csv) |
| Crypto-agility assessment v1.0 | [XLSX](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.xlsx), [CSV](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.csv), [PDF](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.pdf) |
| Cloud/workload identity checklist v1.0 | [XLSX](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.xlsx), [CSV](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.csv), [PDF](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.pdf) |
| SCADA/ICS continuity checklist v1.0 | [XLSX](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.xlsx), [CSV](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.csv), [PDF](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.pdf) |

See the [historical v1.1.0 notes](release-notes-v1.1.0.md) and [release history](release-notes.md).

## Feedback and Evidence of Reuse

Feedback, corrections, and redacted examples of reuse are welcome through [GitHub Issues](https://github.com/CyberAutomationX/Post-Quantum-Migration-Hub/issues/new). Include artifact/version, general use case, adaptations, measurable results, and suggested corrections. Share only non-sensitive information.

## Citation

Ankit Gupta. *SecureAzCloud Post-Quantum Migration Hub*, version 2.0.0, 2026-09-29.  
https://github.com/CyberAutomationX/Post-Quantum-Migration-Hub/blob/main/release-notes-v2.0.0.md
