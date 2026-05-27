# Architecture

> **Status:** Seed document. Content fills in as the experiment runs.

## High-level overview

Moot is a Claude Code–based agentic trading system. The architecture has four layers:

### 1. Signal layer
Reads market data, fundamentals, sentiment, macro indicators, options flow, insider activity, institutional holdings, and sector rotation. Each signal returns a normalized score (strength 0-1, direction BUY/SELL/HOLD).

### 2. Fusion layer
Combines signals via Bayesian cross-reference. No single signal triggers a trade; the fusion produces a calibrated confidence score per ticker.

### 3. Portfolio layer
Position sizing via Sharpe-optimal optimization. Equal-weight constraint to avoid concentration. Risk limits per position and per portfolio.

### 4. Execution layer
Connects to Alpaca brokers (paper for public surface, real for monthly verified receipts). Order management, scaled exits, trailing stops.

## Engine

The signal generation, fusion, and portfolio layers are implemented as a Claude Code plugin (`stock-advisor-plugin`) with 99 MCP tools, 13 skills, 4 subagents, and 2,100+ tests. The plugin runs locally; trades execute via the Alpaca API.

## What's published vs. what stays private

| Component | Published here | Stays in private bot repo |
|---|---|---|
| Signal categories + their conceptual role | ✓ | |
| Exact signal weights / Bayesian priors | | ✓ |
| Decision framework (how signals → actions) | ✓ | |
| Position sizing logic at a high level | ✓ | |
| Specific position sizing formulas | | ✓ |
| Risk management philosophy + thresholds | ✓ | |
| Stop-loss and exit-rule code | | ✓ |
| Claude Code skill structure | ✓ | |
| Production prompts (sanitized) | ✓ | |
| Production prompts (raw, full) | | ✓ |
| Backtest methodology | ✓ | |
| Backtest result data | ✓ | |
| Live trading code | | ✓ |

## Reproducibility line

A competent AI engineer reading this repo should be able to **rebuild a similar system** — not the same system, but one with comparable architectural choices. The line we draw is: methodology yes, specific parameters no. The point of the experiment is to demonstrate that the methodology produces (or doesn't produce) returns over 3 years on a public account, not to ship the recipe for free.
