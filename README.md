# Momentum Trading Strategy for S&P 500 (SPY)

This repository contains the backtest and analysis of a momentum-based trading strategy applied to the S&P 500 ETF (SPY). The strategy uses technical indicators such as Moving Averages, RSI (Relative Strength Index), and Bollinger Bands to generate buy and sell signals.

## Contents

- **`spy_backtest_momentum_strategy.ipynb`**: A Jupyter notebook that implements the backtest code for the strategy, showcasing how the buy and sell signals are generated and how the strategy performed over the backtest period.
- **`strategy_s&p500.pdf`**: A report that provides detailed performance results of the momentum trading strategy, including key metrics such as the Sharpe Ratio and Maximum Drawdown.
- **`strategy.py`**: A Python script that runs the full backtest of the momentum trading strategy. It downloads historical data using `yfinance`, calculates moving averages, RSI, and Bollinger Bands, and then evaluates the strategy's performance.

## Strategy Overview

The momentum trading strategy relies on the following technical indicators to generate buy and sell signals:

- **Moving Averages**: The strategy uses a 50-day and 200-day simple moving average (SMA). A buy signal occurs when the 50-day SMA crosses above the 200-day SMA, and a sell signal occurs when it crosses below.
- **RSI (Relative Strength Index)**: The 14-day RSI is used to identify overbought and oversold conditions. An RSI below 30 signals oversold conditions (buy), while an RSI above 70 signals overbought conditions (sell).
- **Bollinger Bands**: The 20-day moving average with 2 standard deviations is used to calculate Bollinger Bands. A buy signal is triggered when the price falls below the lower band, and a sell signal is triggered when the price rises above the upper band.

## Results

The strategy was backtested from January 2015 to January 2023. Below are the key performance metrics:

- **Sharpe Ratio**:
  - Strategy: 0.62
  - Buy-and-Hold: 0.51
- **Maximum Drawdown**:
  - Strategy: -34.10%
  - Buy-and-Hold: -34.10%

## Installation and Usage

1. **Clone the repository**:

   ```bash
   git clone https://github.com/zanmark00/momentum-trading-strategy.git
   cd momentum-trading-strategy
