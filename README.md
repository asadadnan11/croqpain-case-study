# Croq'Pain Case Study: Optimizing Store Locations with Regression

An applied business analytics project that uses multivariate regression modeling to predict store performance and recommend ideal locations for French restaurant chain **Croq’Pain** to expand in 1996.

---

## Project Summary

### Objective
**Goal:** Identify optimal locations for new Croq’Pain stores by correcting errors in the original regression model and predicting store performance with an improved linear model.

---

## Problem & Solution

### Original Model Issues
- **Multicollinearity:** Highly correlated explanatory variables (P15, P35, P45) distorted the original regression.
- **Heteroskedasticity:** Residuals violated homoscedasticity, suggesting inconsistency in model variance.
- **Insignificant Variables:** Too many variables with high p-values were included, reducing model efficiency.

---

### Improved Model
We refined the model using:
- New explanatory variables:
  - Capital investment (`K`)
  - Average income (`INC`)
  - Natural log of store size (`log(SIZE)`)
  - Natural log of non-restaurant competitors (`log(NREST)`)
  - Natural log of total population (`log(total)`)
- Diagnostic testing to confirm:
  - Normal distribution of errors
  - No multicollinearity (VIF < 5)
  - Homoscedasticity of residuals
  - No autocorrelation

---

## Results & Recommendations

- **Model Performance:**
  - R-squared: **0.8016**
  - Adjusted R-squared: **0.7848**

- **New Store Location Recommendations:**
  - Toulouse: 42.1% projected performance ratio
  - Montpellier: 31.9% projected performance ratio
  - Dijon: 34.6% projected performance ratio

---

## Validation Steps

1. **Multicollinearity Test:** Variance Inflation Factor (VIF) values below 5 ensured no collinearity.
2. **Residual Analysis:** Homoscedasticity confirmed using residual vs. fitted plots.
3. **Autocorrelation Test:** Durbin-Watson test confirmed absence of autocorrelation.
4. **Performance Ratio Prediction:** Applied the improved model to 50 stores opened before 1994 and validated predictions on 10 new stores opened in 1994.

---

## Files in Repository

- `CroqPain_Case_Study.qmd` — Original analysis and model building process
- `CroqPain_Executive_Summary.pdf` — Annotated executive summary with findings
- `datasets/` — Cleaned dataset for replication

---

## Authors

**Asad Adnan**, Charley Conroy, Elisabeth Gangwer, Yun-Shiuan Hsu  
*Master's in Business Analytics, University of Notre Dame*

---

## References
- Original dataset from Croq'Pain's internal historical data
- Case study part of the **Business Analytics Capstone Project** at Notre Dame
