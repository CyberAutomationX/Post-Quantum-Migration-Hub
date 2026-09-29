# SecureAzCloud PQC Readiness Checklist

Author and maintainer: Ankit Gupta

Version: 2.0  
Release date: 2026-09-29

Use this checklist to determine whether an organization is ready to plan, pilot, and govern a post-quantum cryptography migration.

## Checklist

| Domain | Checklist item | Acceptance criteria | Evidence |
|---|---|---|---|
| Governance | Accountable owner and working group are assigned. | Named owner, RACI, cadence, and decision log exist. | Program charter; RACI; meeting notes. |
| Governance | Crypto-agility policy is published. | Policy requires configurable algorithms, approved cryptographic libraries, migration-friendly architectures, and exception handling. | Policy document; architecture standard. |
| Inventory | Cryptographic inventory is established. | Inventory captures applications, certificates, protocols, libraries, services, devices, identities, signing keys, HSM/KMS, and suppliers. | Completed inventory template with evidence links. |
| Inventory | Unknown cryptography is tracked as discovery debt. | Assets with missing algorithm, library, certificate, or supplier information have owners and due dates. | Discovery debt register. |
| Data risk | Long-life sensitive data is prioritized. | Data shelf life, sensitivity, regulatory requirements, and store-now/decrypt-later exposure are recorded. | Data classification and retention mapping. |
| Architecture | Crypto agility is classified for every priority asset. | Hard-coded algorithms, fixed certificate profiles, non-upgradeable libraries, and protocol constraints are documented. | Crypto agility field in inventory. |
| PKI | Certificate authority and trust-store readiness is assessed. | CA profiles, trust anchors, renewal automation, revocation, relying-party compatibility, and chain-size impact are understood. | PKI assessment and certificate profile matrix. |
| Cloud/IAM | Identity and federation crypto dependencies are mapped. | SAML, OIDC/OAuth, JWT, workload identity, mTLS, SSH, service identity, and signing paths are documented. | Cloud/IAM dependency map. |
| Network | Transport crypto is mapped. | TLS, VPN, SSH, remote access, service mesh, API gateway, and database driver dependencies are documented. | Network crypto inventory. |
| Suppliers | Critical supplier PQC roadmaps are requested. | Vendors disclose PQC support, upgrade path, cryptographic dependencies, update mechanism, and product support windows. | Supplier responses and contract language. |
| Testing | Interoperability and performance testing is planned. | Tests include handshake behavior, certificate/signature size, latency, fragmentation, logs, client compatibility, and rollback. | Test plan and pilot report. |
| Operations | Monitoring and runbooks are updated. | New protocols, certificates, signing changes, exceptions, and rollback paths are visible to operations teams. | SOC rules; runbooks; change records. |

## Minimum evidence package

- Cryptographic inventory export for priority assets.
- Risk scoring method and prioritized backlog.
- PQC migration owner, RACI, and decision log.
- PKI, IAM, cloud, application, network, and OT/ICS dependency maps.
- Supplier roadmap and support-window tracker.
- Non-production pilot test plan and results.
- Exception register with compensating controls and expiration dates.

## 2026 and later readiness controls

| Focus | Planning control | Evidence |
|---|---|---|
| Source authority | Record publication ID, status, reviewed date, applicable scope, and source URL. Draft proposals do not become organizational mandates automatically. | Source register and approved policy decision. |
| Threat model | Separate harvest-now-decrypt-later confidentiality from future signature forgery, trust-root compromise, implementation weaknesses, downgrade, and migration outage. | Threat scenario, affected asset, owner, evidence, and treatment. |
| Inventory quality | Capture algorithm role and parameter set, key lifetime, sensitive-data lifetime, signing verification lifetime, library/build version, module validation, discovery provenance, confidence, and last-seen date. | Asset-to-protocol-to-provider-to-supplier dependency graph; unknowns assigned owners. |
| PQC roles | Use ML-KEM for key establishment planning and ML-DSA/SLH-DSA for signatures. Retain suitable symmetric encryption, MAC, and hash controls; PQC is not a direct replacement for AES. | Use-case-specific architecture and product/protocol support evidence. |
| Migration safety | Test downgrade resistance, invalid input, certificate/token size, memory, CPU, interoperability, rollback, and telemetry. Separate algorithm validation from module validation and deployment assurance. | Approved acceptance criteria and actual test results. |
| Planning horizon | Set organization-approved 2026 baseline and 2027 pilot/rollout targets. Track later replacement windows and changing draft transition milestones. | Budgeted roadmap with owner, dependencies, exit criteria, and exception expiry. |

