# Workspace Reorganisation Plan
## `c:\DAD\UK_Lanzarote_Repatriation`

---

## ⚠️ Your GitHub Concern — Answered First

**Short answer: Moving files CAN break things, but only for the nested Git repos — and only if you do it carelessly. The main repo is fine.**

Here is the full picture of every Git repo inside the workspace:

| Folder | GitHub Remote | Risk if Moved |
|---|---|---|
| `c:\DAD\UK_Lanzarote_Repatriation\` | `dean349/lanzarote-repatriation-explainer` | ✅ Safe — this IS the root; don't move it |
| `Files and Information for Phil Harrison\` | `dean349/lanzarote-forensic-portal` | ⚠️ **Nested repo** — moving this folder breaks the local path |
| `deploy_pages\` | `dean349/deploy_pages` repo? (no remote found — `.git` folder only) | ⚠️ Nested repo — can be safely relocated if you update your scripts |
| `philip-harrison-case-report\` | `dean349/philip-harrison-negligent-claims-against-wincham` | ⚠️ Nested repo — moving breaks local path |
| `temp_repos\lanzarote-cgt-report\` | Unnamed local repo | 🟡 Temp — likely disposable |
| `temp_repos\philip-harrison-lanzarote-spanish-cgt-report\` | Unnamed local repo | 🟡 Temp — likely disposable |

> [!IMPORTANT]
> The three nested repos (`Files and Information for Phil Harrison`, `deploy_pages`, `philip-harrison-case-report`) have their own `.git` folders. **Moving their parent folder on disk does NOT change what's on GitHub** — the remote repo stays intact. But all your local Python/PowerShell scripts that reference hard-coded paths to those folders WILL break and will need updating. Nothing is irreversible.

---

## Current State — What the Mess Looks Like

The root has **51 loose files** — a mixture of:
- Python scripts (20+) for generating reports, fetching CH data, building PDFs
- HTML output files (`cgt-report.html`, `historical_ledger.html`, `scenario-planning.html`, etc.)
- Raw data files (`history.json`, `all_accounts_extract.txt`, `graph.mmd`)
- PDFs (`los_romeros_accounts_2025.pdf`, CGT report PDF)
- Config files (`.mcp.json`, `mcp.json`, `.gitignore`)

The existing folders are logically named but inconsistently used (e.g. `Bank_Statements` and `Spanish_Deeds` are completely empty).

---

## Proposed New Structure

```
c:\DAD\UK_Lanzarote_Repatriation\
│
├── 📁 _scripts\                          ← ALL Python & PowerShell utility scripts
│   ├── build_html.py
│   ├── convert_all_md.py
│   ├── convert_html_to_pdf.py
│   ├── convert_md_to_html.py
│   ├── convert_pitch_report.py
│   ├── convert_pitch_report_external.py
│   ├── convert_report.py
│   ├── convert_updated_mds.py
│   ├── download_ch_public.py
│   ├── extract_financials.py
│   ├── fetch_and_organise_ch.py
│   ├── fetch_ch.ps1
│   ├── fetch_ch.py
│   ├── fetch_ch_curl.py
│   ├── fetch_los_romeros.mjs
│   ├── fetch_pdfs_final.ps1
│   ├── fetch_psc.py
│   ├── fetch_requests.py
│   ├── generate_all_pdfs.py
│   ├── generate_all_pdfs_playwright.py
│   ├── generate_five_pdfs.py
│   ├── get_links.py
│   ├── html_to_pdf_playwright.py
│   ├── rebuild_and_publish.py
│   ├── render_external_pdf.py
│   └── render_forensic_portal.py
│
├── 📁 _output\                           ← Generated HTML/PDF output files (root level)
│   ├── accounts_2025.html
│   ├── cgt-report.html
│   ├── ch_history.html
│   ├── divorce_financial_report.html / .pdf / .md (×2 versions)
│   ├── explainer.html
│   ├── historical_ledger.html
│   ├── recovered_conversations.html
│   └── scenario-planning.html
│
├── 📁 _data\                             ← Raw data, JSON, logs, CSVs
│   ├── all_accounts_extract.txt
│   ├── all_accounts_pypdf.txt
│   ├── ch_download_log.txt
│   ├── graph.mmd
│   ├── graph.png
│   ├── history.json
│   └── los_romeros_accounts_2025.pdf
│
├── 📁 Los Romeros - Company Records\     ← (rename from los_romeros_ch_data)
│   └── [12 existing CH subfolders, unchanged]
│
├── 📁 Annual Accounts\                   ← (already exists, keep as-is)
├── 📁 Bank Statements\                   ← (already exists, currently empty)
├── 📁 Spanish Deeds\                     ← (already exists, currently empty)
│
│   ── ROOT-LEVEL HTML (published to GitHub Pages) ──
├── index.html                            ← KEEP HERE (GitHub Pages root)
├── .gitignore
├── .mcp.json
├── mcp.json
├── .nojekyll
│
│   ── NESTED REPOS (leave in place OR move with care) ──
├── 📁 Files and Information for Phil Harrison\   ← ⚠️ Nested repo — LEAVE IN PLACE
│   └── [files unchanged]
│
├── 📁 philip-harrison-case-report\       ← ⚠️ Nested repo — LEAVE IN PLACE
│   └── [files unchanged]
│
├── 📁 deploy_pages\                      ← ⚠️ Nested repo — LEAVE IN PLACE
│
├── 📁 temp_repos\                        ← 🟡 Consider deleting — appears to be staging
│
├── 📁 Dad Correspondence\                ← LEAVE AS-IS (active working files)
│   └── [files unchanged]
│
└── 📁 Wincham Legal Case UK Type Class Action\    ← LEAVE AS-IS (major work area)
    ├── 📁 _scripts\                      ← Move the 15+ Python scripts in here
    ├── 📁 _data\                         ← Move CSVs, XLSXs, raw data
    ├── 📁 Documents\                     ← Keep .md / .html / .pdf report files
    └── 📁 Wincham Scheme-Legal Claims-Victims\   ← LEAVE (already a subfolder)
