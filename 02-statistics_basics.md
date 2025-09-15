# 02 — Statistics: returns, mean, variance, covariance, correlation

## 1. Formulas
Given series \(r_1,\dots,r_n\):
- Sample mean:
  \[
  \bar r = \frac{1}{n}\sum_{i=1}^n r_i.
  \]
- Sample variance:
  \[
  s^2 = \frac{1}{n-1}\sum_{i=1}^n (r_i - \bar r)^2.
  \]
- Sample covariance between X and Y:
  \[
  \mathrm{Cov}(X,Y) = \frac{1}{n-1}\sum (x_i-\bar x)(y_i-\bar y).
  \]
- Correlation:
  \[
  \rho_{XY} = \frac{\mathrm{Cov}(X,Y)}{s_X s_Y}.
  \]

## 2. Manual numeric example (follow this step-by-step)
Prices TSLA: 100, 105, 98, 101  
Prices QQQ: 200, 202, 198, 201

Step A — compute log-returns \(r_{t}=\ln(P_t/P_{t-1})\):
- TSLA returns: ln(105/100)=0.0488, ln(98/105)=-0.0697, ln(101/98)=0.0302
- QQQ returns: ln(202/200)=0.00995, ln(198/202)=-0.0198, ln(201/198)=0.0151

Step B — compute sample means \(\bar r_{TSLA}\), \(\bar r_{QQQ}\).

Step C — compute covariance and correlation using formulas above.

(Do each step in a spreadsheet; commit your manual results as a small CSV `data/manual_example.csv`.)

## 3. Interpretation
- High variance in TSLA + moderate positive covariance with QQQ implies hedging by shorting some QQQ reduces variance (derive in next file).
