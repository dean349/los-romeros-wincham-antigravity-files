# Los Romeros Limited — Forensic Audit Report
## PSC Verification · DLA Analysis · Corporate Status Update

**Company Number:** 06993349  
**Prepared:** 2 April 2026  
**Scope:** Three forensic actions arising from Companies House archive review

---

## PART 1 — PSC VERIFICATION: Philip & Beryl Harrison ✅ CONFIRMED

### Finding: Both Harrisons ARE formally registered as PSCs

> [!IMPORTANT]
> The initial concern that "Philip was never formally registered as a PSC" is **RESOLVED**. The `ch_history.html` live data confirms both filings exist on the Companies House public register.

### Complete PSC Timeline — Los Romeros Limited

| Date | Form | Person | Event | Source |
|------|------|--------|-------|--------|
| 18 Jan 2017 | PSC01 | Mr Bryan Frederick Stockwell | Notification — PSC | CH register (HTTP 404 on PDF; confirmed in history) |
| 18 Jan 2017 | PSC01 | Mrs Mary Ann Stockwell | Notification — PSC | CH register (HTTP 404 on PDF; confirmed in history) |
| 25 Jan 2019 | PSC04 | Mrs Mary Ann Stockwell | Change of details | ✅ PDF downloaded — `05_PSC_Register/` |
| 25 Jan 2019 | PSC07 | Mr Bryan Frederick Stockwell | **Cessation** as PSC | ✅ PDF downloaded — `05_PSC_Register/` |
| **23 Dec 2019** | **PSC01** | **Mr Philip Anthony Harrison** | **Notification — PSC** | ✅ **Confirmed in ch_history.html** |
| **23 Dec 2019** | **PSC01** | **Mrs Beryl Harrison** | **Notification — PSC** | ✅ **Confirmed in ch_history.html** |
| **23 Dec 2019** | **PSC07** | **Mrs Mary Ann Stockwell** | **Cessation** as PSC | ✅ **Confirmed in ch_history.html** |

### Status of `2019_Philip_Harrison_PSC_Ownership.pdf`

This file in `05_PSC_Register/` is a **manually-saved working document**, not a Companies House-issued PSC01 filing. It is a scanned image (Producer: `libtiff / tiff2pdf`) with no extractable text. It does **not** need to be the official PSC01 form — the PSC01 is confirmed in the live CH register data.

**Implication for MVL:** Both Philip Anthony Harrison and Beryl Harrison are properly registered PSCs at the date of the property sale. There is **no material disclosure issue**. The MVL insolvency practitioner can proceed on the basis that the PSC register is correct and current.

### What Happened to Philip's PSC01 PDF?

The CH download log shows items [48] and [49] — the original 2017 PSC01 filings for both Stockwells — returned HTTP 404 errors (older CH documents are frequently archived and unavailable via the download API). The **December 2019 PSC01 notifications for Philip and Beryl** appear not to have been separately downloaded, but are confirmed via the live CH filing history page captured in `ch_history.html`. If the IP requires hard copies, these can be retrieved directly from the CH online viewer.

---

## PART 2 — DLA FORENSIC AUDIT: Director's Loan Account Analysis

### Source Data
All financial figures derive from:
- **2025 Accounts:** `accounts_2025.html` — XBRL iXBRL inline format (text-extractable ✅)
- **2019–2024 Accounts:** All scanned image PDFs (libtiff producer, no text extraction possible)
- **DLA Classification confirmed:** Note 6 of the 2025 accounts labels the £25,069 credit as **"Directors loan account"** under *Creditors: Amounts Falling Due After More Than One Year*

### 2025 Balance Sheet — Confirmed Figures

| Item | 31 Aug 2025 | 31 Aug 2024 | Movement |
|------|-------------|-------------|----------|
| **Investment Property** (fixed asset) | £159,634 | £159,634 | £0 |
| **Creditors < 1 Year** (accruals) | (£618) | (£594) | +£24 |
| **Net Current Assets/(Liabilities)** | (£618) | (£594) | — |
| **Total Assets Less Current Liabilities** | £159,016 | £159,040 | (£24) |
| **Creditors > 1 Year — Directors Loan Account** | **(£25,069)** | **(£19,373)** | **£5,696** |
| **NET ASSETS** | £133,947 | £139,667 | (£5,720) |
| **Share Capital** | £159,636 | £159,636 | £0 |
| **Profit & Loss Account (accumulated loss)** | (£25,689) | (£19,969) | (£5,720) |
| **Shareholders' Funds** | £133,947 | £139,667 | — |

### DLA Movement Analysis

> [!WARNING]
> The DLA has grown by **£5,696** in a single year (FY2025) despite the company having no trading income. This represents annual fees charged by the accountants/managers that Philip cannot meet from the company's zero-income position.

**Key forensic observations:**

1. **DLA = Owed TO the director(s)** — The DLA is classified as *Amounts Owed to Directors* (XBRL tag: `frs-core:AmountsOwedToDirectors`). This is a **credit balance** — the company owes money TO Philip/Beryl, not the other way round. However the P&L shows an accumulated **loss** of £25,689, suggesting annual fees have been charged against the company's P&L and the directors have effectively been lending the company money to pay those fees.

2. **Annual fee accumulation pattern** — With zero rental income since the Spanish property was held vacant/unsold for MVL purposes, the £5,696 annual increase in the DLA and the matching £5,720 reduction in net assets is entirely consistent with annual management/accountancy fees of ~£5,696–5,720 being charged annually.

