# Model guide

**File:** `model/TMCV_Equity_Research_Model.xlsx` · Excel, no macros · ₹ Cr unless stated · FY ends March

| Sheet | What it does |
|---|---|
| **Cover** | Investment summary, 12 automated model checks, contents, key assumptions, how-to, disclaimer |
| **Outputs** | Scenario switch (cell D7: 1 Bull · 2 Base · 3 Bear), dashboard, scenario data table, key financials and chart, DCF sensitivity grids, football field |
| **Inputs** | Company & market data, forecast drivers (Best / Base / Worst blocks), cost of capital, target-price settings, DCF settings, peer group, investment-thesis notes |
| **Model** | Income statement, balance sheet, cash flow, working-capital / fixed-asset / debt schedules, ratios, DCF, trading comparables, target price & rating |

## Conventions
- **Blue** = hard-coded input · **Black** = formula · **Light grey (F2F2F2)** = assumption cells to set or stress-test.
- Forecast cash is the balance-sheet plug from the cash-flow statement; interest uses average debt and other income uses opening cash and investments, so there is no circularity.
- Excel's data table (Outputs scenario table) recalculates in Excel only.

## Where the headline numbers live
| Item | Cell(s) |
|---|---|
| Rating, target, CMP, upside, target basis | Outputs D10–D14 |
| DCF value (12-month), DCF vs target, TV share | Outputs D16–D18 · detail Model rows 175–208 |
| Peer multiples and medians | Model rows 232–248 |
| Target build | Model rows 284–309 |
| Sensitivities | Outputs E78:I83 (WACC × g), E86:I91 (WACC × exit multiple) |
| Assumption rationale | Inputs D150–D160 |
