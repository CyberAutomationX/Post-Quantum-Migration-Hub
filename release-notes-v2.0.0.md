# Release Notes - v2.0.0

Author and maintainer: Ankit Gupta

Release date: 2026-09-29  
Workbook version: 2.0  
NIST source review: 2026-09-29

## Scope

Refreshes all four Excel workbooks and their current CSV/PDF companions, landing/download links, HTML/Markdown guides, and machine-readable source maps for a 2026 evidence baseline and organization-defined 2027 and later planning.

## Updated Downloads

| Artifact | Current workbook |
|---|---|
| Cryptographic Inventory Template | [v2.0 XLSX](downloads/secureazcloud-pqc-crypto-inventory-template-v2.0.xlsx) |
| Crypto-Agility Assessment Template | [v2.0 XLSX](downloads/secureazcloud-crypto-agility-assessment-template-v2.0.xlsx) |
| PQC Cloud and Workload Identity Migration Checklist | [v2.0 XLSX](downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0.xlsx) |
| SCADA/ICS PQC Migration Continuity Checklist | [v2.0 XLSX](downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0.xlsx) |

The [README](README.md) links every current workbook, CSV, and PDF. Historical workbook content is preserved; attribution metadata has been standardized to Ankit Gupta. Existing completed assessments require a reviewed field-to-field transfer into the new schema; do not paste by column position or overwrite formula cells.

## Coverage Added or Expanded

- Cryptographic role, algorithm/parameter set, protocol/library/provider, data confidentiality lifetime, signature-verification lifetime, owner, discovery evidence, confidence, dependencies, suppliers, and lifecycle constraints.
- Threat separation for harvest-now-decrypt-later, durable signature/trust compromise, downgrade, implementation weaknesses, supplier gaps, and migration outages.
- Crypto-agility governance, controlled replacement, KEM use, validation evidence, interoperability, negative testing, rollback, and exceptions.
- Cloud tokens/assertions, issuer-to-verifier dependencies, transport/signature separation, workload identity, APIs, service mesh, key rollover, and provider boundaries.
- OT/ICS firmware and trust lifetimes, constrained resources, latency/failover, backups, restoration, safety gates, maintenance windows, and replacement planning.
- Organization-defined phases for 2026, 2027, 2028–2030, 2031–2035, and 2036 and later, plus a documented standards-review process.

## Standards Corrections and Currency

- Replaces the original CSWP 39 reference with final CSWP 39 Update 1, updated 2026-06-29.
- Adds final SP 800-227, IR 8587, SP 800-228 Update 1, and SP 1339 where relevant.
- Keeps final SP 800-82 Rev. 3 as the OT baseline while clearly identifying Rev. 4 as the 2026-09-21 initial public draft.
- Labels IR 8547, SP 800-57 Part 1 Rev. 6, SP 800-131A Rev. 3, SP 1800-38, CSWP 48, SP 800-230, and SP 800-133 Rev. 3 as drafts.
- Clarifies the IR 8547 draft distinction: proposed deprecation after 2030 applies to its 112-bit classical public-key rows; 128-bit-and-higher rows do not have the same 2030 deprecation entry. Proposed disallowance after 2035 is not presented as a universal legal deadline.
- Tracks FIPS potential errata, HQC/Falcon standardization, signature candidates, and validation-status changes without presenting candidates or forecasts as approved standards.
- Separates algorithm validation, module validation, and actual deployment assurance.

## Related Files

- [NIST 2026 and Beyond Planning Guide](resources/nist-2026-and-beyond.html)
- [NIST Source Status Register](resources/reference-map.html)
- [Artifact Crosswalk](resources/source-map-addendum.html)
- [Final Update Report](FINAL-REPORT-v2.0.0.md)
- [Validation Report](VALIDATION-REPORT.md)

## Limits and Maintenance

This is an independent, vendor-neutral planning aid. Default scoring, priority thresholds, annual phases, and review cadence are hub-defined, not NIST certification criteria. Future unpublished guidance is not assumed to be covered. Review quarterly and when standards, errata, threats, protocols, suppliers, or validation status change; next planned review: 2026-12-29. No automated monitoring service is claimed.
