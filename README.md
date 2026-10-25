# SS-project-
# Sentiment-Driven Cryptocurrency Algorithmic Trading Bot

An end-to-end quantitative trading pipeline built in MATLAB that integrates **Natural Language Processing (NLP)** sentiment data, an **Econometrics** time-series predictive model (ARIMAX), and **Financial Toolbox** portfolio backtesting to dynamically trade Bitcoin (BTC-USD).

---

## 👥 Project Members
* **Shivam Pagar** (Roll No: 24108B0035)
* **Yash Deokar**
* **Aryan Yadav**

**Institution:** Vidyalankar Institute of Technology  
**Coursework:** Quantitative Finance & Algorithmic Trading Systems

---

## 📊 Project Overview
This project explores whether tracking public social media sentiment can generate a reliable financial edge in cryptocurrency markets. Rather than relying solely on traditional technical indicators, the bot processes unstructured text sentiment, models its statistical relationship with price returns via an ARIMAX framework, and executes a tactical asset allocation strategy to maximize returns while mitigating drawdown during market panics.

---

## ⚙️ Core Architecture & Methodology

1. **Sentiment Ingestion & Aggregation (Text Analytics Toolbox):**
   - Parses scored social media text data (`crypto_sentiment_scored.csv`).
   - Maps and aggregates raw sentiment polarity scores across a continuous timeline to establish a daily quantitative market psychology metric.

2. **Synthetic Market Simulation & In-Memory Alignment:**
   - Generates an in-memory synthetic price stream simulating crypto volatility characteristics.
   - Implements strict matrix synchronization and explicit presample extraction (`Y0`) to eliminate dimension mismatches during model fitting.

3. **Time-Series Forecasting (Econometrics Toolbox):**
   - Employs an **ARIMAX(1,0,1)** model (`arima`) to quantify how past price returns and public sentiment predictors influence future market movements.

4. **Algorithmic Backtesting & Execution (Financial Toolbox):**
   - Utilizes `backtestStrategy` and `backtestEngine` to simulate a live execution environment.
   - **Tactical Rule:** Dynamically shifts portfolio weights between **100% long Bitcoin** (when daily average sentiment > 0) and **100% safe cash** (when sentiment drops below zero).

---

## 🗂️ Repository Structure
```text
├── final_bot.m                 # Main executable MATLAB script
├── crypto_sentiment_scored.csv # Processed NLP sentiment dataset
└── BTC-USD.csv                 # Historical asset price reference
