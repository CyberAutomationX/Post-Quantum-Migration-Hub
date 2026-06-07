# SecureAzCloud SCADA/ICS PQC Readiness Checklist

Version: 1.0  
Release date: 2026-06-07

This checklist supports safety-first planning for PQC readiness in SCADA, ICS, and broader operational technology environments.

**Safety-first rule:** do not introduce new cryptographic settings, certificates, firmware, protocol changes, or active scans into production OT without approved management of change, vendor validation, rollback planning, and an operations-approved maintenance window.

## Checklist

| Area | Checklist item | Safety / operational consideration | Evidence |
|---|---|---|---|
| Governance | Create OT-specific PQC change governance. | No production change without safety impact assessment, vendor support, MOC approval, rollback plan, and maintenance window. | MOC procedure; safety approval; rollback checklist. |
| Inventory | Discover OT cryptography safely. | Prefer passive discovery, configuration review, certificate export, vendor documentation, and engineering workstation review before any active scanning. | OT crypto inventory; discovery method log. |
| Criticality | Classify assets by process and safety impact. | Prioritize by process function, downtime tolerance, safety consequence, vendor support, data sensitivity, and remote exposure. | Criticality and safety-impact matrix. |
| Remote access | Map encrypted remote access paths. | Document VPN, jump hosts, privileged access, vendor access, cloud connectors, modems, bastions, and MFA dependencies. | Remote access architecture map. |
| Industrial protocols | Review protocol security capabilities. | Identify where TLS, certificates, signed firmware, secure boot, or application-layer security are enabled, unsupported, or vendor-dependent. | Protocol and device security matrix. |
| PKI | Map OT certificates and trust stores. | Include historians, HMIs, engineering workstations, OPC UA, gateways, web interfaces, remote access systems, and device certificates. | Certificate and trust-store inventory. |
| Suppliers | Request OT supplier PQC roadmaps. | Confirm firmware/software upgrade paths, key/certificate size limits, protocol support, validation process, and support windows. | Supplier response tracker. |
| Testing | Use lab or representative test environment. | Never test unvalidated cryptographic changes directly on production control systems. | Lab plan; test assets; acceptance criteria. |
| Performance | Validate constrained-device impact. | Measure latency, CPU/memory, packet size, fragmentation, session recovery, and failure behavior. | Performance baseline and test results. |
| Compensating controls | Plan for non-upgradeable assets. | Use segmentation, strict remote access, jump hosts, monitoring, controlled conduits, lifecycle replacement, and time-bound risk acceptance. | Compensating control plan. |
| Operations | Update monitoring and incident response. | Ensure changed certificates/protocols are visible in OT monitoring and runbooks; conduct tabletop exercises. | Runbooks; alert rules; tabletop results. |
| Lifecycle | Link PQC readiness to capital planning. | Replace non-agile devices and unsupported appliances during scheduled lifecycle refresh. | Lifecycle roadmap and capital plan. |

## Required safety gates before production change

1. Process owner, asset owner, and safety owner approve the scope.
2. Vendor confirms supportability and known constraints.
3. Representative lab or non-production validation is complete.
4. Backup, rollback, and manual operations procedures are documented.
5. Maintenance window and operational communications are approved.
6. Monitoring and incident response runbooks are updated before deployment.

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