```

---

## What Moves, What Stays

### ✅ SAFE to move (no git impact, just file organisation)
- All `.py` and `.ps1` scripts at the root → `_scripts\`
- HTML and PDF output files at root → `_output\`
- Raw data files at root → `_data\`
- Inside Wincham folder: Python scripts → `Wincham Legal Case UK Type Class Action\_scripts\`
- Inside Wincham folder: CSV/XLSX data files → `Wincham Legal Case UK Type Class Action\_data\`

### ⚠️ DO NOT MOVE (nested Git repos — would break local paths)
- `Files and Information for Phil Harrison\` — has its own `.git` pointing to `lanzarote-forensic-portal`
- `philip-harrison-case-report\` — has its own `.git` pointing to `philip-harrison-negligent-claims-against-wincham`
- `deploy_pages\` — has its own `.git` folder

### 🟡 CONSIDER DELETING
- `temp_repos\` — two identical `index.html` files (34KB), both unnamed local repos. Unless actively used, these are staging artifacts.
- `deploy_report\` — completely empty folder
- `Bank_Statements\` — completely empty
- `Spanish_Deeds\` — completely empty

### 📌 Script Path Updates Required (if you move scripts to `_scripts\`)
Any script that uses relative paths like `../` or that is called from other scripts will need its `Cwd` or internal path references updated. This is manageable — most scripts appear to operate on files in their current directory.

---

## Open Questions for You

> [!IMPORTANT]
> **Before I do anything**, please confirm:
> 1. **Are you happy to move the root-level scripts/outputs/data into subfolders?** (Recommended — biggest immediate cleanup)
> 2. **Should I reorganise inside `Wincham Legal Case UK Type Class Action` too?** (93 files + scripts mixed together)
> 3. **Can I delete `temp_repos\`?** The two repos inside appear to be unused staging copies.
> 4. **Empty folders** (`Bank_Statements`, `Spanish_Deeds`, `deploy_report`) — delete or keep as placeholders?
> 5. **Script paths**: Are you OK with me updating any hard-coded file paths inside the moved Python scripts? This is necessary for them to keep working.

---

## Verification Plan
After moving files:
- Run `git status` in the root repo to confirm no tracked files are accidentally marked as deleted
- Test one Python script (e.g. `convert_all_md.py`) to confirm relative paths still work
- Confirm GitHub Pages repos (`deploy_pages`, `philip-harrison-case-report`) still serve correctly — they are self-contained and unaffected by organisation of sibling folders
