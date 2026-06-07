# SecureAzCloud PQC Readiness Checklist

Version: 1.0  
Release date: 2026-06-07

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