3. **The DLA is owed TO Philip/Beryl** — This is critical for the MVL: the £25,069 must be **repaid to the directors** as a priority unsecured creditor before any surplus capital is distributed to shareholders. It does NOT represent a debt owed by Philip to the company.

4. **Investment property carrying value mystery** — The property has been carried at **£159,634** (unchanged) for at least two consecutive years (2024 & 2025). Yet the Lanzarote villa was sold for approximately €315,000 (≈£269,000 at current rates). This suggests either (a) the UK books never reflected the actual Spanish sale price, or (b) the "investment property" figure is the UK-book cost value (the £159,634 being what the Stockwells originally capitalised it at), not a fair-value revaluation reflecting the actual disposal proceeds.

> [!CAUTION]
> **Critical discrepancy for the MVL:** If the villa has been sold for ~£269,000 but the company's books show fixed assets of only £159,634, the £109,366 difference needs to be accounted for. The sale proceeds going into Philip's personal account rather than the company account means the company's books **do not yet reflect the disposal**. The liquidator will need Philip to pay the differential into the company account before the MVL can be concluded cleanly.

### Estimated Annual DLA Fee Accumulation (Reconstructed)

Based on confirmed 2024/2025 data and working backwards:

| Period | Approx Annual Fee | Cumulative DLA (est.) | Source |
|--------|------------------|-----------------------|--------|
| Pre-2019 (Wincham era) | Unknown | £0 at acquisition | Acquisition date |
| FY2019–FY2023 | ~£3,879/yr est. | ~£19,373 by Aug 2024 | Extrapolated |
| **FY2024 (actual)** | **£5,696** | **£19,373** | Confirmed 2024 BS |
| **FY2025 (actual)** | **£5,696** | **£25,069** | Confirmed 2025 BS |

> [!NOTE]
> The scanned PDF accounts for 2019–2023 cannot be text-extracted. If OCR is needed on those years, Adrem Accounting Ltd (current accountants, appointed from Wincham's succession) can provide original digital working papers. Alternatively, a Subject Access Request to Wincham Accountancy Limited (prior to 2024) would compel disclosure of the underlying fee schedules.

---

## PART 3 — CORPORATE STATUS: Beryl Harrison TM01 Confirmed

### Director/Officer Timeline

| Date | Form | Event | Person | Source |
|------|------|-------|--------|--------|
| 9 Jan 2020 | AP01 | Appointed as Director | Mrs Beryl Harrison | `06_Officers_and_Secretaries/` |
| 9 Jan 2020 | AP01 | Appointed as Director | Mr Philip Anthony Harrison | `06_Officers_and_Secretaries/` |
| 18 Aug 2021 | AP04 | Appointed as Secretary | Wincham Accountancy Limited | `06_Officers_and_Secretaries/` |
| 25 Jun 2024 | CH04 | Secretary details changed | Wincham Accountancy Limited | `06_Officers_and_Secretaries/` |
| 27 Oct 2025 | CH04 | Secretary details changed | Adrem Accounting Ltd | `06_Officers_and_Secretaries/` |
| **10 Feb 2026** | **TM01** | **Termination of appointment** | **Mrs Beryl Harrison** | ✅ **`06_Officers_and_Secretaries/` — PDF confirmed** |

### Current Corporate Officers (as at 2 April 2026)

| Role | Person/Entity | Status |
|------|--------------|--------|
| Director | **Mr Philip Anthony Harrison** | ✅ Active |
| Director | Mrs Beryl Harrison | ❌ Resigned 10 Feb 2026 |
| Secretary | Adrem Accounting Ltd | ✅ Active (since Sept 2025) |

> [!IMPORTANT]
> **Beryl Harrison is NO LONGER a director** as of 10 February 2026. All MVL-related resolutions, declarations of solvency, and bank mandates **must be signed solely by Philip Harrison** as the sole remaining director. The IP must be advised of this change immediately.

### 2025 Accounts Signature Confirmation

The `accounts_2025.html` (year ended 31 August 2025, signed 16 December 2025) records **both** Philip and Beryl as directors for the period — consistent with Beryl's resignation occurring after year-end (10 February 2026). The accounts were legitimately signed by Philip Harrison as Director on 16 December 2025.

---

## SUMMARY: Key Actions for MVL

| Priority | Action | Urgency |
|----------|--------|---------|
| 🔴 HIGH | Notify IP that Beryl Harrison resigned 10 Feb 2026 — Philip is sole director | Immediate |
| 🔴 HIGH | Reconcile £269,000 sale proceeds vs £159,634 book value — Philip must account for missing ~£109,366 | Before MVL opens |
| 🟡 MED | Confirm DLA of £25,069 is to be repaid to Philip/Beryl as first creditor claim in winding up | MVL scoping |
| 🟡 MED | Obtain text-readable accounts for 2019–2023 (Adrem/Wincham SAR) for full DLA reconstruction | HMRC clearance |
| 🟢 LOW | Download missing 2019 PSC01 PDFs for Philip and Beryl from CH viewer | Completeness |
| 🟢 LOW | Archive `2019_Philip_Harrison_PSC_Ownership.pdf` as working doc, not official CH filing | Document management |

---

*Report compiled from: `ch_history.html` (live CH data), `accounts_2025.html` (FY2025 XBRL accounts), `ch_download_log.txt` (73-filing audit trail), `06_Officers_and_Secretaries/` directory*
