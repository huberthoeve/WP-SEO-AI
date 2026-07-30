# Define Position Sizing and Risk Per Trade

Type: grilling
Status: resolved
Blocked by: (none)

## Question

Before you can backtest meaningfully, you need to know: **How much of your account do you risk on each trade?**

This needs to answer:

1. **Risk per trade**: Fixed amount (e.g., $100 per trade) or percentage of account (e.g., 1% of $10k = $100)?
2. **Position sizing**: If risking $100, how many units/lots do you buy given your stop loss distance?
3. **Max loss per day**: Do you have a daily loss limit before you stop trading?
4. **Max consecutive losses**: Do you quit after 3 losing trades in a row, or keep going?
5. **Account scaling**: As you grow the account, does position size scale automatically?

These parameters directly affect whether your backtest results are realistic and whether you'll stick to the system under pressure.

## Answer

**Position Sizing and Risk Framework (Locked)**

1. **Risk per trade**: 1% of account = $100 per trade on $10k account
   - Percentage-based scales automatically as account grows
   - Applied via FXReplay automatic position sizing feature

2. **Position sizing**: Calculated automatically by FXReplay based on 1% risk rule and stop loss distance

3. **Daily loss limit**: 2 consecutive losing trades = stop trading for the day
   - Prevents revenge trading and protects against emotional decisions
   - Clear off-switch for intraday sessions

4. **System circuit breaker**: 10 consecutive losses across any timeframe = pause trading
   - Signal to stop, review the system, and debug what's breaking
   - Not a permanent quit, but a mandatory reassessment checkpoint

5. **Account scaling**: Automatic via percentage-based approach
   - As account grows (e.g., $10k → $15k), 1% risk grows proportionally
   - Position size scales naturally without manual adjustment

**Status**: RESOLVED
