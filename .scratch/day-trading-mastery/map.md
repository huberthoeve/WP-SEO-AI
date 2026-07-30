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

- [Map Garret's System Rules by Timeframe](issues/01-map-garrets-system-rules.md) — GxT system uses 3-timeframe hierarchy (narrative, confirmation, precision timing); entries via C2 closure, Fair Value Gaps, liquidity grabs; exits at precision swing points; risk-based position sizing
- [Define Position Sizing and Risk Per Trade](issues/02-define-position-sizing-and-risk-per-trade.md) — 1% risk per trade ($100), 2-loss daily stop, 10-loss circuit breaker, automatic position sizing via FXReplay

## Not yet specified

- Which specific currency pairs or instruments to focus on initially (GxT works across forex/futures; narrows to a few pairs for consistency?)
- Build the decision tree checklist for multi-timeframe entry/exit (needed before backtesting)
- Success criteria for backtest: what does a "passing" equity curve look like? (win rate %, Sharpe ratio, drawdown tolerance?)
- How many months of historical data to backtest? (current plan: 1 month minimum, but extend if results are marginal)
- Paper trading duration before going live (estimate: 2-4 weeks minimum to validate system under real market conditions?)
- How to recognize if system has degraded or stopped working in live trading vs. normal variance
- Seasonal or quarterly bias confirmation (Garret emphasizes quarterly alignment—should this constrain when you trade?)

## Out of scope

(none yet)
