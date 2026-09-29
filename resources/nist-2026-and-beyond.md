# SecureAzCloud NIST 2026 and Beyond Planning Guide

Author and maintainer: Ankit Gupta

Version: 2.0 | Reviewed: 2026-09-29 | Next planned review: 2026-12-29

## Authority and scope

This version was reviewed against published NIST sources available on 2026-09-29. It supports 2026 baseline work, 2027 execution, and later planning without claiming that future recommendations are already known. The controls and yearly targets below are hub-defined operationalizations, not NIST mandates or a certification checklist.

| Category | How to use it |
|---|---|
| Final standards and guidance | Apply the publication to its stated scope and your system obligations. FIPS 203/204/205 define algorithms; protocol compatibility and product readiness remain separate questions. |
| Draft publications | Track and assess proposed changes. IR 8547, SP 800-57 Part 1 Rev. 6, SP 800-131A Rev. 3, SP 800-82 Rev. 4, CSWP 48, SP 800-230, SP 800-133 Rev. 3, and preliminary SP 1800-38 remain drafts at this review. |
| Forecasts and candidates | HQC and Falcon/FN-DSA are under standardization; additional signatures are under evaluation. An expected 2027 HQC milestone is not a guarantee or current approval. |
| Hub planning controls | Risk scores, priority thresholds, annual phases, review cadence, worksheets, and acceptance criteria are local planning aids. Approve their use for your architecture and obligations. |

## Material 2026 source updates

| Source | Status and practical use |
|---|---|
| CSWP 39 Update 1 [N05] | Final, updated 2026-06-29. Use the corrected crypto-agility guidance for governance, discovery, negotiation, supply chains, and continuous improvement. |
| IR 8587 [N16] | Final 2026-09-15. Assess signed tokens/assertions and their issuers, verifiers, key lifecycle, and PQC interoperability constraints; Section 7.7 addresses PQC migration. |
| SP 800-228 Update 1 [N17] | Final update 2026-03-13. Include cloud-native API lifecycle risks and controls in dependency and migration planning. |
| SP 1339 [N15] | Final 2026-06-17. Attach OT backup/restore evidence to change and recovery plans. |
| SP 800-82 Rev. 4 [N14] | Initial public draft 2026-09-21. Monitor proposed changes while Rev. 3 [N13] remains the final OT baseline. |
| FIPS errata and module status [N01, N02, N24–N26] | Monitor FIPS 203/204 potential-errata notices, implementation updates, and the precise validation certificate/status of deployed cryptographic modules. |

## Transition dates: what 2030 and 2035 mean

IR 8547 [N06] is an initial public draft dated 2024-11-12. Its proposed tables distinguish classical public-key algorithms by security strength. The 112-bit rows propose deprecation after 2030 and disallowance after 2035; the 128-bit-and-higher rows propose disallowance after 2035 without the same 2030 deprecation entry. Do not summarize this as all RSA/ECC becoming deprecated in 2030.

These dates are draft transition proposals, not a universal legal deadline, a prediction of a cryptographically relevant quantum computer, or permission to defer high-risk work. Long confidentiality lifetimes, long verification lifetimes, supplier lead times, and applicable sector/federal policy can justify earlier migration. Record the exact source, status, scope, security strength, approved internal date, and review owner.

## Threat coverage and evidence

