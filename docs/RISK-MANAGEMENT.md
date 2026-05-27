# Risk Management

> **Status:** Seed document. Specific incident postmortems fill in as the experiment runs.

## Philosophy

Risk management is the boring part. Done right, you don't notice it. Done wrong, the whole experiment dies in one bad week.

Moot's risk discipline is rule-based, not discretionary. The rules below are constants; they don't get bent because "this trade is special."

## Hard limits (non-negotiable)

| Limit | Threshold | What happens if exceeded |
|---|---|---|
| Single position size (% of portfolio) | Capped | Cannot add to position |
| Sector exposure (% of portfolio) | Capped | New sector positions rejected |
| Daily portfolio loss | Capped | Trading halted until next open |
| Max drawdown from peak | Capped | Increasingly conservative sizing |
| Open positions (count) | Capped | New entries blocked |
| Correlation (avg pairwise) | Capped | New correlated entries blocked |

Specific threshold values are not published (they're part of the proprietary parameter set). The structure of the limits is what matters for understanding the methodology.

## Position sizing

- **Equal-weight default** on the Sharpe-optimal sleeve. Concentration is the #1 way amateurs blow up; equal-weight forces discipline.
- **Volatility-scaled** within positions: more volatile names get smaller dollar size to equalize risk contribution.
- **Liquidity-constrained**: position size can never exceed N% of average daily volume.

## Exit rules

- **Hard stop-loss** at a fixed percentage below entry.
- **Trailing stops** activate after a position is up by some threshold.
- **Time-stop** on positions that don't move within their thesis window — capital reallocated to opportunities with current signal strength.
- **Scaled exits** on winners — sell partial positions at progressive targets to lock in gains while preserving upside.

## Drawdown protocol

When the portfolio is in drawdown:
1. **-5% from peak**: Normal trading, observation logged
2. **-10% from peak**: Position sizing reduced
3. **-15% from peak**: New entries paused; only manage existing positions
4. **-20% from peak**: Trading halted for at least one full session; methodology review triggered

Each threshold has an exit (return to upper threshold's regime). The drawdown protocol is symmetric — Moot doesn't lift restrictions just because of one good day.

## What "blow up" means and how we prevent it

A blow-up is a single-day or single-week loss that the portfolio can't recover from in a reasonable time. Most retail blow-ups have one of three causes:
1. Position concentration (one trade is too big)
2. Correlated bets (multiple positions are the same trade in disguise)
3. Leverage without limits

Moot's framework addresses each: equal-weight prevents #1, correlation guard prevents #2, leverage cap prevents #3.

The experiment may still produce a losing month or losing quarter. It should not produce a blow-up. If it does, the postmortem goes in this document.
