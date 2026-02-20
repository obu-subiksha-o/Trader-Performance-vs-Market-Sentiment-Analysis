# Trader-Performance-vs-Market-Sentiment-Analysis

## Project Overview

This project analyzes the relationship between **trader performance** and **market sentiment regimes** (Fear & Greed Index).

The objective is to:

* Merge trader-level execution data with daily sentiment data
* Analyze profitability across sentiment classifications
* Test statistical significance (ANOVA)
* Generate actionable trading insights

---

## Dataset Description

### Trader Dataset

Contains trade-level information:

* Account
* Coin
* Execution Price
* Size Tokens
* Size USD
* Closed PnL
* Timestamp IST
* Direction
* Fee

### Sentiment Dataset

Contains daily market sentiment:

* timestamp
* value
* classification (Fear, Greed, Extreme Fear, Extreme Greed, Neutral)
* date

---

## Setup Instructions

### Clone or Download Project

```bash
git clone <your-repo-link>
cd trader-sentiment-analysis
```

Or download the notebook and datasets manually.

---

### Install Required Libraries

Make sure Python 3.9+ is installed.

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scipy
```

---

## How to Run

### Option 1: Jupyter Notebook (Recommended)

```bash
jupyter notebook
```

Open:

```
Trader Performance vs Market Sentiment.ipynb
```

Run all cells in order.

---

### Option 2: Google Colab

1. Upload the notebook
2. Upload both datasets
3. Run cells sequentially

---

## Data Processing Steps

1. Clean column names
2. Convert timestamps to datetime
3. Extract daily date
4. Merge trader and sentiment datasets
5. Handle missing values
6. Create win/loss indicator

---

## Analysis Performed

### Profitability by Sentiment

* Mean PnL
* Median PnL
* Standard deviation
* Trade count

### Win Rate by Sentiment

* Percentage of profitable trades per regime

### Statistical Testing

* One-way ANOVA
* Tested if mean PnL differs across sentiment regimes

Result:
Statistically significant difference found (p < 0.05)

### Performance Segmentation

* Traders split into Top Half vs Bottom Half
* Compared regime performance across segments

---

## Key Findings

* Extreme Greed shows highest average profitability
* Fear regimes increase volatility and dispersion
* Top-half traders benefit more from Greed conditions
* Sentiment significantly impacts trade outcomes

---

## Actionable Strategy Ideas

### Sentiment-Based Position Sizing

* Increase exposure during Greed regimes
* Reduce exposure during Fear regimes
* Maintain neutral sizing during Neutral days

### Regime-Aware Trade Filtering

* Restrict aggressive trades during Extreme Fear
* Allow higher trade frequency during Greed
* Apply tighter risk controls in Fear regimes

---

## Folder Structure

```
├── Trader Performance vs Market Sentiment.ipynb
├── trader_data.csv
├── fear_greed_index.csv
├── README.md
```

---

## Tools Used

* Python
* Pandas
* NumPy
* SciPy
* Matplotlib
* Seaborn

---

## Conclusion

This project demonstrates that trader profitability is significantly influenced by market sentiment regimes.

Incorporating sentiment-aware position sizing and execution rules can potentially improve risk-adjusted returns.

---
