# AI Sentiment Stock Market Trader

An AI-powered trading system that integrates **Reinforcement Learning (SARSA)** with **financial news sentiment analysis** to automate stock trading. Built with real-time data ingestion, backtesting, and live execution using the **Alpaca trading API**, this solution demonstrates an end-to-end ML pipeline for intelligent trading strategies.

---

## 👤 Authors

- **Ndubuisi Godcares Chibuokem**  
- **Najeeb Saiyed**

---

## 🧠 Overview

This project implements a sentiment-aware trading bot that:

- Analyzes financial news using [FinBERT](https://arxiv.org/abs/2006.08097#:~:text=In%20this%20work%2Cwe%20address%20the%20need%20by%20pretraining,advantage%20of%20FinBERT%20over%20generic%20domain%20BERT%20model.) to gauge sentiment on stock-related news.
- Uses a **SARSA (State-Action-Reward-State-Action)** algorithm to learn optimal buy/sell/hold strategies.
- Integrates with **Alpaca Markets API** to fetch real-time stock prices and execute trades.
- Leverages **QuantStats** for strategy performance evaluation via historical backtesting.

---

## 📦 Features

- **Reinforcement Learning**: SARSA-based RL agent adapts trading strategies from reward feedback.
- **Sentiment Analysis**: Real-time classification of financial news using FinBERT.
- **Backtesting Engine**: Simulates performance using historical data (via Yahoo Finance).
- **Risk Management**: Includes position sizing, stop-loss, and take-profit mechanisms.
- **Live Trading Support**: Executes trades securely through Alpaca.

---

## 🧱 System Architecture

![diagram-export-9-30-2024-7_56_33-PM](https://github.com/user-attachments/assets/2d03325f-891e-4a48-ae69-d7adaec90c41)
```

## 📈 Backtesting Results

Backtested on historical data from **2020 to 2024**, benchmarked against the S&P 500 (SPY):

| Metric                    | Value     |
|--------------------------|-----------|
| Cumulative Return        | 80.81%    |
| SPY Benchmark Return     | 79.08%     |
| Annualized Return (CAGR) | 9.35%%     |
| Sharpe Ratio             | 0.47      |
| Max Drawdown             | -27.06%    |

> Detailed performance reports generated using **QuantStats**.

---

## 🛠 Setup & Installation

```bash
git clone https://github.com/iamzayd/AI-Sentiment-Stock-Market-Trader.git
cd AI-Sentiment-Stock-Market-Trader
pip install -r requirements.txt
```

### Configure API Credentials

Create an account at [Alpaca](https://alpaca.markets/) and add your keys to `config.py`:

## API Keys

1. Create an account with [Alpaca](https://alpaca.markets/) to obtain API keys.

2. Add your Alpaca API keys to the respective scripts (`news_classified.py` and `SARSA1.py`).

   Make sure to update the API credentials in both scripts:
   - **news_classified.py**: Insert your API key and secret for fetching news.
   - **SARSA1.py**: Insert your API key and secret for executing trades.
```python
ALPACA_API_KEY = 'your-api-key'
ALPACA_SECRET_KEY = 'your-secret-key'
```

---

## ▶️ Usage

### 1. Run Sentiment Classifier
```bash
python news_classified.py
```

### 2. Run SARSA Agent
```bash
python SARSA1.py
```

---

## 📂 Repository Structure

```bash
.
├── news_classified.py       # News sentiment classification with FinBERT
├── SARSA1.py                # Reinforcement Learning SARSA trading logic
├── backtest.py              # Backtest engine for historical simulation
├── config.py                # API credentials and config
├── requirements.txt         # Project dependencies
├── tearsheet.html           # QuantStats report
└── README.md                # Project documentation
```

---
## 📈 Strategy Performance

### ✅ Cumulative Return vs. SPY Benchmark
![image](https://github.com/user-attachments/assets/3bf10715-bb39-47a7-8daf-a4c90c1a0be4)

--- 

## 📌 Future Enhancements

- Extend sentiment sources (e.g., Reddit, Twitter)
- Upgrade RL agent to Deep Q-Network (DQN) or PPO
- Add portfolio management for multi-asset trading
- Streamlit dashboard for real-time monitoring

---

## 🙏 Acknowledgements

- [FinBERT by Prosus AI](https://github.com/ProsusAI/finBERT)
- [Alpaca Markets](https://alpaca.markets/)
- [QuantStats](https://github.com/ranaroussi/quantstats)

---
