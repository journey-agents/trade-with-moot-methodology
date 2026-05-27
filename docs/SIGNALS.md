# Signals

> **Status:** Seed document. Per-signal performance attribution fills in as the experiment runs.

Moot reads 8 categories of signals. Each signal returns a normalized score (strength 0-1, direction BUY/SELL/HOLD). The signals feed the fusion layer; no single signal triggers a trade.

## 1. Technical signals
Price action, moving averages, momentum, mean reversion, volume confirmation. Multi-timeframe (intraday, daily, weekly).

## 2. Fundamental signals
Earnings trajectory, free cash flow, revenue growth, balance sheet health, sector-relative valuation.

## 3. Sentiment signals
News sentiment, social-media sentiment (carefully sampled — Moot is skeptical of social-driven moves). Magnitude and direction.

## 4. Macro signals
Interest rate environment, yield curve, dollar strength, sector rotation signals, business cycle position.

## 5. Options flow
Unusual options activity, IV percentile, put/call ratios, gamma positioning. Used as a confirmation signal, not a primary driver.

## 6. Insider activity
SEC Form 4 filings — buys and sells by insiders. Cluster behavior matters more than single trades.

## 7. Institutional holdings
13F filings, ownership changes, smart-money concentration. Slow-moving but high-quality.

## 8. Catalyst events
Earnings announcements, FDA approvals, court rulings, regulatory decisions, central bank meetings. Time-decay matters; signals fade after the event.

## What we publish

For each signal category:
- The conceptual role (what question it answers)
- The general data source and timeframe
- How the category enters the fusion layer (high level)
- Sample of recent decisions where this signal mattered

## What we don't publish

- Exact signal weights in the Bayesian fusion
- Threshold values for "strong" vs. "weak" signals
- Internal calibration data
- Custom signal-derivation code

## Signal effectiveness tracking

Moot tracks per-signal attribution: of the trades that won/lost, which signals were strongest at entry? Monthly attribution reports go in `performance/`.
