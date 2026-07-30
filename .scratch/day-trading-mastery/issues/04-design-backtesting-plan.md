# Design Backtesting Plan in FXReplay

Type: grilling
Status: unclaimed
Blocked by: 02, 03

## Question

Before you start clicking through FXReplay, you need a plan: **What data will you test on, and how will you know if it worked?**

This ticket covers:

1. **Data selection**: Which currency pairs? How many months of historical data will you test on? (Recommendation: start with 1–3 months to validate profitability)
2. **What to track during backtest**: Equity curve, win rate, largest winning/losing trades, drawdown, consecutive losses
3. **Success criteria**: What does a passing backtest look like? (e.g., positive P&L, win rate > 45%, max drawdown < 10%?)
4. **Failure criteria**: What would make you reject the system and redesign? (e.g., three consecutive losing trades, equity curve underwater for >2 weeks?)
5. **Testing approach**: Will you test in real-time mode (watching price move) or fast-forward through candles?

## Answer

(to be filled in after resolution)
