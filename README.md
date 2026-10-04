# Crocs, Inc. (CROX): Equity Valuation, LBO & M&A Analysis

**Initiation of coverage: BUY, 12-month price target $190, price $118.54 (30-Sep-2026), +60% upside**

An equity research case study on Crocs built from primary SEC filings: a three-statement operating model, intrinsic and relative valuation, an LBO, a merger model, a HEYDUDE impairment test, and a Monte Carlo risk analysis.

## Files

| | |
|---|---|
| [`CROX_Valuation_Model.xlsx`](CROX_Valuation_Model.xlsx) | 24-sheet Excel model: integrated statements FY21A-FY35E, Base / Bull / Bear scenarios, DCF, comps, precedents, LBO, merger and HEYDUDE analysis |
| [`CROX_Initiation_of_Coverage.pdf`](CROX_Initiation_of_Coverage.pdf) | Initiation report in sell-side format |
| [`CROX_Python_Analysis.ipynb`](CROX_Python_Analysis.ipynb) | Python analysis: SEC data and tie-out to the model, betas and WACC, comps regression, an independent DCF check, Monte Carlo and tornado |

## Results

| Method | Value / share |
|---|---|
| DCF (FCFF), Base / Bull / Bear | $223 / $307 / $114 |
| DCF, probability-weighted (20 / 50 / 30) | $207 |
| FCFE / residual income / justified P/E | $217 / $193 / $186 |
| Trading comps: EV/EBITDA (IFRS 16) / forward P/E | $163 / $190 |
| Precedent transactions (control) | $190 |
| LBO: maximum price at a 20% sponsor IRR | $150 |
| Monte Carlo P10 / median / P90 (10,000 paths) | $97 / $195 / $297 |
| **Price target** (50% probability-weighted DCF, 25% each comps method) | **$190** |

**The thesis.** Crocs trades at 7.1x EV/EBITDA with a 12.8% FCF yield. The reverse DCF shows the price assumes revenue falling 4.3% a year to FY30. The Bear case, where a fashion fade spreads to the core clog, is worth roughly today's price.

## The model

- **History.** FY2021-FY2025 statements and segment revenue from the 10-K/10-Q filings; management's non-GAAP adjustments rebuilt from the earnings releases, with recurring "one-offs" kept in EBIT.
- **Operating model, FY26E-FY35E.** Six revenue lines with a units x ASP cross-check; working capital, PP&E, leases and book vs cash tax; debt schedule with Term Loan B sweep, revolver and refinancing; buybacks at a constant P/E; FY26E calibrated to guidance.
- **Valuation.** CAPM WACC; FCFF DCF with an H2-26 stub and mid-period discounting; FCFE, residual income, justified P/E and sum of the parts; reverse DCF (Goal Seek); sensitivities as data tables.
- **Relative value.** Comps across the US, UK/Europe and India on an IFRS 16 basis, and precedent transactions.
- **Transactions.** LBO (sources and uses, cash sweep, IRR/MOIC, value bridge, maximum price by target IRR), Deckers x Crocs accretion/dilution, HEYDUDE return on capital and ASC 350 impairment test.

## Running the notebook

Keep the notebook next to the workbook, then:

```
pip install pandas numpy matplotlib openpyxl statsmodels yfinance jupyter
jupyter notebook CROX_Python_Analysis.ipynb
```

It downloads data from SEC EDGAR and Yahoo Finance (set `SEC_USER_AGENT` in the first cell to your name and e-mail, as the SEC requests).

*By Sidhant Thalor. Not investment advice. Market data as of 30 September 2026; financials through the 10-Q for the quarter ended 30 June 2026.*
