# UK Government & Legal Authority MCP Servers
### Research Report — Wincham Legal Case

---

## Executive Summary

Three categories of MCP servers are now available that are directly relevant to your case:
1. **UK Legislation** — Official UK government-built MCP giving semantic search across 8.4M legal documents
2. **Companies House (Enhanced)** — Better MCP options than what we currently use
3. **UK Government Aggregator** — 33 government APIs in one server
4. **UK Tax-Benefit Simulation** — PolicyEngine for CGT/IHT modelling

There is **no official ICO MCP server** and **no official HMRC MCP server** as of April 2026. All ICO and HMRC guidance must still be verified manually via their websites.

---

## 1. 🏛️ i.AI Lex — UK Legislation MCP
**Built by:** UK Government's i.AI team + National Archives + Ministry of Justice  
**GitHub:** https://github.com/i-dot-ai/lex  
**Live Docs:** https://lex.lab.i.ai.gov.uk/docs  
**Status:** ✅ Active — v1.1.0 released March 23, 2026

### What it covers
| Dataset | Volume |
|---------|--------|
| UK Acts & Statutory Instruments (1267–present) | 220,000 |
| Legislative amendments | 892,000 |
| Explanatory Notes | 89,000 |
| Case Law judgments (temporarily disabled) | 70,000 |
| Total indexed documents | **8.4 million** |

### Why this matters for Wincham
- Verify UK GDPR Article 6(1)(f) wording directly from statute
- Verify Data Protection Act 2018 (ss.1–6) exact text
- Search Companies Act 2006 for Companies House register obligations
- Verify ICAEW/FCA regulatory legislation (Financial Services Act, etc.)
- **Semantic search** — ask "what constitutes legitimate interests for legal claims?" and get cited statute

### ⚠️ Installation requirement
This requires Docker + Azure OpenAI credentials to self-host. It is **not** a simple `npx` install.

**Easier path:** The live API at `https://lex.lab.i.ai.gov.uk` can be used directly via `read_url_content` without any setup.

### Claude Desktop config (if self-hosting)
```json
{
  "mcpServers": {
    "lex-uk-law": {
      "command": "docker",
      "args": ["compose", "up", "-d"],
      "cwd": "/path/to/lex-repo"
    }
  }
}
```

### Alternative: Direct API access (no setup needed)
```
https://lex.lab.i.ai.gov.uk/docs
Search endpoint: GET /api/v1/legislation/search?q=legitimate+interests+UK+GDPR
```

---

## 2. 🏢 Companies House MCP (Enhanced Options)

### Option A: aicayzer/companies-house-mcp (Recommended — npx, easy install)
**GitHub:** https://github.com/aicayzer/companies-house-mcp

**Capabilities beyond our current setup:**
- ✅ Company profile, officer details, filing history
- ✅ PSC (Person with Significant Control) tracking
- ✅ **Due diligence red-flag scanning** (not in current setup)
- ✅ Caching and rate limit management built in
- ✅ Works natively in Claude Desktop

**Claude Desktop config:**
```json
{
  "mcpServers": {
    "companies-house": {
      "command": "npx",
      "args": ["-y", "companies-house-mcp"],
      "env": {
        "COMPANIES_HOUSE_API_KEY": "37e01bb5-04e8-4d0d-9895-9037e31e2e36"
      }
    }
  }
}
```

### Option B: brummiesteven/GovUK-MCP (Broader coverage)
**GitHub:** https://github.com/brummiesteven/GovUK-MCP  
**Covers:** ~33 UK government APIs including Companies House, Parliament, Transport, NHS

> ⚠️ Hobby project — use for research/enrichment only, not as primary legal source

---

## 3. 🇬🇧 GovUK-MCP Aggregator (33 Government APIs)
**GitHub:** https://github.com/brummiesteven/GovUK-MCP

APIs included relevant to this case:
- Companies House
- UK Parliament API (legislation progress)
- GOV.UK content search
- Electoral Commission (company director checks)
- Land Registry (property ownership verification)

**Setup:**
```bash
git clone https://github.com/brummiesteven/GovUK-MCP.git
cd GovUK-MCP
cp .env.example .env
# Add API keys to .env
npm install
```

---

## 4. 💷 PolicyEngine UK — Tax-Benefit Simulation MCP
**GitHub:** https://github.com/PolicyEngine/policyengine-uk  
**Purpose:** Simulate UK tax-benefit outcomes, CGT, NI, IHT

### Relevance to your case
- Model Philip Harrison's CGT liability from Los Romeros Ltd disposal
- Run IHT scenarios with/without gifting strategies
- Verify NRB/RNRB calculations independently

**Sample queries once connected:**
- "Calculate CGT on £315,000 disposal with £50,000 base cost for 2024-25 tax year"
- "What is IHT liability on estate of £750,000 with NRB and RNRB applied?"

**Installation:**
```bash
pip install policyengine-uk
```

**Claude Desktop config:**
```json
{
  "mcpServers": {
    "policyengine": {
      "command": "python",
      "args": ["-m", "policyengine_mcp.server"]
    }
  }
}
```

---

## 5. ❌ What Does NOT Exist (as of April 2026)

| Authority | Official MCP? | Status |
|-----------|--------------|--------|
| ICO (Information Commissioner) | ❌ No | Manual verification only via ico.org.uk |
| HMRC | ❌ No | Manual verification only via legislation.gov.uk |
| FCA | ❌ No | FCA Handbook manual search only |
| ICAEW | ❌ No | Manual search of icaew.com/regulations |
| Courts (BAILII) | ❌ No (case law in i.AI Lex temporarily disabled) | Use bailii.org directly |

---

## 6. Recommended Priority Actions

### Immediate (no installation required)
1. **Use Lex live API** via read_url_content to verify all legislation citations in the pitch report
   - URL: `https://lex.lab.i.ai.gov.uk/docs`

### Short-term (30-min setup)
2. **Install aicayzer Companies House MCP** in Claude Desktop for richer due diligence on Wincham officer records
   - Adds red-flag scanning not currently available

### Medium-term (requires Docker + Azure OpenAI)
3. **Self-host i.AI Lex** for full offline legislative search — gives you a proper legal verification layer for the pitch report
   - This would allow formal citation of statute in the LIA documentation

---

## 7. Current Legal Verification Stack (Post-MCP)

Once the Lex MCP is connected, the verification chain becomes:

```
Claim in Pitch Report
        ↓
Lex MCP → Search 8.4M UK legal documents → Return exact statutory text + citation
        ↓
ICO guidance → Manual via ico.org.uk (no MCP available)
        ↓
Companies House MCP → Verify officer/filing data → Cross-reference victim database
        ↓
Output: Fully cited, statute-grounded legal position
```

This would give you a **materially stronger** legal basis than the current manual-lookup approach.

---

*Report compiled: April 2, 2026 | Sources: GitHub, mcpmarket.com, i.ai.gov.uk*
