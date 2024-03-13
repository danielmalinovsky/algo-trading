# algo-trading
Repository for various algotrading test scripts

# Installation

```
git clone https://github.com/danielmalinovsky/automated_marketmaker_calc.git
```
# Projects

## Buy/sell Classifier with Neural Networks (using Yahoo Finance)

This Python script automates a data pipeline to scrape financial data about stocks from Yahoo Finance and utilizes a neural network to predict whether a stock's price will increase or decrease in value.

### Features

* Automated data scraping from Yahoo Finance
* Preprocessing of financial data
* Neural network model for stock price prediction

### Disclaimer

This script is for educational purposes only and should not be used for making financial decisions. The accuracy of the predictions cannot be guaranteed.

### Further Development

* Implement additional features like:
    * Support for different data sources
    * More sophisticated neural network architectures
    * Backtesting and evaluation of prediction performance (in progress)
 
## Backtesting with Python and backtesting.py

This tutorial guides you through creating a basic backtesting script using the `backtesting.py` package. Backtesting allows you to evaluate the performance of trading strategies on historical data without risking real capital.

### Prerequisites

- `backtesting.py` package: Install using `pip install backtesting.py`

### Tutorial Structure

1. **Import Libraries**
	- Import necessary libraries like `backtest` from `backtesting.py` and potentially `pandas` for data manipulation.
1. **Define Your Strategy**
	- Create a class inheriting from `backtesting.Strategy`.
	- Override the `init` method to initialize strategy parameters.
	- Override the `next` method to define your trading logic based on current price data.
2. **Set Up Backtest**
	- Create a `backtest` object from `backtesting.Test`.
	- Provide historical price data (e.g., DataFrame).
	- Specify your strategy class.
	- Set initial capital and commission fees (optional).
3. **Run Backtest**
	- Call the `run` method on the `backtest` object.
4. **Analyze Results**
	- Access the backtest object's attributes (e.g., `pnl`, `trades`, `equity`) for performance analysis.
	- Consider plotting relevant metrics for visualization.

## Backtesting streaks trading strategy with Python and backtesting.py

### Assumptions
1. Prices are moving in trends
2. Trends are having time distribution of their length

### Implementation
1. **Create custom technical indicator "Streaks"**
	- streaks are measuring how many time periods is price moving up or down
2. **Identify distribution of streaks for given asset**
	- check distribution of the streaks within given data and propose trading strategy based on it
3. **Optimize and backtest trading strategies**
	- backtesting.py is utilized together with custom Streaks indicator to find optimal parameters for trading strategy
	- Parameters optimized are: streak to open short position at, streak to open long position at, streak to close position at
4. **Investigate optimalization results**
	- Double check optimalization results for errors. Optionally override to optimal rule
5. **Apply to multiple assets**
	- Script is proposed in a way that allows to scan through any asset listed at yahoo finance
	- Thus it is possible to scan for assets that are most responsive to Streaks trading strategy

### Disclaimer

This script is for educational purposes only and should not be used for making financial decisions. The accuracy of the predictions cannot be guaranteed.

### Contribution

We welcome contributions to this project. Feel free to fork the repository and submit pull requests with your improvements.

### License

MIT License

Copyright (c) 2024 Daniel Malinovsky

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Author(s)

* Daniel Malinovsky
