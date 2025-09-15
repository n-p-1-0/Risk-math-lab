# Risk Math Lab — math-first exploration of hedging & tail risk

**Author:** Nolan Price (Center Grove High School, junior)  
**Purpose:** A math-first, transparent notebook project that studies **hedging, volatility, VaR/CVaR, and tail risk** using clear formulas and small numeric examples. This repository is intentionally math- and statistics-centered (not a coding bootcamp). My goal: produce reproducible, explainable quant math that local stakeholders (farmers, small businesses, civic groups) can use to reduce real risk.

## Why math-first?
Many hedging tools fail in crises because they assume normality or fixed correlations. This project:
- derives hedge ratios analytically,
- compares historical vs parametric VaR,
- studies extreme-tail models (EVT),
- tests time-varying hedges conceptually (rolling and state-space),
- and produces short, actionable case studies.

## File map (start here)
- `01-probability.md` — random-walk, price ticks, expectation basics.
- `02-statistics_basics.md` — returns, variance, covariance, correlation, manual examples.
- `03-hedging_math.md` — OLS hedge derivation, optimization hedge, analytic examples.
- `04-var_cvar.md` — historical VaR, parametric VaR (normal), CVaR formula and examples.
- `05-time_varying_hedges.md` — rolling beta + Kalman filter (math sketch).
- `06-stress_and_evt.md` — stress test design and EVT (POT) basics.
- `07-monte_carlo.md` — GBM and jump-diffusion basics and Monte-Carlo math.
- `08-case_studies.md` — real-world case templates (stocks, commodities, small business).
- `09-outreach.md` — email templates, one-page summary template for stakeholders.
- `DISCLAIMER.md` — legal/ethical note.

## How to use this repo
1. Read the math files in order.  
2. Do the small numeric exercises (spreadsheet or hand calculation) — they are the point.  
3. If you want to run numbers, see the `Appendix — optional scripts` section in each file for tiny, drop-in Python (purely optional).

---

**Contact:** nolangp10@icloud.com