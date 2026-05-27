# Decision Framework

> **Status:** Seed document. Concrete decision logs fill in as the experiment runs.

## Core question Moot asks before any trade

> "Given the signals I see right now, what's the best risk-adjusted use of capital?"

Not "what's going to go up" — that's prediction, and the framework doesn't try to predict. The framework allocates capital to the positions with the best expected risk-adjusted return *given current information*, knowing the information will be wrong sometimes.

## Decision inputs (in priority order)

1. **Regime detection** — what kind of market are we in? Trending / mean-reverting / high-volatility / low-volatility. The regime determines which signals get amplified vs. dampened.
2. **Multi-signal fusion** — 8 signal categories combine into one calibrated confidence per ticker.
3. **Portfolio context** — current positions, sector exposure, correlation matrix. A signal to buy NVDA is weaker if we're already long the entire AI sector.
4. **Risk budget** — max daily loss, max drawdown, max single-position size. Hard constraints, not preferences.
5. **Liquidity check** — can we actually fill this order without moving the market?

Only when all five say "go" does Moot place a trade.

## What Moot does NOT do

- Pump-and-dump
- React to short-term price action without signal confirmation
- Take "moonshot" gambles on single-name volatility
- Pyramid into losing positions
- Use leverage beyond Alpaca's default 2:1
- Trade penny stocks or anything below $2 liquidity
- Override risk limits "just this once"

## Why this matters

The framework is rule-based by design. AI is good at producing convincing-looking decisions; a rule-based framework restricts AI's autonomy to the things AI is provably better at (pattern recognition, signal weighting, scenario evaluation) and keeps humans in control of the things humans are still better at (risk philosophy, position sizing discipline, knowing when to stop).

The experiment tests whether constrained AI agency, applied to a real public account, produces returns over 3 years.
