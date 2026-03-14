# Trader Behavior vs Market Sentiment Analysis

## Objective

The objective of this project is to analyze how **Bitcoin market sentiment (Fear vs Greed)** influences trader behavior and performance. By combining market sentiment data with historical trading data from Hyperliquid, the project aims to identify patterns in trading activity, profitability, leverage usage, and trading strategies during different market conditions.

The goal is to generate meaningful insights that can help traders understand how sentiment impacts trading decisions and develop better risk management strategies.
## Dataset Overview

This project uses two datasets:

### 1. Bitcoin Market Sentiment Dataset

This dataset provides the daily **market sentiment classification**.

Columns:

* Date
* Classification (Fear / Greed)

### 2. Hyperliquid Trader Dataset

This dataset contains detailed historical trading records from traders.

Example columns:

* account
* symbol
* execution_price
* size
* side (Long / Short)
* time
* start_position
* closedPnL
* leverage

These datasets were combined to analyze trader behavior under different market sentiment conditions.

---

## Data Cleaning

Several preprocessing steps were performed to prepare the datasets:

* Removed duplicate rows
* Checked and handled missing values
* Converted timestamp columns into proper datetime format
* Standardized column names for easier analysis
* Verified numeric data types for trading metrics

These steps ensured the datasets were accurate and suitable for analysis.

---

## Data Alignment

The sentiment dataset provides **daily sentiment values**, while the trader dataset contains **timestamp-based trading records**.

To align the datasets:

1. Converted trade timestamps into date format
2. Aggregated trader data on a daily level
3. Merged both datasets using the **date column**

This allowed trading activity to be analyzed relative to the sentiment of that day.

---

## Feature Engineering

Several analytical metrics were created to study trader behavior:

* **Daily PnL per trader**
* **Number of trades per day**
* **Average trade size**
* **Leverage distribution**
* **Long vs Short trade ratio**

These features helped evaluate performance and trading behavior across different market sentiments.

---

## Methodology

The analysis was performed using the following steps:

1. Data loading and exploration
2. Data cleaning and preprocessing
3. Feature engineering and metric creation
4. Dataset merging based on date
5. Sentiment-based behavioral analysis
6. Trader segmentation
7. Visualization and insight generation

Python libraries such as **Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn** were used for data analysis and visualization.

---

## Visualizations

Several charts were created to better understand the relationship between sentiment and trader behavior:

* Average **PnL during Fear vs Greed days**
* **Trading frequency by market sentiment**
* **Leverage distribution among traders**
* **Long vs Short trade ratios**

These visualizations help identify behavioral patterns and performance differences under different sentiment conditions.

---

## Trader Segmentation

To better understand trader behavior, traders were divided into different segments:

### 1. High Leverage Traders

Traders who frequently use higher leverage levels in their trades.

### 2. Low Leverage Traders

Traders who maintain lower leverage and lower risk exposure.

### 3. Frequent Traders

Traders who execute a large number of trades per day.

### 4. Infrequent Traders

Traders who trade occasionally with lower activity levels.

Segmenting traders helped analyze how different types of traders react to market sentiment.

---

## Key Insights

1. **Trading activity increases during Greed sentiment**, indicating higher market confidence among traders.

2. **Trade sizes tend to be larger during Greed periods**, suggesting increased risk-taking behavior.

3. **Frequent traders generally show more consistent performance** compared to infrequent traders.

These insights demonstrate that market sentiment significantly influences trading behavior and performance.

---

## Strategy Recommendations

Based on the findings, the following strategies are suggested:

### 1. Reduce Risk During Fear Markets

During Fear periods, traders may reduce leverage and position sizes to minimize exposure to market volatility.

### 2. Increase Activity During Greed Markets

During Greed sentiment, traders may increase trading activity to benefit from stronger market momentum.

These strategies may help traders improve risk management and optimize trading performance.

---

## How to Run
### 1. Install Required Libraries
```bash
pip install -r requirements.txt
```
### 2. Run the Notebook

Open the Jupyter Notebook file and execute all cells to reproduce the analysis.

### Libraries Used

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
