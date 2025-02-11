# 📊 Econometrics Project: Time Series Analysis & Forecasting

## Overview
This project focuses on **econometric modeling of financial time series**, analyzing stock price movements using statistical tests and models. The objective is to assess **stationarity, cointegration, Granger causality, and volatility clustering** in major stocks, providing insights into their long-term relationships and predictive capabilities.

The project consists of:
- **Data transformation** (log transformations & aggregation)
- **Stationarity & unit root testing**
- **Autoregressive Distributed Lag (ADL) modeling**
- **Cointegration vs. spurious regression analysis**
- **Granger causality tests**
- **(G)ARCH modeling for volatility forecasting**

## 📂 Project Setup
### Data
- **Time Frame:** August 2000 - August 2024
- **Stocks Analyzed:**
  - JPMorgan (lp1q)
  - Apple (lp2q)
  - PepsiCo (lp3q)
  - McDonald's (lp4q)

### Tools & Software
- **OxMetrics9** (primary)
- **Alternative options:** Python, R, STATA, MATLAB

## 🔍 Methodology

### 1️⃣ Data Transformation
- Converted daily stock prices into **quarterly averages**.
- Applied **natural logarithm transformation** to normalize volatility.

### 2️⃣ Stationarity Analysis
- Conducted **visual inspection** (time series plots, detrending, differencing).
- Applied **Augmented Dickey-Fuller (ADF) tests** to confirm stationarity.
- Found that **all stock prices were non-stationary at level but stationary after first-order differencing**.

### 3️⃣ Autoregressive Distributed Lag (ADL) Models
- Built **ADL(1) models** to assess lag effects between dependent (JPMorgan) and independent (McDonald's) variables.
- Evaluated **nine nested models** to check for misspecifications.
- The **Error Correction Model (ECM)** emerged as the best model, balancing short-run and long-run dynamics.

### 4️⃣ Cointegration vs. Spurious Regression
- Tested if **PepsiCo (lp3q) and McDonald's (lp4q) share a long-term relationship**.
- **Engle-Granger two-step procedure** found weak evidence of cointegration, suggesting shared trends rather than a robust equilibrium relationship.
- Results indicate a **spurious regression risk**, where apparent correlations may not imply true economic linkage.

### 5️⃣ Granger Causality Analysis
- Tested whether **McDonald’s (lp4q) stock movements "Granger-cause" other stock prices**.
- Results **failed to reject the null hypothesis**, implying that past McDonald's prices do not predict future movements in other stocks.

### 6️⃣ Volatility Modeling: (G)ARCH Models
- Tested for **ARCH effects** using Lagrange Multiplier (LM) tests.
- Applied **GARCH(1,1), GJR-GARCH, and EGARCH models** to capture volatility clustering.
- **EGARCH(1,1) with a Student’s t-distribution** was the best model for capturing asymmetric volatility behavior in McDonald's stock.
- **GARCH(1,1) was optimal for JPMorgan, Apple, and PepsiCo.**

## 📌 Key Findings
- **Stock returns are non-stationary but become stationary after first-order differencing.**
- **ADL modeling confirmed short-run dependencies, with ECM as the best model.**
- **No strong cointegration was found, suggesting that observed stock price correlations are not long-term equilibrium relationships.**
- **No Granger causality was detected among the selected stocks.**
- **Volatility clustering is present, with EGARCH performing best for asymmetric shocks.**

## 📬 Contact
For inquiries or collaboration, feel free to reach out:
- **Email:** [lollordp@gmail.com](mailto:lollordp@gmail.com)
- **LinkedIn:** [Lorenzo Rossi](https://www.linkedin.com/in/lorenzo-rossi01/)

