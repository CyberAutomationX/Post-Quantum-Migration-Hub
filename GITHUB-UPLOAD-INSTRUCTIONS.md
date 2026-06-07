# GitHub Upload Instructions - SecureAzCloud PQC Add-on Implementation Artifacts v1.1.0

## What is already done

Your existing GitHub Pages hub is live here:

https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/

It already contains:
- Crypto Inventory Template
- PQC Readiness Checklist
- Cloud/IAM Migration Playbook
- SCADA/ICS Checklist
- Reference Map

## What this add-on delivers now

This add-on adds three more focused implementation artifacts without replacing the hub:

1. Crypto-Agility Assessment Template
2. PQC Cloud & Workload Identity Migration Checklist
3. SCADA/ICS PQC Migration Continuity Checklist

## Upload steps

1. Unzip `SecureAzCloud_PQC_GitHub_Addon_Upload_Bundle_v1.1.0.zip`.

2. Open your GitHub repository:
   `CyberAutomationX/Post-Quantum-Migration-Hub`

3. Click:
   `Add file` -> `Upload files`

4. Drag these items from the unzipped bundle:
   - `downloads/`
   - `resources/`
   - `README-ADD-ON.md`
   - `release-notes-v1.1.0.md`
   - `source-map-addendum.json`

   GitHub will merge the `downloads` and `resources` folders with the folders already in your repository.

5. Commit with this message:
   `Add SecureAzCloud PQC implementation artifacts v1.1.0`

6. Edit `index.html`.

7. Open `index-additions-snippet.html` from this bundle and copy its full content.

8. Paste the snippet in `index.html` below the current `Resource downloads` section and before the `Five-step migration preparation workflow` section.

9. Commit the `index.html` change with this message:
   `Update hub landing page for PQC implementation artifacts v1.1.0`

10. Wait 2-5 minutes for GitHub Pages deployment.

## Test URLs after deployment

Open these URLs:

- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/resources/crypto-agility-assessment-template.html
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-crypto-agility-assessment-template-v1.0.xlsx
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-crypto-agility-assessment-template-v1.0.pdf

- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/resources/pqc-cloud-workload-identity-migration-checklist.html
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.xlsx
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-pqc-cloud-workload-identity-checklist-v1.0.pdf

- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/resources/scada-ics-pqc-migration-continuity-checklist.html
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.xlsx
- https://cyberautomationx.github.io/Post-Quantum-Migration-Hub/downloads/secureazcloud-scada-ics-pqc-continuity-checklist-v1.0.pdf

## Release recommendation

Create a GitHub release:

Tag: `v1.1.0`

Title: `SecureAzCloud PQC Implementation Artifacts v1.1.0`

Release notes:

```
Adds three public/redacted implementation artifacts:
- Crypto-Agility Assessment Template
- PQC Cloud & Workload Identity Migration Checklist
- SCADA/ICS PQC Migration Continuity Checklist

Each artifact includes PDF, XLSX, CSV, GitHub Pages HTML resource page, and NIST/CISA standards alignment.
```

Upload the three individual ZIP packages as release assets.