| Threat or failure scenario | Inventory focus | Planning response |
|---|---|---|
| Harvest now, decrypt later | Confidentiality lifetime; stored/transported sensitive data; public-key key establishment and wrapping; archives and backups. | Prioritize long-lived exposed data and supported migration paths; keep scenario assumptions explicit without inventing a quantum arrival date. |
| Future signature forgery and trust compromise | Certificate authorities, trust anchors, signed firmware/code, artifacts, long-lived assertions, and verification lifetime. | Map every verifier and recovery path; plan signature/trust migration independently from transport key establishment. |
| Downgrade and incomplete migration | Negotiated versus configured algorithms, fallback behavior, mixed clients, legacy exceptions, gateway boundaries. | Test negative negotiation and fallback cases; monitor actual use; govern exceptions and retire obsolete paths with evidence. |
| Implementation and key-management weaknesses | Library/provider/build, entropy source, key custody, input validation, key lifecycle, module scope. | Follow SP 800-227 [N04], supported implementations, relevant key management, patch/errata monitoring, and validation evidence. |
| Migration outage or resource exhaustion | Message/chain/token size, MTU, CPU/memory, timeouts, interoperability, failover, deterministic OT latency. | Use representative tests, measured limits, approved change windows, backup restoration, rollback and continuity gates. |
| Supplier and discovery gaps | Unsupported/embedded crypto, end-of-support dates, provider-managed services, unknown dependencies, stale discovery evidence. | Assign accountable owners, confirm supplier commitments, track unknowns and confidence, budget replacement and reassess continuously. |

## Minimum inventory model

For each asset and cryptographic component, record a stable ID, owner, business service, environment, criticality, confidentiality lifetime, signature-verification lifetime, crypto role, algorithm and parameter set, protocol/profile/version, key identifier and custody, certificate/trust references, library/provider/build, hardware/firmware, supplier/support window, observed versus configured state, discovery source/date/confidence, dependencies, target profile, migration lead time, evidence, exceptions, expiry, and next review. Store identifiers and evidence references, never private keys or raw credentials.

Separate ML-KEM key establishment from ML-DSA/SLH-DSA signatures. Symmetric ciphers, MACs, and hashes retain distinct roles; a strong data cipher does not remove a vulnerable public-key wrapping or key-establishment dependency. A protocol profile and product implementation must support the chosen construction. Do not invent hybrid combiners or infer end-to-end PQC from a gateway or hybrid TLS setting.

## Validation and deployment boundaries

Algorithm standardization, CAVP algorithm validation, CMVP module validation, and deployment correctness are separate [N24–N26]. Record certificate number and status, exact module and version, operating environment, approved mode, covered algorithms/services, and security-policy evidence. Validate protocol compatibility and the full deployment independently. A validated embedded module does not validate its enclosing product or protocol.

The CMVP FAQ records the FIPS 140-2 active-list transition after 2026-09-21. Check whether a certificate is active, historical, or revoked and whether its use is permitted for the specific deployment. Historical is not the same as revoked, and the transition does not establish a universal private-sector ban or prove that a product is insecure.

## Organization-defined forward plan

| Period | Planning focus | Exit evidence |
|---|---|---|
| 2026 baseline | Reconcile ownership, discovered crypto, data/trust lifetimes, source status, supplier roadmaps, threats and unknowns. | Inventory coverage/gaps, risk register, source-dated evidence, owners and approved priorities. |
| 2027 execution | Pilot supported high-risk migrations; verify identity/PKI interoperability; exercise OT restoration; embed agility in procurement. | Measured tests, end-to-end verifier support, rollout decision, rollback/recovery proof. |
| 2028–2030 scaling | Expand successful migrations; retire avoidable legacy dependencies; revisit draft 112-bit milestones against then-current final publications. | Observed deployment state, exception reduction, current policy decisions and supplier evidence. |
| 2031–2035 closure | Resolve remaining long-lived and supplier-limited dependencies early enough for applicable final requirements. | Funded replacement, approved/expiring exceptions, closure and legacy-retirement evidence. |
| 2036 and later | Maintain discovery, emergency substitution, library/module status, algorithm/errata monitoring, and long-term verification obligations. | Recurring and event-triggered reassessment, refreshed test suites, updated inventory and decisions. |

The periods above structure work; they are not NIST-imposed universal deadlines. Adjust the sequence to applicable requirements, exposure, system lifecycle, safety, supplier readiness, and business continuity. Do not mark a task complete solely because a vendor advertises PQC support.

## Review process that keeps the hub current

