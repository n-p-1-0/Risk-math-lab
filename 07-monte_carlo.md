# 07 — Monte-Carlo forward scenarios (math first)

## 1. Geometric Brownian Motion (GBM)
Standard model for price S(t):
\[
dS_t = \mu S_t dt + \sigma S_t dW_t,
\]
Discrete Euler approximation for daily steps Δt:
\[
S_{t+\Delta t} \approx S_t \exp\left((\mu-\tfrac{1}{2}\sigma^2)\Delta t + \sigma \sqrt{\Delta t}\ z\right),\quad z\sim N(0,1).
\]

## 2. Monte-Carlo for hedging
Simulate many paths for asset and hedge (correlated normals), compute hedged portfolio return each path, then obtain distribution of outcomes → compute VaR/CVaR from simulated losses.

## 3. Manual math exercise (conceptual)
- Suppose μ=0.05, σ=0.2, Δt=1/252. Simulate 1-step log-return mean and variance via formulas; compute probability of >5% daily loss under the normal approximation.

## 4. Notes about jumps
To capture crashes, add a Poisson jump term (Merton jump-diffusion). This complicates analytics — explain it, but not necessary for initial project.
