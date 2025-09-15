# 03 — Hedging math (static OLS hedge + optimization)

## 1. Problem: create a hedged portfolio
You hold 1 unit of asset A (returns \(r_A\)). You can short β units of hedge asset H (returns \(r_H\)). Hedged return:
\[
r_Hdg = r_A - \beta r_H.
\]

Goal: choose β to **minimize variance** of hedged return.

## 2. Derive optimal β (analytic)
Minimize:
\[
\mathrm{Var}(r_A - \beta r_H) = \mathrm{Var}(r_A) + \beta^2 \mathrm{Var}(r_H) - 2\beta\mathrm{Cov}(r_A,r_H).
\]
Differentiate w.r.t. β and set to zero:
\[
2\beta\mathrm{Var}(r_H) - 2\mathrm{Cov}(r_A,r_H) = 0
\]
So
\[
\boxed{\beta^\star = \frac{\mathrm{Cov}(r_A,r_H)}{\mathrm{Var}(r_H)}.}
\]
This is exactly the slope from OLS regression of \(r_A\) on \(r_H\).

## 3. Interpretation
- If β* > 1: hedge asset moves more per-dollar than A → need >1$ hedge per $1 of A.
- This is the **minimum-variance linear hedge** (works under linear assumptions).

## 4. Optimization variant (constrained)
If you can allocate weights \(w\) across n hedges with covariance matrix Σ, minimize portfolio variance:
\[
\min_w w^\top \Sigma w \quad \text{s.t. } \mathbf{1}^\top w = 1 \ (\text{or other constraint}).
\]
Lagrange method leads to linear system; see appendix for closed form for minimum-variance portfolio.

## 5. Manual numeric example (use outputs of `02` exercise)
- Using the covariance and var you computed above, compute β* numerically.
- Build hedged returns \(r_A - β^* r_H\) and compute sample variance; compare to unhedged variance.

## Appendix (optional) — relation to OLS
OLS slope when regressing \(r_A\) onto \(r_H\) equals β* above (assumes mean-zero residuals or use demeaned series).
