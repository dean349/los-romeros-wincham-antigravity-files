# Master Case Dossier Structure

This plan outlines the steps we will take to consolidate your various HTML reports, legal strategies, and tax documents into a single, unified "Case Dossier." 

This will provide your father, Philip Harrison, with a single link to access all the relevant documentation effortlessly, and it will clean up your GitHub account.

## User Review Required

> [!IMPORTANT]
> The main dashboard (`index.html`) will replace the current "Forensic Reporting Portal" landing page. The forensic report will still be fully available, it will just become one of the options to click on from the new master dashboard. Let me know if you are okay with this!

## Proposed Changes

### 1. File Consolidation (Moving the CGT Report)
We will bring the Capital Gains Tax report over from its separate repository.
* **[NEW FOLDER]** Create `capital-gains-tax-report/` in the main workspace.
* **[NEW FILE]** Copy the `index.html` from your `C:\temp\git_repos\lanzarote-cgt-report\` folder into this new folder.

### 2. Restructuring the Wincham Forensic Portal
The current `index.html` in your workspace is the "Action Plan & Executive Briefing." We will move this into its own page so the root `index.html` can become the Master Dashboard.
* **[RENAME]** Rename the current `index.html` to `wincham_report.html`.
* **[MODIFY]** Update any navigation links inside `historical_ledger.html` and `wincham_report.html` to ensure they still link to each other correctly.

### 3. Building the Master Dashboard
We will build a high-quality, professional, and mobile-friendly hub page that links out to all the other resources.
* **[NEW]** `index.html` (The Master Dashboard)
  * Will include a clean navigation menu linking to:
    1. Wincham Forensic Investigation & Action Plan
    2. Spanish Capital Gains Tax Report
    3. 17-Year Historical Ledger & Evidence Vault
    4. 2025 Financial Accounts

### 4. Deploying to GitHub
Once everything is moved into place locally and we ensure the links work:
* We will push the entire `UK_Lanzarote_Repatriation` folder up to the `dean349/lanzarote-repatriation-explainer` GitHub repository.
* This guarantees that a single GitHub Pages link (e.g., `https://dean349.github.io/lanzarote-repatriation-explainer/`) acts as the front door to the entire case dossier.

## Open Questions

1. **Title of Dashboard:** Do you want the main dashboard page to be titled something like "Lanzarote Repatriation — Master Legal & Financial Dossier"?
2. **Deleting Old Repositories:** After we publish this safely to GitHub, do you want my help safely deleting the old, messy repositories on GitHub so they no longer clutter your account?

## Verification Plan

### Automated Tests
* Use local testing to ensure all links correctly resolve between the newly created Master Dashboard and the sub-reports (`wincham_report.html`, `capital-gains-tax-report/index.html`).

### Manual Verification
* Once pushed, we will verify the live GitHub Pages link to ensure the site renders correctly on mobile and desktop.
