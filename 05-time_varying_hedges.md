# 05 — Time-varying hedges: rolling windows & state-space (Kalman) sketch

## 1. Rolling beta
Compute covariance and variance over a rolling window of length W:
\[
\beta_t^\text{rolling} = \frac{\mathrm{Cov}_t(r_A,r_H;\,W)}{\mathrm{Var}_t(r_H;\,W)}.
\]
This reacts to regime changes (volatility shifts). Choose W (e.g., 21 days, 63 days) and compare.

## 2. Kalman filter idea (high-level math)
Model time-varying β_t as a hidden state:
- State equation: \(\beta_{t+1} = \beta_t + \eta_t\) with \(\eta_t\sim N(0,q)\).
- Observation: \(r_{A,t} = \beta_t r_{H,t} + \epsilon_t\) with \(\epsilon_t\sim N(0,r)\).

Kalman filter gives sequential updates:
- prediction of β_{t+1}
- update with new observation r_{A,t+1}

In practice, this produces a smooth, adaptive β estimate that downweights noise.

## 3. When to use which
- Rolling: simple, easy to explain.
- Kalman: better when true β drifts slowly; requires choosing process noise q.

## 4. Manual exercise
- Using the numeric example, compute β over two window sizes (W=2, W=3) and observe differences.