**Source review:** 2026-09-29. Final sources, drafts, and hub-defined targets have different authority. See the [2026 and beyond guide](nist-2026-and-beyond.md) and [source status register](reference-map.html). Future recommendations cannot be known in advance. Review quarterly and on standards, protocol, errata, supplier, or threat changes; next planned review: 2026-12-29.

Default scoring and completion bands are hub-defined planning heuristics, not NIST scoring or certification criteria. Record exclusions and rationale; completion is not cryptographic assurance.

## Sources

Sources reviewed 2026-09-29. See the [full register](reference-map.html) for status and scope.

| ID | Source | Status |
|---|---|---|
| N01 | [FIPS 203 ML-KEM; key establishment, parameter sets 512/768/1024; monitor potential errata](https://csrc.nist.gov/pubs/fips/203/final) | Final 2024-08-13; notice 2025-11-17 |
| N02 | [FIPS 204 ML-DSA; signature generation and verification; monitor potential errata](https://csrc.nist.gov/pubs/fips/204/final) | Final 2024-08-13; notice 2026-07-31 |
| N03 | [FIPS 205 SLH-DSA; stateless hash-based signatures](https://csrc.nist.gov/pubs/fips/205/final) | Final 2024-08-13 |
| N04 | [SP 800-227; conforming KEM implementation, randomness, input validation, key destruction, authentication, key derivation/confirmation and multi-algorithm construction](https://csrc.nist.gov/pubs/sp/800/227/final) | Final 2025-09-18 |
| N05 | [CSWP 39-upd1; governance, inventory, risk-prioritized agility, negotiation, supply chains, APIs, continuous improvement](https://csrc.nist.gov/pubs/cswp/39/upd1/considerations-for-achieving-crypto-agility/final) | Final 2025-12-19; updated 2026-06-29 |
| N06 | [IR 8547; HNDL, signature and code-verification distinctions, draft transition tables](https://csrc.nist.gov/pubs/ir/8547/ipd) | Initial public draft 2024-11-12 |
| N07 | [NCCoE Migration to PQC; discovery/inventory and interoperability workstreams; evolving output model](https://www.nccoe.nist.gov/applied-cryptography/migration-to-pqc) | Active project; preliminary documents |
| N09 | [SP 800-57 Part 1 Rev. 5; key management baseline](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) | Final 2020-05-04 |
| N11 | [SP 800-131A Rev. 2; current final algorithm transition baseline](https://csrc.nist.gov/pubs/sp/800/131/a/r2/final) | Final 2019-03-21 |
| N19 | [NIST PQC project; current standardized/selected algorithm status](https://csrc.nist.gov/projects/post-quantum-cryptography) | Project updated 2026-08-05 |
| N24 | [CAVP program; algorithm validation is prerequisite to, not replacement for, module validation](https://csrc.nist.gov/projects/cryptographic-algorithm-validation-program) | Official program; updated 2026-09-22 |
| N25 | [CMVP FAQ; module/version/operating-environment verification, protocol/product validation boundary, FIPS140-2 active-list transition](https://csrc.nist.gov/Projects/cryptographic-module-validation-program/faqs) | Official FAQ checked 2026-09-29 |
| N26 | [CMVP validated modules; inspect certificate/security policy and active/historical/revoked status](https://csrc.nist.gov/projects/cryptographic-module-validation-program/validated-modules) | Live certificate registry checked 2026-09-29 |
| N27 | [CSWP 29 / CSF 2.0; cybersecurity outcome framework, not a prescriptive PQC implementation standard](https://csrc.nist.gov/pubs/cswp/29/the-nist-cybersecurity-framework-csf-20/final) | Final 2024-02-26 |
| N28 | [SP 800-53 Rev. 5; current control catalog is Release 5.2.0 referenced by publication-page planning note](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) | Final; base 2020-09/update 2020-12-10; minor Release 5.2.0 finalized 2025-08-27 |
| N29 | [SP 800-161 Rev. 1-upd1; supplier risk and dependency governance](https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final) | Final; original 2022-05, update 2024-11-01 |

Independent planning aid; not a NIST publication or endorsement.
