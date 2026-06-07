# SecureAzCloud Cloud/IAM PQC Migration Playbook

Version: 1.0  
Release date: 2026-06-07

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

## Sources

- NIST FIPS 203 — Module-Lattice-Based Key-Encapsulation Mechanism Standard (ML-KEM): https://csrc.nist.gov/pubs/fips/203/final
- NIST FIPS 204 — Module-Lattice-Based Digital Signature Standard (ML-DSA): https://csrc.nist.gov/pubs/fips/204/final
- NIST FIPS 205 — Stateless Hash-Based Digital Signature Standard (SLH-DSA): https://csrc.nist.gov/pubs/fips/205/final
- NIST PQC Standardization Project: https://csrc.nist.gov/projects/post-quantum-cryptography/post-quantum-cryptography-standardization
- NIST NCCoE Migration to Post-Quantum Cryptography: https://www.nccoe.nist.gov/applied-cryptography/migration-to-pqc
- NIST CSWP 39 — Considerations for Achieving Crypto Agility: https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.39.pdf
- NIST Cybersecurity Framework 2.0 announcement and resources: https://www.nist.gov/news-events/news/2024/02/nist-releases-version-20-landmark-cybersecurity-framework
- NIST SP 800-53 Rev. 5 — Security and Privacy Controls: https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final
- NIST SP 800-82 Rev. 3 — Guide to Operational Technology Security: https://csrc.nist.gov/pubs/sp/800/82/r3/final
- NIST SP 800-161 Rev. 1 Update 1 — Cybersecurity Supply Chain Risk Management: https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final
- CISA — Quantum-Readiness: Migration to Post-Quantum Cryptography: https://www.cisa.gov/resources-tools/resources/quantum-readiness-migration-post-quantum-cryptography
- CISA — Post-Quantum Considerations for Operational Technology: https://www.cisa.gov/resources-tools/resources/post-quantum-considerations-operational-technology
- CISA — Product Categories for Technologies that Use PQC Standards: https://www.cisa.gov/resources-tools/resources/product-categories-technologies-use-post-quantum-cryptography-standards
