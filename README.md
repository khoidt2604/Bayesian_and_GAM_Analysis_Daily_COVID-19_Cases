# 📈 Bayesian and GAM Analysis of Daily COVID-19 Cases

This repository contains my R code and analysis for modelling daily COVID-19 case numbers using Bayesian methods and generalized additive models (GAMs), completed as part of a FIT3154 academic assignment.

---

## 📌 Introduction

This project explores statistical modelling techniques for daily COVID-19 case data. The analysis is divided into two main parts.

The first part focuses on Bayesian inference, where a half-Cauchy prior is used to study posterior behaviour, MAP estimates, and prior sensitivity. The second part applies generalized additive models and gamma regression to model daily case trends over time and compare predicted values against observed data.

The project demonstrates how different modelling assumptions can influence parameter estimation and predictive performance.

---

## 💡 Motivation

Daily case data often shows non-linear patterns, changing variability, and strong time-related effects. Because of this, it is useful to apply models that can both incorporate prior beliefs and capture flexible trends in the data.

This project was motivated by the need to better understand:
- how prior distributions affect Bayesian estimates
- how daily case counts can be modelled using smooth functions of time
- how different regression approaches compare when fitting real-world epidemic data

---

## 📊 Key Visualisations

### 1. Transformed Half-Cauchy Prior for Different Scale Values

![Transformed Half-Cauchy Prior for Different s Values](Screenshot%202026-04-10%20at%2012.15.57%E2%80%AFam.png)

This figure shows how the transformed half-Cauchy prior changes for different values of the scale parameter `s`. Smaller values of `s` produce a more concentrated prior, while larger values create a broader and less informative prior. This helps illustrate how prior choice affects Bayesian modelling assumptions.

### 2. Daily Cases and Model Predictions

![Daily Cases and Model Predictions](Screenshot%202026-04-10%20at%2012.16.11%E2%80%AFam.png)

This visual compares the observed daily case numbers with predictions from both Gamma and Gaussian GAM models. Both models follow the overall trend closely, but the Gamma model appears better suited to the non-negative and slightly skewed nature of the case data.

### 3. Observed vs Predicted Daily Case Numbers

![Observed vs Predicted Daily Case Numbers](Screenshot%202026-04-10%20at%2012.16.28%E2%80%AFam.png)

This plot compares observed case counts with predictions from the gamma regression approach. The model captures the overall rise, peak, and decline in cases reasonably well, showing that it can reflect the main structure of the data even if some local fluctuations remain.

---

## 🔍 Project Highlights

- Applied Bayesian analysis using a half-Cauchy prior
- Examined posterior mean, credible intervals, and MAP estimation
- Investigated sensitivity of MAP estimates to different scale parameters
- Visualised transformed prior distributions under multiple prior settings
- Built Gamma and Gaussian generalized additive models (GAMs)
- Compared observed and predicted daily COVID-19 case numbers
- Implemented gamma regression and gradient descent-based modelling

---

## 🧪 Methods Used

### Bayesian Methods
- Posterior analysis using half-Cauchy prior
- MAP estimation
- Prior sensitivity analysis
- Credible interval interpretation

### Regression and Smoothing Methods
- Generalized Additive Model (GAM)
- Gamma regression with log link
- Gaussian GAM with log link
- Polynomial-based gamma regression
- Gradient descent for gamma regression

---

## 🛠️ Tools and Libraries

- **R**
- **ggplot2**
- **mgcv**
- **data.table**

---

## 📁 Files

- `Assignment2_FIT3154.Rmd` — main R Markdown file containing the full analysis
- `Screenshot 2026-04-10 at 12.15.57 am.png` — transformed half-Cauchy prior visualisation
- `Screenshot 2026-04-10 at 12.16.11 am.png` — observed cases with Gamma and Gaussian GAM predictions
- `Screenshot 2026-04-10 at 12.16.28 am.png` — observed vs predicted daily case numbers

If you also upload the supporting datasets and helper scripts, you may include:
- `gamma.hc.2024.csv`
- `covid.cases.ass1.2024.csv`
- `cases.12.weeks.2024.csv`
- `gamreg.test.csv`
- `gamma.hc.map.R`
- `gamreg.gd.R`

---

## ▶️ How to Run the Code

1. Open the `.Rmd` file in **RStudio**
2. Make sure the required datasets and helper scripts are in the same working directory
3. Install the required packages if needed
4. Knit the file or run the code chunks step by step

```r
install.packages(c("ggplot2", "mgcv", "data.table"))
