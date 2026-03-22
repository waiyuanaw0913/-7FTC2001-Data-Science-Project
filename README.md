# Multi-Timeframe FX Prediction (USD/JPY)

##  Project Overview

This project explores the use of machine learning and deep learning models for short-term foreign exchange (FX) trend prediction and trading signal generation.

The study focuses on USD/JPY using multi-horizon technical indicators (1-day and 4-day) derived from mid-price data. Models implemented include Logistic Regression, Random Forest, and a Transformer-based architecture.

The objective is to evaluate whether combining multiple time horizons improves predictive accuracy and trading performance.

---

##  Dataset

* Source: Dukascopy historical FX data
* Period: 2016 – 2025
* Frequency: Daily
* Features:

  * Bid / Ask prices
  * Mid-price (computed)
  * Technical indicators: EMA, RSI, MACD, ATR

Processed data is stored in a SQLite database (`forex_mtf.db`) for reproducibility.

---

##  Methodology

1. Data preprocessing and cleaning
2. Feature engineering (technical indicators + multi-horizon features)
3. Model training:

   * Logistic Regression (baseline)
   * Random Forest (nonlinear model)
   * Transformer (sequence model)
4. Evaluation:

   * Classification metrics (Accuracy, Precision, Recall, F1-score)
   * Trading performance (Cumulative Return, Sharpe Ratio, Max Drawdown)
5. Backtesting using historical data

---

##  Results Summary

* Random Forest achieved the best trading performance
* Logistic Regression performed competitively as a baseline
* Transformer did not significantly outperform simpler models
* Multi-horizon features showed mixed impact

---

##  Limitations

* No transaction cost modelling
* Single currency pair (USD/JPY)
* Limited hyperparameter tuning for Transformer

---

##  Future Work

* Extend to multiple currency pairs
* Include macroeconomic features
* Improve Transformer architecture
* Explore reinforcement learning for trading

---

##  How to Run

Note: The original implementation uses Google Colab with Google Drive paths. 
Users need to modify the dataset paths to match their local or cloud environment before running the code.

---

##  Repository Structure

* `USDJPY_Data/Data/` – raw and processed data
* `notebooks/` – analysis and experiments

---

##  Author

Aw Wai Yuan

---

##  License

This project is for academic purposes only.
