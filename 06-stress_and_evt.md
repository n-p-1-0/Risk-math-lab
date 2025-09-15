# 06 — Stress testing and Extreme Value Theory (EVT) basics

## 1. Stress testing (design)
- Historical scenario: pick crisis windows (e.g., March 2020) and recompute hedged/unhedged P&L.
- Synthetic shock: apply an instantaneous shock (e.g., -20% asset A, +shock to hedge) and compute new portfolio loss.

Deliverable: table showing loss under scenarios for both portfolios.

## 2. EVT (Peaks Over Threshold, POT) — sketch
Model exceedances over high threshold u with Generalized Pareto Distribution (GPD). If \(X\) are returns and \(Y=X-u\) for \(X>u\), then:
\[
\Pr(Y \le y \mid X>u) \approx 1 - \left(1 + \frac{\xi y}{\beta}\right)^{-1/\xi},\quad y>0.
\]
Parameters: shape ξ (tail heaviness) and scale β.

Interpretation: larger ξ → heavier tails → hedges need to account for rare, huge moves.

## 3. Practical note
EVT requires a substantial sample to estimate reliably; for small-sample high-school work, use EVT only as an illustrative concept and perform sensitivity checks.
