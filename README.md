# Comparing-the-Risk-Performance-of-UMVU-and-MLE-Estimators-Under-Squared-Error-Loss

# 📊 Risk Comparison: UMVU vs MLE Estimators for θ(1 - θ)

This project compares the **UMVU (Uniformly Minimum Variance Unbiased)** estimator and the **MLE-based (Maximum Likelihood Estimator)** for estimating the quantity θ(1 - θ), where X follws Bin(n, θ). We explore how each estimator performs in terms of **risk** (mean squared error) under varying values of \(\theta\) and sample size \(n\).

---

## ✏️ Estimators Being Compared

### ✅ UMVU Estimator (Unbiased)
The unbiased and minimum variance estimator among all unbiased estimators:
δ*(X) = [X(n - X)] / [n(n - 1)]

### ✅ MLE-based Estimator (Biased)
δ(X) = [X(n - X)] / n²

The MLE is biased for finite samples but often has lower variance, which can lead to better overall performance in terms of risk.

---

## 🔍 What This Project Does

- Computes the **risk** (mean squared error) of each estimator for:
  -  θ = {0.05, 0.10, ...., 0.95}
  - n = {5, 15, 30, 45}
- Compares risks across estimators using:
  - Direct risk plots
  - Risk ratio plots Risk Ratio:  [ R(δ*) ] / [ R(MLE) ]
  - A summary comparison table
- Shows how estimator performance changes as sample size increases

---

## 📈 Key Findings

- **MLE outperforms UMVU** at most \(\theta\) values when sample size is small
- **UMVU only performs better near \(\theta = 0.5\)** and becomes more competitive as n increases
- The **risk ratio plots** show that the UMVU estimator has lower risk than MLE only in the central region of θ, never across the full range

---



## 📌 Requirements

This project uses standard R libraries:

- `ggplot2`
- `dplyr`
- `reshape2`
- `knitr`

You can install them using:

```r
install.packages(c("ggplot2", "dplyr", "reshape2", "knitr"))
