# Portfolio Analysis: Investment Management Firms vs. Algorithms vs. S&P 500
![chart](https://www.stockideas.org/wp-content/uploads/2013/12/stock-chart-technical-analysis.jpg)

Performing quantitative analysis (using Python/Pandas) on different Investment Management firm portfolios, algorithmic returns and returns based on the S&P 500 closing price to determine which is performing the best across areas such as volatility, risk and Sharpe ratios.  Data based on a 4-year timeframe from 2015-2019.  Investment Management Firm portfolios analyzed include Soros Fund Management LLC, Paulson & Co. Inc., Tiger Global Management LLC and Berkshire Hathaway LLC.  These metrics are then visualized using matplotlib.

### While the Investment Management Firm dataset and the Algorithmic dataset already had "daily returns" data before being loading into the notebook, the S&P 500 dataset had only "returns" as the data.  Therefore, it was necessary to convert this to "daily returns" by using the ".pct_change()" function:

    # Calculate S&P 500 daily returns using .pct_change() function:
    sp500_daily_returns = sp500_history_df.pct_change()

    # Rename column:
    sp500_daily_returns.columns = ["S&P 500 Daily Returns"]

    # Drop nulls:
    sp500_daily_returns.dropna(inplace=True)


```
# Calculate S&P 500 daily returns using .pct_change() function:
sp500_daily_returns = sp500_history_df.pct_change()

# Rename column:
sp500_daily_returns.columns = ["S&P 500 Daily Returns"]

# Drop nulls:
sp500_daily_returns.dropna(inplace=True)
```




## Conclusions:

### Here:
![Plot1.1](/Pics_of_Plots/Plot1.1.png?raw=true)