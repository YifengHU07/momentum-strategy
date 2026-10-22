# Cross-sectional Momentum Strategy

A monthly long-short momentum backtest on 10 US large caps, compared with the S&P 500 (SPY). Daily prices from Yahoo Finance, 2020-2024.

## Strategy
- Universe: AAPL, MSFT, GOOGL, AMZN, META, TSLA, NVDA, JPM, JNJ, XOM
- Signal: sum of the past 12 monthly returns
- Each month-end: long the top 3 and short the bottom 3 stocks, equal weights, held for one month
- The signal from the previous month-end is used, so there is no look-ahead

## Results (2021-2024)
| Metric | Value |
|---|---|
| Annualised return | 7.17% |
| Annualised volatility | 30.53% |
| Sharpe ratio (no risk-free rate) | 0.23 |
| Maximum drawdown | -42.44% |

The strategy underperformed SPY over the period.

## Limitations
- The stock universe was hand-picked after the fact and includes 2020-2024 winners (NVDA, TSLA, META), so it is subject to survivorship and selection bias.
- No transaction costs, borrow fees or slippage.
- Small cross-section (10 stocks) and a single sample period with no out-of-sample test, so the results are noisy.
- The signal uses the full 12 months; the standard 12-1 momentum skips the most recent month.
