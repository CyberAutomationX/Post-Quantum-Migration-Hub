# SecureAzCloud Cloud/IAM PQC Migration Playbook

Author and maintainer: Ankit Gupta

Version: 2.0  
Release date: 2026-09-29

This playbook helps cloud, IAM, application, and security teams convert PQC readiness into a controlled migration program.

## Cryptographic touchpoints

| Area | Examples to inventory |
|---|---|
| TLS/mTLS | Ingress, egress, service mesh, API gateways, load balancers, database connections, partner endpoints. |
| Federation | SAML signing/encryption certificates, OIDC/OAuth token signing algorithms, JWT key rotation, partner metadata. |
| Workload identity | Service accounts, managed identities, SPIFFE/SPIRE-style identities, machine certificates, short-lived credentials. |
| Remote access | VPN, SSH, privileged access gateways, bastion hosts, jump servers, break-glass paths. |
| Signing | Code signing, container signing, artifact signing, firmware signing, secure boot, release pipelines. |
| Key management | KMS, HSM, certificate authorities, secrets stores, trust stores, BYOK/HYOK processes, key rotation workflows. |
| Applications | Cryptographic libraries, protocol negotiation, hard-coded algorithms, SDK/client library behavior, dependency update paths. |

## Phases

| Phase | Activity | Detailed action | Output |
|---|---|---|---|
| 0. Mobilize | Define scope and governance | Confirm cloud, IAM, PKI, signing, service identity, API, network, and supplier scope. Assign an owner, RACI, and review cadence. | Approved scope, RACI, and timeline. |
| 1. Discover | Inventory crypto touchpoints | Collect certificates, TLS endpoints, federation metadata, token signing keys, workload identities, SSH keys, VPN profiles, code signing keys, KMS/HSM integrations, service mesh settings, and CI/CD dependencies. | Cloud/IAM crypto dependency map. |
| 2. Prioritize | Score risk and blockers | Score by quantum vulnerability, data shelf life, criticality, exposure, crypto agility, supplier support, and operational complexity. | Prioritized migration backlog. |
| 3. Design | Define target migration patterns | Use approved libraries, certificate lifecycle automation, policy-managed algorithms, protocol upgrades, hardware refresh, supplier upgrades, or compensating controls. Use PQC or hybrid-capable paths only where protocols and products support them. | Target-state architecture and standards. |
| 4. Pilot | Validate in non-production | Test representative TLS, mTLS, federation, signing, workload identity, API gateway, service mesh, and monitoring flows. Verify latency, certificate size, client compatibility, logs, and rollback. | Pilot report and go/no-go decision. |
| 5. Rollout | Execute phased deployment | Use canaries, maintenance windows, partner notifications, automated checks, and rollback triggers. Keep changes reversible until compatibility is proven. | Change records and deployment evidence. |
| 6. Operate | Make discovery continuous | Refresh crypto inventory using certificates, endpoints, code repositories, dependencies, SBOM/CBOM where available, CI/CD, and network telemetry. | Recurring inventory dashboard and exception review. |

## Target design principles

- Use policy-managed cryptographic settings rather than hard-coded algorithms.
- Centralize certificate lifecycle management.
- Abstract cryptographic libraries behind supported interfaces.
- Validate PQC or hybrid-capable configurations only where protocol, product, client, and partner support is mature enough for the use case.
- Maintain backward-compatible rollout and rollback paths.
- Require supplier disclosures for cryptographic dependencies, update mechanisms, support windows, and PQC roadmaps.

## Cloud and identity controls for 2026 and later

| Focus | Planning control | Evidence |
|---|---|---|
| Separate trust layers | Inventory TLS key establishment, TLS authentication, token/assertion signatures, encryption/key wrapping, workload credentials, and artifact signatures independently. A PQC TLS handshake does not prove token-signing migration. | Layered dependency map and algorithm-role inventory. |
| Tokens and assertions | Apply final NIST IR 8587 considerations to long-lived assertions, federation metadata, signed credentials, verification lifetime, issuer/verifier support, and key rollover. Short-lived tokens still depend on long-lived trust infrastructure. | Issuer-to-verifier map, protocol profile status, lifetime/risk assessment. |
| Protocol readiness | Record the specific protocol/profile revision and status, client/server support, certificate/key formats, and provider release. Do not infer protocol support from an algorithm standard. | Supported version matrix and partner acceptance evidence. |
| Service control boundaries | For SaaS, KMS/HSM, managed identities, federation, and cloud services, distinguish customer-controlled settings from provider-managed cryptography. | Supplier roadmap, responsibility owner, supported configuration, validation evidence. |
| Pilot failure paths | Test negotiation downgrade, malformed keys/signatures/ciphertexts, unknown key IDs, token/chain size limits, JWKS caching, mixed-version peers, rollover, revocation, and disaster recovery. | Pass/fail criteria, metrics, logs, rollback drill, accountable approval. |
| 2027 and later operations | Stage supported migrations by risk; track negotiated algorithms, signing/verifier drift, dependencies, outages, and exception expiry. Retire legacy use only after all relying parties and recovery paths are verified. | Continuous discovery and migration evidence dashboard. |

**Source review:** 2026-09-29. Final sources, drafts, and hub-defined targets have different authority. See the [2026 and beyond guide](nist-2026-and-beyond.md) and [source status register](reference-map.html). Future recommendations cannot be known in advance. Review quarterly and on standards, protocol, errata, supplier, or threat changes; next planned review: 2026-12-29.

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
| N16 | [IR 8587; signed tokens/assertions, key lifecycle, verification, automated workload identity token use, Section 7.7 PQC interoperability constraints](https://csrc.nist.gov/pubs/ir/8587/final) | Final 2026-09-15 |
| N17 | [SP 800-228-upd1; API lifecycle risks and controls](https://csrc.nist.gov/pubs/sp/800/228/upd1/final) | Final; original 2025-06-27, updated 2026-03-13 |
| N22 | [SP 800-204A; service-mesh security architecture](https://csrc.nist.gov/pubs/sp/800/204/a/final) | Final 2020-05-27 |
| N23 | [SP 800-204B; service-mesh authentication/authorization](https://csrc.nist.gov/pubs/sp/800/204/b/final) | Final 2021-08 |
| N24 | [CAVP program; algorithm validation is prerequisite to, not replacement for, module validation](https://csrc.nist.gov/projects/cryptographic-algorithm-validation-program) | Official program; updated 2026-09-22 |
| N25 | [CMVP FAQ; module/version/operating-environment verification, protocol/product validation boundary, FIPS140-2 active-list transition](https://csrc.nist.gov/Projects/cryptographic-module-validation-program/faqs) | Official FAQ checked 2026-09-29 |
| N26 | [CMVP validated modules; inspect certificate/security policy and active/historical/revoked status](https://csrc.nist.gov/projects/cryptographic-module-validation-program/validated-modules) | Live certificate registry checked 2026-09-29 |

Independent planning aid; not a NIST publication or endorsement.
