# Wincham Investigation & Evidence Recovery Report

Based on a thorough analysis of all Antigravity workspaces and conversation histories, I have successfully located the exact files, conversations, and forensic evidence you requested regarding Wincham, Phil Harrison's portal, and the SSL breaches.

Here is the breakdown of the historical research and recovered evidence files:

### 1. Wincham & Subsidiaries (Companies & Websites)
Extensive research was previously conducted into the entire corporate structure of the Wincham Group, mapping out their UK and Spanish entities, management, and regulatory compliance status.

**Primary Research Document Located:**
- **[Comprehensive Forensic Audit - Wincham Group](file:///C:/Users/Dean%20Harrison/.gemini/antigravity/brain/86cb3d0f-20b2-49f8-afb4-41a841d0b31b/wincham_group_audit.md)**

*Key Contents of this document:*
- **UK Entities:** Identifies over 17 active/dissolved UK companies linked to Wincham (including *Wincham Investments Limited*, *Wincham Accountants Limited*, *Agere International Ltd*, etc.), plus over 782 client nominee companies registered to their addresses.
- **Spanish Entities:** Identifies 3 Spanish companies (*Wincham Spanish Services SL*, *Wincham Investments Spain SL*, *Wincham International Spain SL*) and unequivocally confirms the absence of any legitimate Lanzarote office.
- **Websites:** Audits multiple group websites including `wincham.com`, `winchamiht.com`, `winchamukcompany.com`, `winchampropertyshop.com`, and `adremaccs.com`.

### 2. Phil Harrison's Client Portal (Scraping Info)
A full forensic session reconstruction was found detailing a major operation to scrape and catalog evidence from Philip Harrison's client portal cases. 

**Primary Reconstruction Document Located:**
- **[Conversation: "Analyzing Wincham Contractual Irregularities" - Full Reconstruction](file:///C:/Users/Dean%20Harrison/.gemini/antigravity/brain/30e5d75f-3ce4-4c75-8190-335263edf9f6/conversation_2bdee8af_full_reconstruction.md)**
- **[Wincham Project Brief](file:///C:/Users/Dean%20Harrison/.gemini/antigravity/brain/4975232e-60ac-439b-90ba-92845263c8dd/project_brief.md)**

*Key Contents of this operation:*
- The system used a browser subagent to log into `https://www.wincham.com/` as Philip Harrison and target his two primary cases: **WI-25863** (Property Sales Case) and **WI-13211** (Los Romeros Limited).
- Subagents captured all available tabs: Company Details, Cash Book, Documents, Directors, Secretaries, Allotments, and Messages.
- **Critical Findings Extracted:** Discovered an unexplained massive jump in "Client Expenditure" marked as *Telephone and Internet* for €53,002.00, evidence of 16.5% ITP misrepresentations, and missing resolution records.

*Captured Screenshots/Visual Evidence Identified During Scrape:*
- `tax_illustration_full_1775393741051.png`
- `wincham_portal_phase1_recon_1775393262231.webp`
- `company_details_tab_full_1775398185594.png`
- `cash_book_huge_telephone_bill_erroneous_1775398628692.png`

*(Note: These visual captures are stored in the `/browser` scratchpads under Conversation ID `2bdee8af-8877-4b5f-ad9c-7a8b0df7942d`)*.

### 3. SSL Certificates Expiring & Insecure Login Evidence
A dedicated forensic report was compiled regarding the complete failure of the SSL encryption on the primary Wincham portals, creating a `NET::ERR_CERT_DATE_INVALID` error standardizing a failure of UK GDPR and ethical compliance.

**Primary Breach Report Located:**
- **[Wincham Group — SSL/TLS Certificate Failure Report](file:///C:/Users/Dean%20Harrison/.gemini/antigravity/brain/86cb3d0f-20b2-49f8-afb4-41a841d0b31b/wincham_ssl_breach_report.md)**

*Key Contents of this document:*
- Evaluated the expired SSL/TLS on `wincham.com` that presented risks of Man-in-the-Middle (MitM) attacks allowing actors to intercept and read client login credentials, NIA, bank references, and will instructions.
- Confirmed that the AI browser scraping operation specifically had to **bypass this expired SSL warning** to login, logging this as concrete forensic evidence of regulatory negligence.
- Highlighted breaches of **UK GDPR Article 32**, **Article 5(1)(f)**, and **CRA 2015 s.49** regarding reasonable care.

---
> [!NOTE] 
> All mentioned documents exist permanently in your workspace's historical `.gemini` brain storage. Click the absolute links provided above in this markdown file to review the fully extracted contents.
