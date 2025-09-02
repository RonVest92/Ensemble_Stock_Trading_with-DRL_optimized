# 📈 All-Ensemble Deep Reinforcement Learning Stock Trading

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yourusername/all-ensemble-stock-trading/blob/main/notebooks/New_Ensemble_StockTrading_2024.ipynb)

## 📌 Overview
This project implements an **ensemble-based Deep Reinforcement Learning (DRL) trading strategy** for the **Dow 30** stocks using the [FinRL](https://github.com/AI4Finance-Foundation/FinRL) framework.  
It trains multiple DRL agents — **PPO, DDPG, TD3, SAC, and A2C** — and dynamically selects the best-performing agent based on **Sharpe ratio** during validation.  
The selected agent is then deployed for **out-of-sample trading** and evaluated against the **Dow Jones Industrial Average (DJIA)** benchmark.

---

## 🎯 Objectives
- Automate multi-stock trading using DRL agents.
- Compare multiple DRL algorithms and select the best performer dynamically.
- Incorporate **transaction costs** and **technical indicators** for realistic performance.
- Backtest against a market benchmark to evaluate strategy robustness.

---

## 📊 Dataset
- **Source**: Yahoo Finance API
- **Assets**: Dow 30 constituents
- **Period**: 2009-01-01 to 2024-10-17
- **Features**:
  - OHLCV data
  - Technical indicators: MACD, Bollinger Bands, RSI, CCI, DX, SMA(30), SMA(60)
  - Turbulence index for market risk

---

## 🛠️ Methodology
1. **Data Collection & Preprocessing**
   - Download historical stock data from Yahoo Finance.
   - Compute technical indicators and turbulence index.
2. **Environment Setup**
   - Define state space, action space, and reward function.
3. **Agent Training**
   - Train PPO, DDPG, TD3, SAC, and A2C on in-sample data.
4. **Ensemble Selection**
   - Evaluate agents on validation data.
   - Select the agent with the highest Sharpe ratio.
5. **Backtesting**
   - Deploy the selected agent on out-of-sample data.
   - Compare performance against DJIA benchmark.

---

## 📈 Results Summary
| Metric              | Ensemble Strategy | DJIA Benchmark |
|---------------------|------------------:|---------------:|
| Annual Return       | 21.12%            | 18.03%         |
| Sharpe Ratio        | 1.92              | 1.64           |
| Sortino Ratio       | 3.08              | 2.42           |
| Max Drawdown        | -7.94%            | -9.02%         |

---

## 📊 Performance Plot
![Backtest Performance](results/backtest_performance.png)  
*Example: Replace with your actual backtest plot from the `results/` folder.*

---

## 🚀 How to Run

### **Option 1: Google Colab**
1. Click the **"Open in Colab"** badge at the top.
2. Install dependencies.
3. Run all cells sequentially.

### **Option 2: Local Environment**
```bash
# Clone the repository
git clone https://github.com/yourusername/all-ensemble-stock-trading.git
cd all-ensemble-stock-trading

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook notebooks/New_Ensemble_StockTrading_2024.ipynb
```

---

## 📦 Requirements
```
finrl
stable-baselines3
pandas
numpy==1.23.5
matplotlib
stockstats
tensorflow
gymnasium
pyfolio-reloaded
yahoo-finance-api
```

---

## 🔮 Future Improvements
- Integrate live trading via broker APIs (e.g., Alpaca, Interactive Brokers).
- Add more DRL algorithms for comparison.
- Implement hyperparameter optimization.
- Expand to global equity indices and ETFs.

---

## 📜 License
This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements
- [FinRL](https://github.com/AI4Finance-Foundation/FinRL) for the DRL trading framework.
- Yahoo Finance API for historical market data.
- Stable-Baselines3 for DRL algorithm implementations.
```

