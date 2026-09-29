# SecureAzCloud SCADA/ICS PQC Readiness Checklist

Author and maintainer: Ankit Gupta

Version: 2.0  
Release date: 2026-09-29

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

## OT continuity controls for 2026 and later

| Focus | Planning control | Evidence |
|---|---|---|
| Publication status | Use SP 800-82 Rev. 3 as the final baseline; track Rev. 4 as an initial public draft as of this review. Do not treat the draft as a mandatory replacement. | Standards watch item, gap assessment, review owner. |
| Long device and signature lifetimes | Inventory secure boot, firmware verification, trust-anchor updateability, recovery images, engineering tools, offline devices, and hardware lifecycles. | Vendor-confirmed key/signature-size limits and supported update path. |
| Passive evidence first | Record discovery method and confidence. Avoid active probing that may disrupt deterministic control or safety systems. | Passive discovery/configuration review and engineering-approved test method. |
| Real-time validation | Test worst-case latency, jitter, packet loss, fragmentation, retransmission, reconnect storms, CPU/memory, failover, and watchdog/safety behavior. | Engineering-approved limits and representative lab results. |
| Gateway boundaries | Record which link a PQC-capable gateway protects and where plaintext or classical cryptography remains. Segmentation and gateways do not provide end-to-end PQC automatically. | Conduit diagram and documented residual risk. |
| Change and recovery | Require safety/operations approval, vendor support, maintenance window, backup restoration, rollback, monitoring, and time-limited legacy exception. | MOC record, rollback drill, outage/fail-safe criteria, funded replacement plan. |

**Source review:** 2026-09-29. Final sources, drafts, and hub-defined targets have different authority. See the [2026 and beyond guide](nist-2026-and-beyond.md) and [source status register](reference-map.html). Future recommendations cannot be known in advance. Review quarterly and on standards, protocol, errata, supplier, or threat changes; next planned review: 2026-12-29.

## Sources

Sources reviewed 2026-09-29. See the [full register](reference-map.html) for status and scope.

| ID | Source | Status |
|---|---|---|
| N01 | [FIPS 203 ML-KEM; key establishment, parameter sets 512/768/1024; monitor potential errata](https://csrc.nist.gov/pubs/fips/203/final) | Final 2024-08-13; notice 2025-11-17 |
| N02 | [FIPS 204 ML-DSA; signature generation and verification; monitor potential errata](https://csrc.nist.gov/pubs/fips/204/final) | Final 2024-08-13; notice 2026-07-31 |
| N03 | [FIPS 205 SLH-DSA; stateless hash-based signatures](https://csrc.nist.gov/pubs/fips/205/final) | Final 2024-08-13 |
| N05 | [CSWP 39-upd1; governance, inventory, risk-prioritized agility, negotiation, supply chains, APIs, continuous improvement](https://csrc.nist.gov/pubs/cswp/39/upd1/considerations-for-achieving-crypto-agility/final) | Final 2025-12-19; updated 2026-06-29 |
| N06 | [IR 8547; HNDL, signature and code-verification distinctions, draft transition tables](https://csrc.nist.gov/pubs/ir/8547/ipd) | Initial public draft 2024-11-12 |
| N13 | [SP 800-82 Rev. 3; OT performance, reliability, safety and controls](https://csrc.nist.gov/pubs/sp/800/82/r3/final) | Final 2023-09-28 |
| N14 | [SP 800-82 Rev. 4; CSF2 alignment, asset management, monitoring, OT/IIoT/cloud, system-management security](https://csrc.nist.gov/pubs/sp/800/82/r4/ipd) | Initial public draft 2026-09-21 |
| N15 | [SP 1339; backups in OT change and recovery practice](https://csrc.nist.gov/pubs/sp/1339/final) | Final 2026-06-17 |
| N29 | [SP 800-161 Rev. 1-upd1; supplier risk and dependency governance](https://csrc.nist.gov/pubs/sp/800/161/r1/upd1/final) | Final; original 2022-05, update 2024-11-01 |
| N30 | [SP 800-230; additional limited-signature SLH-DSA parameter sets, software/firmware/certificate watch item](https://csrc.nist.gov/pubs/sp/800/230/ipd) | Initial public draft 2026-04-13 |

Independent planning aid; not a NIST publication or endorsement.
