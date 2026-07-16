# Energy Cross-Commodity Quantitative Research

> Status: Work in progress

This project aims to build a quantitative research framework for energy and commodity markets.

The objective is to study statistical relationships across energy-related assets, build simple and interpretable trading signals, and evaluate them through transaction-cost-aware backtesting.

## Project Overview

Energy markets include assets such as crude oil, natural gas, refined products, power and carbon. These markets are often linked through economic relationships, supply and demand dynamics, storage constraints and substitution effects.

This project focuses on cross-commodity quantitative research. The goal is to analyze price relationships between energy-related assets and test whether simple signals such as momentum, mean reversion and spread-based indicators can provide useful information.

The purpose is not to build a production-ready trading strategy, but to develop a disciplined research process close to what is expected in quantitative trading and commodity research.

## Objectives

The project focuses on:

- collecting and cleaning historical commodity price data;
- analyzing price dynamics, returns and volatility;
- studying rolling correlations across energy assets;
- building spreads and ratios between related commodities;
- constructing momentum and mean-reversion signals;
- testing simple long/short strategies;
- including transaction costs in the backtest;
- measuring risk-adjusted performance;
- analyzing robustness and limitations.

## Motivation

Commodity and energy markets are important areas for quantitative research, options trading and systematic strategies.

A quantitative approach can help study:

- trend-following behavior;
- mean-reverting spreads;
- volatility regimes;
- cross-market relationships;
- statistical biases;
- risk-adjusted performance of trading signals.

This project is designed to connect market intuition, statistical analysis and practical backtesting.

## Planned Repository Structure

```text
notebooks/
  01_energy_market_data_exploration.ipynb
  02_spread_and_signal_research.ipynb
  03_backtesting_and_risk_analysis.ipynb

src/
  data.py
  signals.py
  backtest.py
  risk_metrics.py

references/
  README.md

README.md
```

## Research Questions

The project will be guided by the following questions:

- Do energy-related assets exhibit stable or unstable correlations over time?
- Can spreads between related commodities show mean-reverting behavior?
- Are simple momentum signals useful across energy markets?
- How sensitive are the results to transaction costs?
- Are the signals robust across different market regimes?
- What are the main limitations of a simple backtest on commodity price series?

## Roadmap

### Step 1 — Data Collection and Cleaning

- Collect historical price data for energy-related assets.
- Start with assets such as crude oil, Brent, natural gas, gasoline or heating oil depending on data availability.
- Align all time series on the same calendar.
- Handle missing values.
- Compute log returns.

### Step 2 — Exploratory Data Analysis

- Plot price series and returns.
- Compute descriptive statistics.
- Analyze rolling volatility.
- Analyze rolling correlations.
- Identify major market regimes and stress periods.

### Step 3 — Spread and Ratio Analysis

- Build spreads between related assets.
- Compute ratios between commodity prices.
- Standardize spreads using rolling z-scores.
- Study whether some spreads display mean-reverting behavior.
- Analyze the stability of these relationships over time.

### Step 4 — Signal Construction

- Build simple momentum signals.
- Build mean-reversion signals based on spread z-scores.
- Add volatility filters.
- Compare signal behavior across assets and regimes.

### Step 5 — Backtesting Framework

- Construct simple long/short strategies.
- Avoid look-ahead bias.
- Include transaction costs.
- Compute daily or weekly PnL.
- Track positions, turnover and exposure.

### Step 6 — Risk and Performance Analysis

- Compute cumulative returns.
- Compute annualized return and volatility.
- Compute Sharpe ratio.
- Compute maximum drawdown.
- Compute hit ratio.
- Analyze performance by market regime.

### Step 7 — Robustness and Limitations

- Discuss the risk of overfitting.
- Study the impact of transaction costs.
- Discuss the difference between spot prices and futures prices.
- Discuss futures roll issues.
- Identify limitations of the simplified framework.
- Propose possible improvements.

## References

- Moskowitz, Ooi and Pedersen, *Time Series Momentum*.
- Gorton, Hayashi and Rouwenhorst, *The Fundamentals of Commodity Futures Returns*.
- Academic literature on pairs trading and statistical arbitrage.
- Research on commodity futures, spread trading and systematic strategies.

## Tech Stack

- Python
- pandas
- NumPy
- scipy
- statsmodels
- matplotlib
- scikit-learn
- Time series analysis
- Backtesting
- Risk metrics

## Current Status

The project is currently in progress.

The first development phase focuses on reviewing commodity market basics, collecting clean historical data and building exploratory analysis tools before implementing trading signals and backtests.

## Disclaimer

This project is for academic and educational purposes only. It does not constitute financial advice or a production-ready trading strategy.
