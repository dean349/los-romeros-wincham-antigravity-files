# UK Legal MCP Installation — Complete
### Workspace: `c:\DAD\UK_Lanzarote_Repatriation`

---

## ✅ Scope Isolation — How It Works

> [!IMPORTANT]
> All UK law tools are confined to this workspace via the `.mcp.json` file at the project root. This is the **workspace-scoped** MCP config, which is entirely separate from your global `claude_desktop_config.json`. Your US-law projects are completely unaffected.

| Config File | Scope | Status |
|-------------|-------|--------|
| `c:\DAD\UK_Lanzarote_Repatriation\.mcp.json` | **This workspace only** | ✅ Created |
| `%APPDATA%\Claude\claude_desktop_config.json` | Global (all projects) | ⛔ NOT touched |

---

## ✅ Installed Components

### 1. UK Law MCP — Local Build (Ansvar Systems)
| Item | Status |
|------|--------|
| **GitHub** | `Ansvar-Systems/UK-law-mcp` |
| **Database** | `data/database.db` — **278 MB**, pre-built from legislation.gov.uk |
| **Build** | `dist/index.js` — ✅ compiled successfully |
| **Coverage** | 3,241 UK statutes · 512,651 provisions |
| **Freshness** | Daily automated checks against legislation.gov.uk |
| **Data source** | Verbatim from The National Archives — zero LLM content |

**13 Tools available:**
- `search_legislation` — FTS5 full-text search across 512,651 provisions
- `get_provision` — exact section text by Act name + section number
- `validate_citation` — zero-hallucination citation check
- `build_legal_stance` — aggregate across statutes, case law, explanatory notes
- `format_citation` — UK citation format (full/short/pinpoint)
- `check_currency` — is this statute still in force?
- `get_eu_basis` — trace UK law back to its EU origin
- `validate_eu_compliance` — verify UK GDPR adequacy status
- + 5 more EU/international alignment tools

**Key statutes covered:** UK GDPR · DPA 2018 · Companies Act 2006 · Insolvency Act 1986 · TCGA 1992 · IHT Act 1984 · Limitation Act 1980 · POCA 2002 · FSMA 2000 · Civil Liability Act 2018

---

### 2. UK Law MCP — Remote Fallback (Ansvar Systems)
| Item | Status |
|------|--------|
| **Endpoint** | `https://mcp.ansvar.eu/law-uk-law-mcp/mcp` |
| **Coverage** | Same 3,241 statutes / 512,651 provisions |
| **Note** | Use only for non-confidential research — queries transit Ansvar's server |

---

### 3. Companies House MCP — Custom Local Server
| Item | Status |
|------|--------|
| **Location** | `.agent/mcp/companies-house/server.js` |
| **API Key** | `37e01bb5-04e8-4d0d-9895-9037e31e2e36` (active) |
| **Tools** | search_company · get_company · get_officers · get_filings |
| **Use** | Wincham victim verification · Adrem/Los Romeros officer lookups |

---

### 4. i.AI Lex Skill — UK Government Legal Database
| Item | Status |
|------|--------|
| **Location** | `.agent/skills/lex-uk-law/SKILL.md` |
| **Built by** | UK Government i.AI team + National Archives + Ministry of Justice |
| **Coverage** | 8.4 million UK legal documents |
| **Access** | Via `read_url_content` — no install required |
| **API** | `https://lex.lab.i.ai.gov.uk` |

---

### 5. PolicyEngine UK — Tax-Benefit Simulation
| Item | Status |
|------|--------|
| **Install** | `pip install policyengine-uk` ✅ |
| **Version** | v2.45.4 |
| **Use** | CGT modelling · IHT scenarios · NRB/RNRB calculations |
| **Import** | `from policyengine_uk import Microsimulation` |

---

## 📋 All Workspace Skills (8 Total)

| Skill | Purpose |
|-------|---------|
| `fx-risk-adviser` | EUR/GBP repatriation, forward contracts, FX broker selection |
| `iht-calculator` | UK IHT modelling, NRB/RNRB, PET taper relief, gifting strategies |
| `lex-uk-law` | ⭐ **NEW** — i.AI Lex API, 8.4M UK legal docs, statute verification |
| `mvl-process-tracker` | MVL stages, IP appointment, HMRC clearance, capital distribution |
| `spanish-property-compliance` | Modelo 210/211, AEAT retention, Plusvalía, Notary compliance |
| `uk-commercial-litigation-solicitor` | Professional negligence, pre-action protocols, POCA considerations |
| `uk-cross-border-tax-adviser` | CGT, FTCR, MVL capital extraction, cross-border corporate tax |
| `uk-private-client-solicitor` | Wills, trusts, IHT mitigation, Sheffield estate planning |

---

## 🔧 One Action Required From You

To activate the MCP servers in Claude Desktop/Antigravity, you need to add the contents of `.mcp.json` to your Claude configuration. There are two ways:

### Option A — Claude Code (recommended, automatic)
When you open this workspace in Claude Code, the `.mcp.json` is picked up **automatically**. No action needed.

### Option B — Claude Desktop (manual, one-time)
Open `%APPDATA%\Claude\claude_desktop_config.json` and add the `uk-law` and `companies-house` entries from `.mcp.json`. Keep them confined inside the `mcpServers` object — do **not** add a scope restriction in Claude Desktop as it applies globally.

> [!WARNING]
> If using Claude Desktop (Option B), adding UK law servers globally means they'll technically be available in other workspaces — but since they only respond to UK law queries, in practice they won't interfere with US-law work. Claude Code's `.mcp.json` is the safer option for strict isolation.

---

## 🗂 File Locations

| Component | Location |
|-----------|----------|
| Workspace MCP config | `c:\DAD\UK_Lanzarote_Repatriation\.mcp.json` |
| Master MCP reference | `c:\DAD\UK_Lanzarote_Repatriation\.agent\mcp\mcp-config.json` |
| UK Law MCP server | `.agent\mcp\UK-law-mcp\dist\index.js` |
| UK Law database | `.agent\mcp\UK-law-mcp\data\database.db` (278 MB) |
| Companies House server | `.agent\mcp\companies-house\server.js` |
| i.AI Lex skill | `.agent\skills\lex-uk-law\SKILL.md` |

---

*Installation completed: April 2, 2026*
