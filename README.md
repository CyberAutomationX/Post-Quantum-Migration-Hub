# SecureAzCloud Post-Quantum Migration Hub

Public, vendor-neutral planning aids for cryptographic discovery, crypto-agility assessment, cloud and identity migration, and safety-first OT/ICS transition planning.

[Live Resource Hub](https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/) |
[Latest Release: v1.1.0](https://github.com/CyberAutomationX/Post-Quantum-Migration-Hub/releases/tag/v1.1.0) |
[Validation Report](VALIDATION-REPORT.md) |
[MIT License](LICENSE)

**Current repository release:** v1.1.0, published 2026-06-07.

> This repository provides planning and implementation-support artifacts. It does not claim external adoption, production deployment, certification, compliance, or endorsement by NIST, CISA, or another government agency.

## Resource Catalog

| Artifact | Practical Use | Available Formats |
|---|---|---|
| Cryptographic Inventory Template | Catalog cryptographic assets, algorithms, certificates, identities, suppliers, cloud workloads, and OT dependencies; calculate a default planning score and migration priority. | [XLSX](downloads/secureazcloud-pqc-crypto-inventory-template.xlsx), [CSV](downloads/secureazcloud-pqc-crypto-inventory-template.csv) |
| PQC Readiness Checklist | Assess governance, inventory, data risk, crypto agility, PKI, cloud/IAM, supplier, testing, and operational readiness. | [HTML](resources/pqc-readiness-checklist.html), [Markdown](resources/pqc-readiness-checklist.md), included in the inventory workbook |
| Cloud/IAM Migration Playbook | Plan phased discovery, prioritization, design, pilot, rollout, and operation for cloud, IAM, PKI, federation, machine identity, and signing dependencies. | [HTML](resources/cloud-iam-migration-playbook.html), [Markdown](resources/cloud-iam-migration-playbook.md), included in the inventory workbook |
| SCADA/ICS PQC Readiness Checklist | Apply safety-first discovery, vendor coordination, lab validation, compensating controls, and lifecycle planning to OT environments. | [HTML](resources/scada-ics-pqc-checklist.html), [Markdown](resources/scada-ics-pqc-checklist.md), included in the inventory workbook |
| Crypto-Agility Assessment Template | Convert an evidence-backed crypto inventory into a weighted risk score, P1/P2/P3 backlog, migration roadmap, and supplier questionnaire. | [Overview](resources/crypto-agility-assessment-template.html), [XLSX](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.xlsx), [CSV](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.csv), [PDF](downloads/secureazcloud-crypto-agility-assessment-template-v1.0.pdf) |
| PQC Cloud and Workload Identity Migration Checklist | Map certificates, workload identities, token signing, KMS/HSM, SaaS, CI/CD signing, and non-production pilot dependencies. | [Overview](resources/pqc-cloud-workload-identity-migration-checklist.html), [XLSX](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.xlsx), [CSV](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.csv), [PDF](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.pdf) |
| SCADA/ICS PQC Migration Continuity Checklist | Plan latency testing, legacy-gateway handling, maintenance windows, vendor dependencies, rollback, and operational continuity. | [Overview](resources/scada-ics-pqc-migration-continuity-checklist.html), [XLSX](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.xlsx), [CSV](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.csv), [PDF](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.pdf) |
| Source and Standards Maps | Identify the public NIST and CISA sources that informed the artifact fields and workflows. | [Base Map](resources/reference-map.html), [Base JSON](source-map.json), [v1.1 Addendum](resources/source-map-addendum.html), [Addendum JSON](source-map-addendum.json) |

The three implementation artifacts added in repository release v1.1.0 retain file version v1.0 because they are the first releases of those individual artifacts.

## Standards Basis and Currency

The artifacts are informed by public sources including NIST FIPS 203, FIPS 204, FIPS 205, the NIST NCCoE Migration to PQC project, NIST crypto-agility guidance, NIST SP 800-82, NIST SP 800-161, and CISA quantum-readiness resources.

“Mapped” means that a public source informed an artifact field, control, or workflow. It does not mean that NIST, CISA, or another agency has reviewed, approved, certified, or endorsed the artifact.

### Source Currency Note

Release v1.1.0 was published on 2026-06-07. It predates the following sources, which are not yet explicitly crosswalked into the v1.1.0 downloadable artifacts:

- [Executive Order 14412, Securing the Nation Against Advanced Cryptographic Attacks](https://www.whitehouse.gov/presidential-actions/2026/06/securing-the-nation-against-advanced-cryptographic-attacks/), published 2026-06-22
- [OMB Memorandum M-26-15, Execution of the Migration to Post-Quantum Cryptography](https://www.whitehouse.gov/wp-content/uploads/2026/06/M-26-15-Execution-of-the-Migration-to-Post-Quantum-Cryptography.pdf), published 2026-06-24
- [NIST CSWP 39upd1, Considerations for Achieving Crypto Agility](https://csrc.nist.gov/pubs/cswp/39/upd1/considerations-for-achieving-crypto-agility/final), updated 2026-06-29

Users applying these resources to federal systems should review those sources directly.

## Validation and Limitations

The [validation report](VALIDATION-REPORT.md) records local structural checks for workbook import, scoring formulas, PDF rendering, and relative file links. These checks demonstrate file integrity and basic usability; they are not independent technical validation or production testing.

- Example data is synthetic and redacted.
- Default scoring weights and priority thresholds are maintainer-defined planning heuristics, not NIST or CISA scoring methods.
- Organizations should review and approve scoring, controls, and migration sequencing for their architecture, sector, safety obligations, and regulatory requirements.
- Accessibility conformance, external adoption, production outcomes, and compliance certification have not been established.

## Feedback and Evidence of Reuse

Feedback, corrections, and redacted examples of reuse are welcome through [GitHub Issues](https://github.com/CyberAutomationX/Post-Quantum-Migration-Hub/issues/new).

When reporting reuse, include only non-sensitive information:

- Artifact and version used
- Sector or general use case
- Adaptations made
- Measurable result, such as assets inventoried, controls assessed, suppliers contacted, or pilots completed
- Suggested corrections or missing fields

Do not upload inventories, hostnames, IP addresses, customer information, internal architecture, credentials, certificates, or key material.

## Citation

CyberAutomationX. *SecureAzCloud Post-Quantum Migration Hub*, version 1.1.0, 2026-06-07.  
https://github.com/CyberAutomationX/Post-Quantum-Migration-Hub/releases/tag/v1.1.0
