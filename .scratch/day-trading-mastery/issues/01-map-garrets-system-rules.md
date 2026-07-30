# Map Garret's System Rules by Timeframe

Type: grilling
Status: resolved
Blocked by: (none)

## Question

Garret's system has multiple concepts (entries, exits, risk management, multi-timeframe alignment) that you understand individually but haven't yet mapped out explicitly. This ticket is about externalizing the system—pulling it out of your notes and Garret's materials into a clear document that shows:

1. What are the core **entry rules** Garret teaches? (How do you know when to enter a trade?)
2. What are the core **exit rules**? (How do you know when to exit?)
3. How do these rules **differ across timeframes**? (What changes on a 5m vs 15m vs 1h chart?)
4. What are the **prerequisites** before entering? (Market conditions, trend confirmation, etc.?)
5. What's the **position sizing logic** built into the system?

By the end, you'll have a decision tree document that you can reference without confusion during backtesting.

## Answer

**GxT Garret Trading System Framework**

### **Entry Rules and Signals**

1. **C2 Closure** (most reliable entry signal)
   - Candle fails to close beyond the previous candle's low/high
   - Indicates rejection and potential reversal
   - Applies across all timeframes

2. **Fair Value Gaps (FVG)**
   - Unretraced areas between candle bodies
   - Smart money targets and defends these levels
   - Serve as both entry confirmation and target zones

3. **CISD (Closing Inside Swing Displacement)**
   - Confirms that smart money is defending a level
   - Shows institutional interest in the area

4. **Liquidity Grabs**
   - Fakeout breakouts followed by reversals
   - Entry occurs on the reversal back into the original zone
   - Requires confirmation on lower timeframe

5. **Session Timing Entries**
   - London Open (1am UTC)
   - NY Open (5am UTC)
   - NY Continuation (9am UTC)
   - Strongest entries align with major session transitions

6. **Wick Analysis**
   - Small wicks support expansion trades
   - Large wicks indicate rejection/caution
   - Used to filter weak setups

### **Exit Rules and Targets**

1. **Precision Swing Points (PSP)**
   - Primary profit-taking methodology
   - Use protected swings on multiple timeframes
   - Market-generated targets based on structure

2. **Fair Value Gaps**
   - Secondary target zones
   - Often hit before PSP targets

3. **Key Structural Levels**
   - Higher timeframe highs/lows
   - Protected swings from previous structure

4. **Stop Loss Placement**
   - Placed just beyond candle structures that would invalidate thesis
   - Determines position size via risk management rules

### **Multi-Timeframe Alignment (CRITICAL)**

The system uses a strict 3-timeframe hierarchy:

1. **Higher Timeframe** (4-hour or daily)
   - Sets the **NARRATIVE** (direction bias)
   - Defines whether to look for long or short entries only

2. **Structural Timeframe** (1-hour)
   - Provides **CONFIRMATION** of narrative
   - Validates that structure supports the directional bias

3. **Entry Timeframe** (15-min or 5-min)
   - Provides **PRECISION TIMING**
   - Where actual entry signals (C2, FVG, Liquidity Grab) are hunted

**Key Rule**: Require 3+ timeframes aligned before entering. Only take entries in the narrative direction.

### **Position Sizing Philosophy**

- Risk-based entries: Stop placement determines position size
- Capital preservation is paramount
- Asset synchronization: Use Swing Market Turns (SMT) to align correlated assets
- Avoid trades when correlated assets decouple (correlation breaks)

### **Key Concepts and Principles**

1. **Narrative vs. Drivers**
   - Narrative = direction (higher timeframe)
   - Drivers = confirmation (structural timeframe)

2. **Liquidity Targeting**
   - Smart money grabs liquidity before moving
   - Recognize and fade these moves

3. **Candle Profiling**
   - Analyze wick size, range, and color
   - Filters weak setups early

4. **Market Structure Shifts**
   - Identify when swing patterns change
   - Signals major moves coming

5. **Quarterly Alignment**
   - Use seasonal/longer-term timeframes as ultimate bias confirmation

6. **Decoupling Recognition**
   - When correlated assets diverge, thesis is weakened
   - Reduce risk or exit

### **Workflow Summary**

1. Establish higher timeframe narrative (4h or daily) - bullish or bearish?
2. Confirm on structural timeframe (1h) - does structure support narrative?
3. Hunt for entry on lower timeframe (15m/5m) - only in narrative direction
4. Execute using C2 closure, FVG approach, or liquidity grab
5. Exit at precision swing points or key structural levels

**Status**: RESOLVED
