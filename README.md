# Bitcoin Market Sentiment vs Trader Performance Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment and trader performance using the Bitcoin Fear & Greed Index and Hyperliquid historical trading data.

The objective is to understand how different market sentiment conditions influence:

- Trading activity
- Profitability
- Win rate
- Position sizing behavior
- Buy vs Sell strategy effectiveness
- Risk-adjusted performance

By combining market sentiment data with real trading records, the analysis aims to uncover actionable insights that can support smarter trading decisions.

---

## Datasets Used

### 1. Bitcoin Fear & Greed Index

The Bitcoin Fear & Greed Index measures overall market sentiment and classifies market conditions into:

- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

Columns Used:

- Date
- Classification
- Value

### 2. Hyperliquid Historical Trader Data

Historical trading records containing information such as:

- Account
- Coin
- Execution Price
- Size Tokens
- Size USD
- Side (BUY/SELL)
- Closed PnL
- Trade ID
- Timestamp

---

## Project Workflow

### Data Preparation

- Loaded both datasets
- Fixed timestamp parsing issues
- Converted timestamps into datetime format
- Merged trading data with sentiment data using trade date
- Converted financial columns into numeric format
- Removed unmatched records

### Feature Engineering

Created:

- Trade Date
- Winning Trade Flag
- Sentiment-based trade groups

---

## Analysis Performed

### 1. Trading Activity Analysis

Analyzed trading frequency across different sentiment categories to understand trader participation during varying market conditions.

### 2. Profitability Analysis

Evaluated:

- Total PnL
- Average PnL
- Median PnL

for each sentiment category.

### 3. Win Rate Analysis

Measured the percentage of profitable trades across sentiment regimes.

### 4. Position Size Analysis

Compared average trade sizes across different market sentiments.

### 5. Buy vs Sell Strategy Analysis

Examined the profitability of BUY and SELL trades under each sentiment condition.

### 6. Risk-Adjusted Performance Analysis

Calculated a simple risk-adjusted performance score:

Risk Adjusted Score = Average PnL / Standard Deviation of PnL

### 7. Top Trader Analysis

Identified the most profitable traders and compared trading frequency with profitability.

---

## Key Findings

### 1. Trading Activity Was Highest During Fear

Fear periods recorded the highest number of trades, indicating increased market participation during uncertain conditions.

### 2. Extreme Greed Produced the Highest Profitability

Extreme Greed generated the highest average profit per trade among all sentiment categories.

### 3. Extreme Greed Achieved the Highest Win Rate

Trades executed during Extreme Greed conditions had the highest probability of being profitable.

### 4. Trade Size Did Not Drive Performance

Despite generating the highest profitability, Extreme Greed had the smallest average trade size, suggesting improved trade quality rather than increased risk-taking.

### 5. Sentiment Influenced Strategy Effectiveness

- BUY trades performed best during Fear periods.
- SELL trades performed best during Greed and Extreme Greed periods.

### 6. Extreme Greed Delivered the Best Risk-Adjusted Performance

Extreme Greed achieved the strongest balance between profitability and volatility.

---

## Strategic Recommendations

Based on the analysis:

1. Consider increasing exposure to BUY opportunities during Fear periods.

2. Consider profit-taking or SELL-focused strategies during Greed and Extreme Greed conditions.

3. Incorporate sentiment indicators into trading decision frameworks.

4. Focus on trade quality rather than simply increasing position size.

5. Monitor sentiment transitions as potential signals for strategy adjustments.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

## Repository Structure

```text
bitcoin-sentiment-trader-performance-analysis/
│
├── Bitcoin_Sentiment_Analysis.ipynb
├── README.md
├── requirements.txt
└── report.pdf
```

---

## Conclusion

The analysis demonstrates that market sentiment has a measurable impact on trader behavior and trading performance.

Extreme Greed emerged as the most favorable sentiment regime in terms of profitability, win rate, and risk-adjusted returns. Additionally, BUY strategies performed better during Fear periods, while SELL strategies became increasingly effective as market optimism increased.

These findings highlight the potential value of incorporating sentiment signals into trading and risk-management systems.
