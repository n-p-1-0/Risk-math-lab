# 04 — VaR & CVaR (definitions + math)

## 1. Historical VaR
Given a return series \(r_1,\ldots,r_n\) sorted ascending, historical VaR at level α (e.g., 5%) is:
\[
\text{VaR}_\alpha^\text{hist} = -\text{quantile}_\alpha(r).
\]
Interpretation: with probability \(1-\alpha\), loss will not exceed VaR.

## 2. Parametric (Normal) VaR
If \(r\sim N(\mu,\sigma^2)\), the one-period VaR at level α:
\[
\text{VaR}_\alpha^\text{norm} = -\left(\mu + z_\alpha \sigma\right),
\]
where \(z_\alpha\) is the α-quantile of standard normal (e.g., \(z_{0.05}\approx -1.645\)).

Be careful with signs: VaR is typically reported as a positive loss number.

## 3. CVaR (Expected Shortfall)
CVaR at α is the average loss beyond the VaR threshold:
\[
\text{CVaR}_\alpha = -\mathbb{E}[r \mid r \le \text{quantile}_\alpha(r)].
\]

## 4. Manual example (small sample)
Using the returns from 02:
- Sort returns ascending.
- If n=100 and α=0.05, VaR is the 5th smallest return (empirical). For small n, use interpolation.

Compute both VaR and CVaR for unhedged and hedged returns and compare.

## 5. Why CVaR matters
CVaR captures tail severity, not just threshold. Hedging may reduce VaR but not CVaR if tail shape remains heavy.
