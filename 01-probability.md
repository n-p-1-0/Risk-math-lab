# 01 — Probability foundation for price ticks

## 1. Random walk model (discrete time)
Let \(P_t\) be price at discrete times \(t=0,1,2,\dots\). A simple random-walk model:
\[
P_{t+1} = P_t + \varepsilon_{t+1},
\qquad \mathbb{E}[\varepsilon_{t+1}]=0,\ \mathrm{Var}(\varepsilon_{t+1})=\sigma^2.
\]
This captures micro-price noise.

## 2. Returns and log-returns
Define simple return:
\[
R_t = \frac{P_t - P_{t-1}}{P_{t-1}}.
\]
Log-return:
\[
r_t = \ln\left(\frac{P_t}{P_{t-1}}\right) \approx R_t\ \text{for small }R_t.
\]

## 3. Expectation & variance (why they matter)
- Expected return \(\mu = \mathbb{E}[r_t]\).  
- Volatility \(\sigma = \sqrt{\mathrm{Var}(r_t)}\).

If \(\mu\) is near 0 and \(\sigma\) large, predicting short-term direction is hard → HFT strategies must rely on microstructure, not fundamentals.

## 4. Tiny exercise (do by hand or in a spreadsheet)
Given prices: 100, 102, 101, 103  
- Compute simple returns \(R_t\) for each step.  
- Compute mean return and sample variance.

(Answers are in `02-statistics_basics.md` as reference.)