- Assign a standards owner and source review date. Review quarterly; next planned review is 2026-12-29. This cadence is a hub recommendation.
- Reassess sooner for a final standard or draft update, erratum, credible cryptanalytic result, protocol/profile change, supplier release, CMVP status change, incident, or major architecture change.
- Record the prior and new source status, affected assets/controls, gap decision, owner, due date, evidence, and approval. Draft-to-final changes require an explicit applicability review.
- Refresh inventory and supplier evidence; rerun affected interoperability, negative, performance, rollover, rollback, and recovery tests.
- Publish versioned artifacts, source mappings, release notes and validation results; keep prior releases clearly historical.

## Sources

| ID | Publication and purpose | Status at review | Official source |
|---|---|---|---|
| N01 | FIPS 203 ML-KEM; key establishment, parameter sets 512/768/1024; monitor potential errata | Final 2024-08-13; notice 2025-11-17 | [NIST](https://csrc.nist.gov/pubs/fips/203/final) |
| N02 | FIPS 204 ML-DSA; signature generation and verification; monitor potential errata | Final 2024-08-13; notice 2026-07-31 | [NIST](https://csrc.nist.gov/pubs/fips/204/final) |
| N03 | FIPS 205 SLH-DSA; stateless hash-based signatures | Final 2024-08-13 | [NIST](https://csrc.nist.gov/pubs/fips/205/final) |
| N04 | SP 800-227; conforming KEM implementation, randomness, input validation, key destruction, authentication, key derivation/confirmation and multi-algorithm construction | Final 2025-09-18 | [NIST](https://csrc.nist.gov/pubs/sp/800/227/final) |
| N05 | CSWP 39-upd1; governance, inventory, risk-prioritized agility, negotiation, supply chains, APIs, continuous improvement | Final 2025-12-19; updated 2026-06-29 | [NIST](https://csrc.nist.gov/pubs/cswp/39/upd1/considerations-for-achieving-crypto-agility/final) |
| N06 | IR 8547; HNDL, signature and code-verification distinctions, draft transition tables | Initial public draft 2024-11-12 | [NIST](https://csrc.nist.gov/pubs/ir/8547/ipd) |
| N07 | NCCoE Migration to PQC; discovery/inventory and interoperability workstreams; evolving output model | Active project; preliminary documents | [NIST](https://www.nccoe.nist.gov/applied-cryptography/migration-to-pqc) |
| N08 | SP 1800-38 B/C; discovery and interoperability/performance demonstration | Initial preliminary draft 2023-12-19 | [NIST](https://csrc.nist.gov/pubs/sp/1800/38/iprd-(1)) |
| N09 | SP 800-57 Part 1 Rev. 5; key management baseline | Final 2020-05-04 | [NIST](https://csrc.nist.gov/pubs/sp/800/57/pt1/r5/final) |
| N10 | SP 800-57 Part 1 Rev. 6; PQC-aware key management and storage proposals | Initial public draft 2025-12-05 | [NIST](https://csrc.nist.gov/pubs/sp/800/57/pt1/r6/ipd) |
| N11 | SP 800-131A Rev. 2; current final algorithm transition baseline | Final 2019-03-21 | [NIST](https://csrc.nist.gov/pubs/sp/800/131/a/r2/final) |
| N12 | SP 800-131A Rev. 3; proposed algorithm/key-strength transitions | Initial public draft 2024-10-21 | [NIST](https://csrc.nist.gov/pubs/sp/800/131/a/r3/ipd) |
| N13 | SP 800-82 Rev. 3; OT performance, reliability, safety and controls | Final 2023-09-28 | [NIST](https://csrc.nist.gov/pubs/sp/800/82/r3/final) |
| N14 | SP 800-82 Rev. 4; CSF2 alignment, asset management, monitoring, OT/IIoT/cloud, system-management security | Initial public draft 2026-09-21 | [NIST](https://csrc.nist.gov/pubs/sp/800/82/r4/ipd) |
| N15 | SP 1339; backups in OT change and recovery practice | Final 2026-06-17 | [NIST](https://csrc.nist.gov/pubs/sp/1339/final) |
| N16 | IR 8587; signed tokens/assertions, key lifecycle, verification, automated workload identity token use, Section 7.7 PQC interoperability constraints | Final 2026-09-15 | [NIST](https://csrc.nist.gov/pubs/ir/8587/final) |
| N17 | SP 800-228-upd1; API lifecycle risks and controls | Final; original 2025-06-27, updated 2026-03-13 | [NIST](https://csrc.nist.gov/pubs/sp/800/228/upd1/final) |
| N18 | CSWP 48; mapping PQC discovery and interoperability capabilities to risk frameworks | Initial public draft 2025-09-18 | [NIST](https://csrc.nist.gov/pubs/cswp/48/mapping-migration-to-pqc-project-capabilities-to-r/ipd) |
| N19 | NIST PQC project; current standardized/selected algorithm status | Project updated 2026-08-05 | [NIST](https://csrc.nist.gov/projects/post-quantum-cryptography) |
| N20 | HQC selection announcement; diversification backup, continue current migration, expected 2027 finalization | Selection announcement 2025-03-11, forecast not approval | [NIST](https://www.nist.gov/news-events/news/2025/03/nist-selects-hqc-fifth-algorithm-post-quantum-encryption) |
| N21 | Additional digital signature schemes; Round3 announced May14,2026 | Evaluation candidates, not standards | [NIST](https://csrc.nist.gov/projects/pqc-dig-sig) |
| N22 | SP 800-204A; service-mesh security architecture | Final 2020-05-27 | [NIST](https://csrc.nist.gov/pubs/sp/800/204/a/final) |
| N23 | SP 800-204B; service-mesh authentication/authorization | Final 2021-08 | [NIST](https://csrc.nist.gov/pubs/sp/800/204/b/final) |
| N24 | CAVP program; algorithm validation is prerequisite to, not replacement for, module validation | Official program; updated 2026-09-22 | [NIST](https://csrc.nist.gov/projects/cryptographic-algorithm-validation-program) |
| N25 | CMVP FAQ; module/version/operating-environment verification, protocol/product validation boundary, FIPS140-2 active-list transition | Official FAQ checked 2026-09-29 | [NIST](https://csrc.nist.gov/Projects/cryptographic-module-validation-program/faqs) |
| N26 | CMVP validated modules; inspect certificate/security policy and active/historical/revoked status | Live certificate registry checked 2026-09-29 | [NIST](https://csrc.nist.gov/projects/cryptographic-module-validation-program/validated-modules) |
| N27 | CSWP 29 / CSF 2.0; cybersecurity outcome framework, not a prescriptive PQC implementation standard | Final 2024-02-26 | [NIST](https://csrc.nist.gov/pubs/cswp/29/the-nist-cybersecurity-framework-csf-20/final) |
| N28 | SP 800-53 Rev. 5; current control catalog is Release 5.2.0 referenced by publication-page planning note | Final; base 2020-09/update 2020-12-10; minor Release 5.2.0 finalized 2025-08-27 | [NIST](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) |
| N29 | SP 800-161 Rev. 1-upd1; supplier risk and dependency governance | Final; original 2022-05, update 2024-11-01 | [NIST](https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final) |
| N30 | SP 800-230; additional limited-signature SLH-DSA parameter sets, software/firmware/certificate watch item | Initial public draft 2026-04-13 | [NIST](https://csrc.nist.gov/pubs/sp/800/230/ipd) |
| N31 | SP 800-133 Rev. 3; proposed PQC key generation, seed expansion, KEM and HSM considerations | Initial public draft 2026-04-17 | [NIST](https://csrc.nist.gov/pubs/sp/800/133/r3/ipd) |

Independent vendor-neutral planning aid. No agency endorsement, certification, or compliance determination is claimed.
