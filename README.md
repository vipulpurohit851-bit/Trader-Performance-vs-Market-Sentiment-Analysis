# 📊 Trader Performance vs Market Sentiment Analysis

## 📌 Overview
This project analyzes how market sentiment (Fear/Greed) impacts trader behavior and performance on Hyperliquid.

The goal is to identify patterns in trading activity and propose actionable strategies based on sentiment-driven insights.

---

## 📂 Datasets Used

1. **Bitcoin Market Sentiment**
   - Columns: timestamp, value, classification (Fear/Greed)

2. **Historical Trader Data (Hyperliquid)**
   - Includes: account, execution price, size, side, timestamp, PnL, etc.

---

## ⚙️ Methodology

- Cleaned and validated both datasets
- Converted timestamps to date format
- Merged datasets on daily level
- Created key metrics:
  - PnL (profit/loss)
  - Win rate
  - Trade size (USD)
  - Trade frequency
  - Long/Short distribution

> Note: Leverage data was not available; trade size is used as a proxy for risk exposure.

---

## 📊 Key Insights

- **Performance varies with sentiment**
  - Highest PnL during *Extreme Greed (~67.9)*
  - Lowest during *Neutral/Extreme Fear (~34)*

- **Trader behavior changes**
  - Larger trade sizes during Fear → higher risk-taking
  - Smaller trades during Extreme Greed → cautious behavior

- **Trading frequency impact**
  - Infrequent traders outperform frequent traders, especially during Greed

- **Directional bias**
  - SELL trades slightly dominate across most sentiment conditions

---

## 📈 Segmentation

Traders were segmented into:
- Frequent vs Infrequent traders
- Trade size groups (risk proxy)

👉 Infrequent traders showed higher profitability, suggesting that selective trading is more effective than overtrading.

---

## 🤖 Bonus Analysis (Clustering)

KMeans clustering identified 3 trader groups:

- Low-risk traders (majority)
- Medium-risk traders
- High-risk traders (small group with highest returns)

👉 Larger trade sizes strongly correlate with higher PnL.

---

## 💡 Strategy Recommendations

1. **Reduce risk during Fear**
   - Lower position sizes to manage volatility

2. **Leverage bullish conditions**
   - Increase trading activity during Extreme Greed

3. **Avoid overtrading**
   - Focus on selective, high-quality trades

---

## 🚀 Conclusion

Market sentiment plays a significant role in shaping trader performance and behavior.

Aligning trading strategies with sentiment and managing risk effectively can improve overall profitability.

---

## ▶️ How to Run

1. Open the notebook (`.ipynb`)
2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
