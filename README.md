# derivatives-structured-products-python
 Black–Scholes delta-hedging simulations, moneyness impact, inflation curve calibration + pension liability PV/hedging, and CDS curve bootstrapping/valuation (FinancePy, Python).

# Derivatives & Structured Products Coursework 

## Overview
This repository contains our EDHEC M2 Derivatives & Structured Products coursework (Academic Year 2025–26).
We implemented pricing/risk tasks in Python (FinancePy) and documented results in a formal report.

**Main deliverables**
- Question (PDF): `assignment_2025_dsp.pdf`
- Report (PDF): `DSP_Coursework_Group13_Report.pdf`
- Code (notebook): `DSP_Coursework_Group13_code_as_jupyter_notebook.ipynb`
- Code (HTML, easy to view on GitHub): `DSP_Coursework_Group13_code_as_html_file.html`

## What we built (by question)
### Q1 — Black–Scholes delta hedging (simulation)
- Simulated delta-hedging of a European put under GBM with a self-financing replicating portfolio.
- Compared replication error under different hedge frequencies (monthly/weekly/daily).
- Studied how error relates to terminal price and realized volatility.

### Q2 — Moneyness impact (ITM vs ATM vs OTM)
- Repeated the Q1 experiment for in-the-money and out-of-the-money puts.
- Compared distributions of hedging error and discussed implications for hedging difficulty / smile intuition.

### Q3 — Inflation markets + pension liabilities
- Calibrated an inflation curve from zero-coupon inflation swaps (CPI base month Aug-2025).
- Produced forward CPI levels via log-linear interpolation.
- Computed inflation PV01 and valued a real-liability profile in nominal and real terms.
- Discussed practical hedging using nominal IR instruments and inflation-linked instruments.

### Q4 — CDS valuation & risk
- Bootstrapped a CDS curve from market quotes (assumed recovery 40%).
- Computed a par spread for a 4Y maturity and valued an off-market CDS position.
- Computed bucketed sensitivity (CS01-style) and discussed dealer hedging intuition.

## Key results (highlights)
- Delta-hedging: mean replication error ~0, while error variance decreases materially as hedge frequency increases.
- Realized volatility explains a meaningful share of hedging error when hedging with a constant-vol Black–Scholes delta.
- Inflation: produced a market-implied CPI curve, PV01 by maturity, and nominal vs real PV of liabilities.
- CDS: computed par spread for the target maturity and marked-to-market a long-protection position vs market.

## How to view quickly (recruiter-friendly)
- Read the report first (final narrative): `report/DSP_Coursework_Group13_Report.pdf`
- If you want to skim the code without running anything: open the HTML export in `notebooks/`.
