# Lanzarote Repatriation Financial Strategy

The objective is to calculate the Spanish Capital Gains Tax (CGT) for the sale of the Lanzarote property by Los Romeros Limited, formulate two risk scenarios for the unpaid Modelo 210 tax, and determine the most tax-efficient UK extraction route via a Members' Voluntary Liquidation (MVL) for Philip and Beryl Harrison.

## User Review Required
Before writing the final financial breakdown, please review the proposed calculations below. 

> [!NOTE]
> **Data Discovered:** I ran a cross-notebook query and found two key acquisition values:
> 1.  **UK Capital Gains Base:** The base acquisition cost to calculate UK CGT for Philip Harrison is **£159,636** (the amount paid for the Los Romeros shares in December 2019).
> 2.  **Spanish Corporate CGT Base Estimate:** The company recorded an allotment of shares worth **£171,734** on 22 June 2010. This must be converted into Euros based on the spot exchange rate on that date to estimate the Spanish CGT base, assuming we don't have the final *Escritura de Compraventa* Euro value yet.

## Proposed Strategy

### 1. Spanish Capital Gains Calculation (Corporate - 19%)

**Sale value:** €315,000
**Deductible expenses:**
*   Notary Fees: €474.86
*   Wincham Fees (Spanish portion): £9,600 (approx. €11,200)
*   Estate agent fees: €3,150 (Option part) - *Awaiting exact total commission, typically 5%*
*   Plusvalia Municipal: *Awaiting exact calculation*

**Two CGT Scenarios based on Modelo 210 Compliance:**

*   **Scenario A (Modelo 210 historically paid or voluntarily settled):**
    If the company pre-emptively settles the 2022-2026 back taxes, the cost is the base tax (€13,822) plus a small 15% late surcharge (~€2,073).
    *Total Modelo 210 impact:* ~€15,895.
    The Capital Gains tax logic holds standard. The 3% AEAT retention is taken at source from the purchase price, and the 19% corporate non-resident capital gains tax on the net gain is paid.

*   **Scenario B (Modelo 210 ignored; Audit Triggered):**
    Spain catches the unpaid imputed income upon processing the CGT declaration.
    *Total Modelo 210 impact:* Up to €34,554 (due to 50%-150% audit fines plus interest).
    The authorities will likely freeze or offset the 3% AEAT retention refund against this penalty, severely impacting the net cash repatriated.

### 2. UK MVL Liquidation & Tax Maximization (Phil & Beryl Harrison)

With £247,730 safely received into the UK HSBC bank account, the cash must be extracted from Los Romeros Limited.

**MVL Process & Costs**
*   Appoint an Insolvency Practitioner (IP). Typical MVL costs range from £2,500 to £4,000 + VAT.
*   Disbursements (London Gazette notices, bonding): ~£300.
*   Statutory Declaration of Solvency to swear at a solicitor.

**50/50 Shareholder Maximization Strategies**
*   **Business Asset Disposal Relief (BADR - formerly Entrepreneurs' Relief):** A property investment company usually *does not* qualify for BADR (which gives a 10% tax rate). However, normal CGT rules will apply to the capital distribution, which would be 10% or 20% depending on Phil and Beryl's personal income tax bands.
*   **Capital Gains Annual Exemption:** Both Phil and Beryl have an annual CGT allowance (currently £3,000 each for 2024/25, remaining £3,000 for upcoming years). Liquidating and distributing cash over two tax years could double this allowance (e.g., £6,000 total in Year 1, £6,000 in Year 2 if timed over April 5th).
*   **Foreign Tax Credit Relief (FTCR):** Any Spanish Corporate Tax and CGT paid by the company cannot easily be claimed personally by the shareholders, but the *net* asset value of the company dropping reduces the overall capital gain on the shares. We will explore specific loopholes in the UK-Spain Double Taxation Convention.

## Open Questions
1. Do you have the original 2010 acquisition value or share capital amount assigned to the Lanzarote property? 
2. Are there any other business expenses (e.g. accountancy fees, flights for board meetings) Los Romeros Limited has incurred recently that we can offset against UK Corporation Tax before the MVL?
3. What is the total estate agent commission percentage or amount paid for the sale?
4. Shall I build out the full HTML/Markdown financial dashboard next?

## Verification Plan
1. Calculate hard numbers for both scenarios.
2. Outline the exact timeline for the IP appointment.
3. Verify UK CGT rates (10% vs 20%) applicable to the solvent winding up of a property holding company.
