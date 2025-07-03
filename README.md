# 📈 Stock Market Regime Detection using Hidden Markov Models 📈

This project applies **unsupervised machine learning**,  specifically **Hidden Markov Models (HMMs)** to detect **hidden market regimes** (e.g., bull vs bear markets) using historical price data of the S&P 500 (SPY ETF). It also demonstrates how regime detection can guide a simple **risk-on/risk-off trading strategy**.

---

## Project Overview

Traditional financial models often assume markets are stable over time — but in reality, they go through distinct phases or "regimes." This project aims to:

- Detect hidden market regimes using **HMMs**
- Engineer features like log returns, volatility, and momentum
- Label each time period with a regime (e.g., bull, bear, neutral)
- Build a **strategy** that only invests during favorable regimes
- Compare performance vs buy-and-hold benchmark
![1st](https://github.com/user-attachments/assets/e67fa97b-f719-4c08-83ca-c633f30636ba)
![2nd](https://github.com/user-attachments/assets/9c149e16-920d-40e8-b74a-affab13d6075)

---

##  Tools & Technologies

- Python 
- `yfinance` for historical data
- `hmmlearn` for HMM modeling
- `pandas`, `numpy` for data manipulation
- `matplotlib`, `seaborn` for visualization
- Jupyter Notebook (Google Colab compatible)

---

## Features Used

- Log returns
- Rolling volatility
- Price momentum
- Regime mapping based on predicted HMM states

---

##  Strategy Logic

The backtest applies a simple rule:
- **Invest only in regimes that appear historically profitable**
- **Stay in cash** (or reduce exposure) during bearish regimes

Returns are compared with a passive buy-and-hold portfolio.

---

##  Results

- The model successfully segments the market into distinct behavioral regimes.
- While the default model avoids some downturns, it may underperform buy-and-hold without tuning.
- You can improve results by adjusting:
  - Number of regimes
  - Feature set
  - Strategy rules
![last](https://github.com/user-attachments/assets/6d7ba8f4-c54b-4d8b-9825-11734f6e0661)

---
