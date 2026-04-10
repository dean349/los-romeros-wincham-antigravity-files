# Integration of New Intelligence Updates into the Philip Harrison Case Report

This plan details how we will incorporate the extensive new forensic intelligence, emergency action plans, and legal precedents discovered across the workspace into the master `index.html` report.

## User Review Required

> [!WARNING]
> Please review this plan to ensure I am capturing all the recent updates correctly before I make the changes to the live HTML file.

## Proposed Changes

We will systematically update `C:\DAD\UK_Lanzarote_Repatriation\philip-harrison-case-report\index.html` to integrate the new findings from across the workspace.

### 1. Update Section 4: The Rescue Plan (Emergency Bank Correction)
We will completely overhaul the rescue plan to incorporate the immediate crisis steps detailed in the `emergency_bank_correction_plan.html`.
- **Add immediate actions:** Quarantining the personal account so the money isn't spent or mixed.
- **Add corporate account setup:** Prompting the setup of a challenger bank (Starling/Tide).
- **Add the exact reversal mechanic:** Explaining the reversal of funds with the exact `ERROR CORRECTION - CO FUNDS` reference to defeat the Section 455 HMRC threat.
- **Audit Logging:** Mention sending the internal email to establish a paper trail.

### 2. Update Section 4.5/4.6: The Legal Case (Corporate Phoenixing & The Giambrone Precedent)
We will expand the legal arguments to feature our newest leverage points.
- **Corporate Phoenixing:** Highlight the discovery of the unauthorized AD01 form filing in September 2025 (breach of Section 1112 of the Companies Act 2006).
- **The Giambrone Precedent:** Introduce the fact that this setup mirrors the exact circumstances of the *Giambrone* group action (successfully litigated by Edwin Coe LLP), providing massive leverage and proving we have the legal ammunition for a full group action.
- **Spanish Criminal Threshold:** Explicitly note the AEAT rulings and the €120k threshold for criminal tax fraud if the corporate wrapper is used improperly.

### 3. Add a "Starling Onboarding Guide" Summarized Appendix
We will append a quick reference to the Starling Bank application guide, ensuring Dad knows exactly what Enhanced Due Diligence (EDD) documents are required (Escritura, Nota Simple, Source of Wealth/Funds docs) to prevent the application from being blocked.

#### [MODIFY] `C:\DAD\UK_Lanzarote_Repatriation\philip-harrison-case-report\index.html`
- Make all the above insertions and formatting adjustments inside the existing HTML structure.
- Ensure the newly added tables and alerts use the existing CSS classes for continuity.

### 4. Push Updates to GitHub
Once the file is updated locally, I will commit and push the updates up to the `philip-harrison-negligent-claims-against-wincham` GitHub repository so that the live GitHub Pages link automatically updates.

## Open Questions

> [!IMPORTANT]
> - Do you want me to keep the new Giambrone and Phoenixing information within the "Legal Dossier" tab, or make sure it is directly prominent on the "Plain English" tab for maximum immediate impact?
> - Are there any other specific documents you want completely embedded in the report, or should I summarize the key action points as planned?

## Verification Plan

### Automated Tests
- Review the HTML locally using the `view_file` tool to ensure no broken tags or missing `.CSS` elements.
- Check the `gh api` to confirm the GitHub Pages deployment builds successfully after pushing.

### Manual Verification
- You will be able to review the live page at `https://dean349.github.io/philip-harrison-negligent-claims-against-wincham/` once the deployment finishes.
