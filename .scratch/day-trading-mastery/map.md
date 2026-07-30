# Day Trading Mastery

## Destination

Build and validate Garret's day trading system across multiple timeframes, backtest it to profitability over a full month of historical data, paper trade it successfully, then trade live on a $10k account (no leverage) to consistently achieve 5% monthly returns ($500/month).

## Notes

- **System framework**: Garret's system (not ttrades or blended)
- **Backtesting tool**: FXReplay
- **Timeline**: Months, no rush—time is available to do this right
- **Account**: $10k, no leverage
- **Success bar**: Profitable backtest over one full month of historical data before paper trading
- **Validation path**: Backtest → Paper trade → Live trade
- **Current blocker**: System concepts are understood individually but don't align together, especially across multiple timeframes

## Decisions so far

(none yet)

## Not yet specified

- Which specific currency pairs or instruments to focus on initially
- Time of day / market conditions constraints (US session only? specific volatility conditions?)
- Drawdown management—how much downside before stopping trading in a day/week
- Win criteria post-backtest: what does a "good" equity curve look like? (consistency, win rate, Sharpe ratio?)
- Paper trading duration—how many weeks/months of live market before going live?
- How to recognize if the system has stopped working in live conditions vs. variance
- Position sizing formula—how much per trade relative to account size?
- Risk per trade—fixed $ amount, % of account, or variable by opportunity?

## Out of scope

(none yet)
