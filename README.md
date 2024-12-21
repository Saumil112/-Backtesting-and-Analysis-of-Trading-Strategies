# -Backtesting-and-Analysis-of-Trading-Strategies
This project implements and evaluates three trading strategies (SMA, Big Moves on Mondays, and Moving Average Crossover) using Python. It backtests the strategies, calculates performanc
README: Backtesting Strategies for AAPL Stock

This project involves backtesting three distinct trading strategies on Apple Inc. (AAPL) stock data for the last 10 years (2014-12-20 to 2024-12-20). The analysis uses Python and its financial libraries to fetch historical data, apply strategies, and calculate performance metrics.

Strategies Overview

1. Simple Moving Average (SMA) Strategy

Definition:
The SMA strategy uses the rolling average of the closing prices over a specified window (e.g., 50 days) to determine buying and selling signals. If the closing price is above the SMA, a buy signal is generated. Otherwise, a sell signal is generated.

Calculation:

Calculate the 50-day SMA:

SMA = Closing Price Rolling Mean (window=50)

Generate signals:

Buy (1) if Closing Price > SMA

Sell (-1) otherwise

Calculate returns:

Returns = Daily Price Change * Signal from Previous Day

2. Big Moves on Mondays Strategy

Definition:
This strategy identifies significant weekly movements (greater than a defined threshold, e.g., 5%) and trades in the direction of the movement.

Calculation:

Compute weekly returns over the last 5 trading days:

Week_Return = Closing Price Change over 5 days

Generate signals:

Buy (1) if Week_Return > Threshold

Hold (0) otherwise

Calculate returns:

Returns = Daily Price Change * Signal from Previous Day

3. Moving Average Crossover Strategy

Definition:
The Moving Average Crossover strategy uses two SMAs (short-term and long-term). A buy signal is generated when the short-term SMA crosses above the long-term SMA, and a sell signal is generated when it crosses below.

Calculation:

Compute SMAs:

Short-term SMA (50-day)

Long-term SMA (200-day)

Generate signals:

Buy (1) if SMA50 > SMA200

Sell (-1) otherwise

Calculate returns:

Returns = Daily Price Change * Signal from Previous Day

Backtesting and Metrics

The strategies are backtested to compute the following performance metrics:

CAGR (Compound Annual Growth Rate): Measures the annualized return over the testing period.

Sharpe Ratio: Evaluates risk-adjusted returns.

Max Drawdown: Largest percentage drop from a peak in the equity curve.

Win Rate: Percentage of trades with positive returns.

Visualization

1. Cumulative Returns (Equity Curve)

Displays the growth of a $1 investment using each strategy over time.

Helps compare overall performance visually.

2. Drawdown Plot

Visualizes the drawdowns of each strategy over time, indicating periods of underperformance.

3. Yearly Returns Heatmap

Compares annual returns for each strategy using a heatmap for easy interpretation.

Displays performance consistency across years.

4. Performance Metrics Comparison

A bar plot comparing key performance metrics (CAGR, Sharpe Ratio, Max Drawdown, Win Rate) for all strategies.

How to Run the Code

Ensure you have Python installed along with the required libraries:

yfinance

pandas

numpy

matplotlib

seaborn

Save the script and execute it.

The code will:

Fetch historical stock data.

Apply each strategy.

Calculate performance metrics.

Visualize results.

Insights

SMA Strategy: Best for trending markets where prices exhibit strong momentum.

Big Moves Monday Strategy: Captures weekly volatility but may underperform in stable conditions.

MACrossover Strategy: Effective for identifying longer-term trends, but may lag in sideways markets.

By comparing the results, you can identify the strategy that best suits your investment goals and market conditions.
