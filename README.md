# Financial Market Risk Analysis and Portfolio Performance

## Project Overview

This project analyses historical stock-market data to evaluate investment returns, volatility, downside risk, and portfolio performance. Using Python, it compares Apple (AAPL), Alphabet (GOOGL), and Microsoft (MSFT), constructs an equally weighted portfolio, and benchmarks its performance against the S&P 500 index.

The project applies financial risk metrics and portfolio analysis techniques to understand the relationship between historical returns and investment risk.

## Objectives

- Analyse historical stock prices and daily returns.
- Calculate annualised returns and volatility.
- Examine correlations between individual stocks.
- Measure downside risk using historical Value at Risk (VaR) and maximum drawdown.
- Evaluate portfolio performance using the Sharpe ratio.
- Compare portfolio risk and returns against the S&P 500.
- Estimate market sensitivity using beta and CAPM alpha.

## Tools and Technologies

- **Language:** Python
- **Environment:** Google Colab / Jupyter Notebook
- **Libraries:** pandas, NumPy, Matplotlib, yfinance
- **Concepts:** Financial time-series analysis, portfolio diversification, risk measurement, benchmark analysis, CAPM

## Dataset

Historical adjusted stock prices were retrieved using Yahoo Finance data through `yfinance`.

- **Stocks:** AAPL, GOOGL, MSFT
- **Benchmark:** S&P 500 (`^GSPC`)
- **Date range:** January 2021 to December 2025
- **Observations:** Approximately 1,255 price observations and 1,254 daily return observations.

## Methodology

1. Download and inspect historical adjusted prices.
2. Calculate daily percentage returns.
3. Estimate annualised mean returns and volatility using 252 trading days per year.
4. Calculate the correlation matrix to examine relationships between stocks.
5. Estimate historical one-day 95% VaR and maximum drawdown.
6. Construct an equally weighted portfolio with daily rebalancing.
7. Calculate Sharpe ratios using an assumed annual risk-free rate of 4%.
8. Compare portfolio returns, volatility, and VaR with the S&P 500.
9. Estimate portfolio beta and CAPM alpha relative to the benchmark.

## Key Findings

The analysis produced the following historical results:

| Metric | Equal-Weight Portfolio | S&P 500 |
|---|---:|---:|
| Annualised mean return | 23.463% | 13.799% |
| Annualised volatility | 24.386% | 16.958% |
| Historical one-day 95% VaR | 2.512% | 1.646% |

Additional findings:

- GOOGL recorded the highest annualised mean return and volatility among the three stocks in the sample.
- The portfolio's annualised volatility was lower than that of each individual stock.
- The portfolio's Sharpe ratio was approximately 0.798, compared with 0.863 for GOOGL.
- Estimated portfolio beta was 1.222.
- Estimated annualised CAPM alpha was 7.48% under the assumptions used.

These results indicate that the portfolio achieved a higher historical mean return than the S&P 500 while also exhibiting higher volatility and historical downside risk.

## Limitations

- Historical performance does not guarantee future returns.
- The portfolio contains only three stocks and is not broadly diversified across sectors.
- VaR does not measure the severity of losses beyond its estimated threshold.
- Results depend on the selected historical period and the assumptions used for annualisation.
- The risk-free rate of 4% is an illustrative assumption.
- CAPM alpha is a historical model estimate, not proof of persistent outperformance.
- Transaction costs, taxes, and real-world execution constraints are not included.

## How to Run

1. Clone or download this repository.
2. Install the dependencies listed in `requirements.txt`.
3. Open `Financial_Market_Risk_Analysis.ipynb` in Google Colab or Jupyter Notebook.
4. Run the notebook cells in order.

The notebook retrieves historical data using `yfinance`, so an internet connection is required for data downloads.

## Future Scope

- Compare performance across additional sectors and asset classes.
- Evaluate alternative portfolio-weighting strategies.
- Add rolling volatility, rolling beta, and conditional risk measures.
- Explore out-of-sample evaluation and portfolio rebalancing frequencies.
- Incorporate transaction costs and alternative risk-free-rate assumptions.

## Disclaimer

This project is for educational and analytical purposes only. It does not constitute financial or investment advice.

