# Publishing Guide — SecureAzCloud PQC Migration Resource Hub

Author and maintainer: Ankit Gupta

Repository version: 2.0.0  
Workbook version: 2.0  
Source review and release date: 2026-09-29

## Static Publication

1. Publish the repository's static content, keeping `index.html`, `assets/`, `resources/`, and `downloads/` in their relative locations.
2. Preserve historical workbook content and existing links; attribution metadata is standardized to Ankit Gupta. Current landing pages and source-map JSON must point to the `-v2.0` filenames.
3. Confirm all four current XLSX files, their CSV/PDF companions, the guide pages, source maps, reports, license, and release notes resolve.
4. Check the root landing page and resource pages at desktop and mobile widths. Confirm navigation, downloads, source links, source status, and version/date labels.
5. Open the workbooks in a compatible spreadsheet application; check dropdowns, formulas, examples, blank rows, instructions, and export consistency. Record what was actually tested in `VALIDATION-REPORT.md`.
6. Record repository commit, publication URL, version, and date in the final release report. Do not claim the site is deployed or a GitHub Release exists until verified.

## Current File Set

All current XLSX, CSV, and PDF companions use these bases with the relevant extension:

- `downloads/secureazcloud-pqc-crypto-inventory-template-v2.0`
- `downloads/secureazcloud-crypto-agility-assessment-template-v2.0`
- `downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v2.0`
- `downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v2.0`

The [README](README.md) is the complete current/historical download catalog. The [source map](source-map.json) and [crosswalk](source-map-addendum.json) record reviewed NIST source IDs and statuses. Do not infer approval from inclusion in the register.

## Maintaining Completed Assessments

Preserve the original assessment and its version. Map old fields into the version 2.0 schema by header/meaning, retain evidence provenance, and review new fields. Do not paste by column position or overwrite formula cells. Unknowns remain unassessed until evidence supports a decision.

## Standards and Threat Review

Assign an owner. Review quarterly, with the next planned review on **2026-12-29**, and sooner when a material event occurs. This is a documented maintenance process, not an automated monitoring service or a NIST-mandated interval.

- Check official NIST publication pages for final/draft status, errata, new versions, candidate status, and supersession.
- Verify module certificate/status, exact implementation, protocol profile, and supplier-supported configuration.
- Monitor credible cryptanalytic results, implementation issues, supplier releases, incidents, and architecture changes.
- Record source changes, affected artifacts/assets, applicability, decisions, owners, due dates, evidence, and tests.
- Revisit 2026/2027/later plans against current requirements. Do not turn draft dates or expected publication dates into mandates.
- Update the source register, affected files, versions, release notes, links, and validation report together.

## Publication Limits

Publish synthetic/redacted examples only. Do not include operational inventories, credentials, private keys, hostnames, internal architecture, customer data, or sensitive evidence. Describe source alignment precisely; do not claim NIST endorsement, certification, universal compliance, future guidance coverage, or unperformed testing.
