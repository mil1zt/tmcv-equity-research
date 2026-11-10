# Tata Motors Ltd (TMCV) — Initiation of Coverage

**What is India's largest commercial-vehicle maker worth once you strip away the headlines — and what does the market need to believe to pay today's price?**

This repository is my attempt to answer that question the way a sell-side analyst would: an integrated three-statement model, a comps-led valuation with a DCF as the sanity check, and a 20-page initiation report.

> Educational project based solely on public information. Ratings and target values are illustrative and are **not investment advice**.


---

## Why this company

After its 2025 demerger, Tata Motors Ltd (TMCV) became a pure commercial-vehicle business — a newly listed entity with about a year of trading history and only one annual report of its own. That made it an interesting problem: rebuilding history across a demerger, finding peers that are genuinely comparable, and valuing a market leader in the middle of an up-cycle, while a €3.8bn acquisition (Iveco) closed during the analysis.

## The call

| Rating | CMP (08-Nov-26) | 12M target | Upside | DCF cross-check | Bull / Bear |
|:--:|:--:|:--:|:--:|:--:|:--:|
| **HOLD** | ₹426 | **₹440** | +3.3% | ₹366 (−17%) | ₹510 / ₹330 |

**What the numbers revealed:** a strong business — around 36% market share, revenue up 28% in H1 FY27, a net-cash balance sheet and high returns on capital — but one where commodity costs had already taken 540–590 bp off EBITDA margins.

**What settled the rating:** a reverse DCF. At ₹426, the market is pricing in a steady-state EBITDA margin of about **15.2%** — above the company's best recent level of **12.0%** (FY26) and my base case. A great business, but a fully valued one.

| Thesis pillar | Evidence | What would prove me wrong |
|---|---|---|
| 1. Volume leadership in an up-cycle | ~36% CV share (~55% in heavy trucks); GST cut from 28% to 18%; 70k-unit Indonesia order | Domestic volumes negative YoY for two quarters |
| 2. The margin dip is cyclical, not structural | ~540–590 bp commodity hit; four price hikes this year; FY26 margin 12.0% | EBITDA margin below 10% for two quarters |
| 3. Capital-light, net-cash compounding | Capex 2–4% of revenue; pre-tax ROCE ~40%; net cash ₹7.4k Cr | Iveco acquisition debt pushed onto the Indian balance sheet |

---

## Valuation snapshot

- **Primary — trading comparables (FY28E):** 12.7x EV/EBITDA and 19.8x P/E, a 10% discount to the median of Ashok Leyland, M&M and SML Mahindra, weighted 50/50 → **₹440**.
- **Sanity check — FCFF DCF:** WACC 12.6% (Rf 7.12%, ERP 5.2%, β 1.20), terminal growth 5.0%, Gordon-growth terminal value → ₹366, within my ±20% tolerance.
- **Scenarios:** bull ₹510 / base ₹440 / bear ₹330; probability-weighted value ≈ ₹430.

---

## Challenging the assumptions

The number at the end is only as good as the assumptions behind it, so this is where most of the work went

1. **Comps first, DCF as the sanity check.** This follows sell-side convention. The DCF uses Gordon growth only, so the intrinsic check doesn't quietly borrow a market multiple.
2. **Peers that are genuinely comparable.** After the demerger, only three listed companies truly compete with TMCV. I left out the passenger-vehicle makers rather than pad the peer set.
3. **Like-for-like debt.** Ashok Leyland's and M&M's consolidated debt includes their lending arms (₹64k Cr and ₹1.3 lakh Cr), so I took both on a standalone basis.
4. **Clean earnings.** FY26 profit carried ₹1,428 Cr of exceptional items and a ₹2,418 Cr fair-value loss. I adjusted for both at the 25.17% statutory tax rate — the reported 36% rate was itself distorted by those one-offs.
5. **No double-counted country risk.** Damodaran's India ERP (7.08%) less the 1.87% sovereign default spread that the INR G-Sec yield already prices in.
6. **A proxy beta.** With about a year of trading history, a regression beta for TMCV would be unreliable.
7. **History across a demerger.** FY22–FY25 rebuilt from the pre-demerger Tata Motors CV segment; FY26 from TMCV's first annual report.
8. **Iveco left out, deliberately.** The October 2026 acquisition is treated as value-neutral and flagged as the key swing factor.

---

## What's in this repository

```
├── report/     TMCV_Initiation_of_Coverage.pdf      20-page initiation report
├── model/      TMCV_Equity_Research_Model.xlsx      Fully linked model (Bull / Base / Bear switch)
├── templates/  Template_Equity_Research_Model.xlsx   Blank, reusable model
│               Template_Initiation_of_Coverage.docx  Report template with a model-link map
│               Template_Company_Update.docx          Follow-up / results-review template
├── docs/       methodology.md · model-guide.md · data-sources.md
└── assets/     Charts used in this README
```

### The model (Excel, no macros)
Laid out **Cover → Outputs → Inputs → Model**, vertically stacked in CFI formatting (blue = inputs, black = formulas, light grey = assumptions to set or stress-test).

- **Three-statement model** with working-capital, fixed-asset and debt schedules — the balance sheet balances in all 10 years and all three scenarios.
- **Scenario switch** (Bull / Base / Bear) driving revenue growth, EBITDA margin and capex, with an Excel data table summarising all three.
- **Trading comps engine** — market data, LTM and forward multiples, quartile statistics, implied share prices, and a target-multiple build with premium / discount and override.
- **DCF cross-check** — stub-period and mid-year discounting, cash rolled forward to the valuation date, a 12-month roll-forward and two live sensitivity grids.
- **12 automated model checks** on the Cover, from balance-sheet integrity to terminal-value share and DCF tolerance.

---

## Reusing the templates

I turned the work into templates so the next company starts from a stronger base:

1. Copy `Template_Equity_Research_Model.xlsx` and fill the **Inputs** sheet — company data, five years of history, peers, then the light-grey assumption cells.
2. Check the **Cover**: every model check should read *No*, or the flag should be explained in the report.
3. Fill `Template_Initiation_of_Coverage.docx` — blue italic text marks placeholders, and green *Model link* notes point to the exact model cells.
4. After results, use `Template_Company_Update.docx` with a dated copy of the model to show old vs new estimates, an EPS bridge and a target-value bridge.

---

## How this was built

Primary sources came first — audited annual reports, exchange filings and results — with Screener and broker research used as secondary sources and cross-checks

I developed the model and report with an AI-assisted workflow, then reviewed, challenged and validated every input, assumption and output: formula consistency across all forecast columns, three-statement ties in every scenario, and an independent recomputation of the DCF. It's the same discipline of structured validation I apply to research work day to day.

## Feedback

If you work in equity research, valuation or financial analysis, I'd value your perspective — especially on the assumptions. Open an issue or reach out on LinkedIn.

## Disclaimer
This is an independent educational project prepared from publicly available information. It is not issued by a SEBI-registered research analyst, is not investment advice, and is not an offer or solicitation to buy or sell any security. Information is believed reliable but is not guaranteed.

## License
Content is shared under [CC BY-NC 4.0]— free to use and adapt for non-commercial purposes, with attribution.
