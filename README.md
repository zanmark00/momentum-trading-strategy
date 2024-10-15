# momentum-trading-strategy

This repository contains the backtest and analysis of a momentum-based trading strategy applied to the S&P 500 ETF (SPY) using technical indicators such as Moving Averages, RSI (Relative Strength Index), and Bollinger Bands. The strategy was tested from 2015 to 2023 and compared to a buy-and-hold approach to evaluate performance.

## Contents

- **`spy_backtest_momentum_strategy.ipynb`**: A Jupyter notebook containing the backtest code for the momentum-based trading strategy. It demonstrates how buy and sell signals are generated using technical indicators and how the strategy performed over the backtest period.
- **`strategy_s&p500.pdf`**: A report that details the performance of the strategy, including risk metrics such as the Sharpe Ratio and Maximum Drawdown, as well as a comparison to the buy-and-hold strategy.

## Strategy Overview

The momentum trading strategy utilizes the following technical indicators to identify buy and sell signals:

- **Moving Averages**: The strategy uses a 50-day and 200-day simple moving average (SMA). A buy signal is triggered when the 50-day SMA crosses above the 200-day SMA, and a sell signal is triggered when it crosses below.
- **RSI (Relative Strength Index)**: A 14-day RSI is used to identify overbought and oversold conditions. An RSI below 30 is considered oversold (buy signal), while an RSI above 70 is considered overbought (sell signal).
- **Bollinger Bands**: The Bollinger Bands are calculated using a 20-day moving average and 2 standard deviations. A buy signal is generated when the price touches or drops below the lower band, and a sell signal occurs when the price touches or exceeds the upper band.

## Results

The strategy was backtested on historical data from January 2015 to January 2023. Below are the key performance metrics:

- **Sharpe Ratio**: 0.62 (compared to 0.51 for the buy-and-hold strategy)
- **Maximum Drawdown**: -34.10% (same as buy-and-hold strategy)
  
While the strategy outperforms the buy-and-hold approach in trending markets, it struggles in sideways or choppy markets, where frequent buy/sell signals lead to overtrading.

## Files

- `spy_backtest_momentum_strategy.ipynb`: The Jupyter notebook implementing the momentum strategy and backtesting it on SPY.
- `strategy_s&p500.pdf`: A comprehensive report detailing the strategy's performance, including risk considerations and areas for improvement.

## Installation and Usage

1. **Clone the repository**:

   ```bash
   git clone https://github.com/zanmark00/momentum-trading-strategy.git
   cd momentum-trading-strategy
