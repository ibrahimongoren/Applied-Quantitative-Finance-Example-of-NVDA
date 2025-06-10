# **Applied Quantitative Finance: NVIDIA (NVDA) Stock Analysis**

This repository contains an advanced, interactive, and modular notebook focused on the **quantitative financial analysis** of NVIDIA Corporation (ticker: `NVDA`). The notebook demonstrates how to combine fundamental financial data, time-series analysis, volatility modeling, and risk simulation using Python-based tools and libraries.

---

## **Project Structure & Scope**

### 1. **Fundamental Dashboard**
This section gathers essential company-specific data using `yfinance`. It includes:
- **CAPM Beta** and company metadata
- **Shareholding Structure** (major, institutional, and mutual fund holders)
- **Dividend & Stock Split History**
- **Financial Statements** (Income Statement, Balance Sheet, Cash Flow)
- **Recent News** and headlines

> All data is retrieved programmatically and displayed in an interactive **tabbed view** for easy navigation and comparison.

---

### 2. **Exploratory Data Analysis (EDA)**

#### ❯ Configuration
- **Stocks Analyzed:** NVDA, MSFT, AMD, INTC, ADBE
- **Time Period:** 2020-01-01 to 2025-06-05
- **Frequency:** Daily (1d)
- **Source:** Yahoo Finance

#### ❯ Data Prepared
- **Adjusted Close Prices** (dividend & split-adjusted)
- **Simple Returns:**  
  \( R_t = \frac{P_t}{P_{t-1}} - 1 \)
- **Log Returns:**  
  \( r_t = \ln\left(\frac{P_t}{P_{t-1}}\right) \)

Each return series is analyzed structurally and visually for missing values, distributional properties, and volatility.

---

## **Time-Series Modeling**

### 3. **Volatility Models**

#### ❯ AR(1)-GARCH(1,1)
- Fitted with **Student’s t-distribution**
- Captures volatility clustering and heavy tails

#### ❯ EGARCH(1,1)
- Captures asymmetry in volatility shocks
- Incorporates leverage effects

#### ❯ Outputs
- Daily conditional volatility forecast
- 10-day ahead simulations with confidence bounds
- Inter-model comparison based on RMSE, MAE, AIC/BIC

---

## **Risk Management**

### 4. **Monte Carlo Simulation & VaR/CVaR**
- Parametric simulation of return paths
- 1% and 5% **Value at Risk (VaR)** estimation
- **Conditional VaR (CVaR)** for tail-risk modeling
- **Kupiec Test** for statistical backtesting

> Results are visualized with interactive plots and explained with financial intuition.

---

## **Diagnostics & Validation**

- **Residual Diagnostics:** Ljung-Box, Q-Q plots
- **Normality Tests:** Jarque-Bera, Shapiro-Wilk
- **Model Validity:** Distribution fits and volatility forecasts
- **Rolling Windows:** Robustness checks over time

---

## **Visualization Tools**

All plots are generated with `plotly`, allowing:
- Interactive zoom and pan
- Hover tooltips
- Annotated charts for model interpretation
- Dynamic subplots with shared x-axis for comparative view

---

## **Key Libraries Used**

- `pandas`, `numpy`
- `yfinance`
- `statsmodels`
- `arch`
- `scipy`, `matplotlib`, `plotly`

---

## **Use Cases**

This notebook is ideal for:
- Financial Econometrics Projects
- Academic Thesis & Research
- Quantitative Risk Analysis
- Algorithmic Trading Pipeline
- Time-Series Forecasting & Backtesting

---

## **File Structure**

```plaintext
📦 Applied_Quantitative_Finance_NVDA.ipynb
├── 📊 Fundamental Dashboard (Tabs)
├── 🧮 Return Calculation & EDA
├── 📈 GARCH/EGARCH Modeling
├── 🔁 Forecasting & Simulation
├── ⚠️ Risk Metrics (VaR, CVaR)
├── 🧪 Diagnostics & Backtesting
├── 📈 Technical Analysis
```

---

## **Reference**

This notebook is based on methods and examples presented in:

> **Aleš Kresta** (2024). *Applied Quantitative Finance in Python: Selected theories and examples*. [ResearchGate](https://www.researchgate.net/publication/386032446_Applied_Quantitative_Finance_in_Python_Selected_theories_and_examples)

Please cite this work accordingly if you use or modify the notebook for academic or professional purposes.
