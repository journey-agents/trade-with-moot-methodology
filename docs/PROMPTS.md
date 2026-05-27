# Prompts

> **Status:** Seed document. Sanitized prompts fill in as the experiment evolves.

## Why this document exists

A Claude Code-based trading system is, at the implementation level, a collection of prompts that route LLM reasoning through specific decision tasks. The shape of those prompts — their structure, what context they receive, what they're asked to produce — is methodology. The specific parameter values within them is proprietary.

This document publishes the shape; the parameter values stay in the bot's private repo.

## Sample (sanitized): regime classification prompt

```
SYSTEM: You are a market regime classifier. Given the market data below,
output a JSON object with: {regime: ..., confidence: ..., reasoning: ...}.
Valid regimes: trending_up, trending_down, mean_reverting, volatile, quiet.
Be conservative — when in doubt, output "quiet" with low confidence.

DATA:
- SPY 20/50/200 SMA position: <provided>
- VIX level: <provided>
- Sector dispersion: <provided>
- Recent macro data points: <provided>

OUTPUT JSON ONLY.
```

The sanitization removes:
- Exact threshold values that classify "high VIX"
- The specific list of macro data points
- The internal weighting of features

## Skill structure

Moot's Claude Code plugin uses skills (slash commands) for high-level user-facing operations. Each skill is itself a prompt template wrapped around tool calls. The skills are documented in the bot's CLAUDE.md (private), but the category list is public:

- Stock analysis (multi-dimension)
- Portfolio review (live broker positions)
- Recommendation (top N picks)
- Scanner (custom screening)
- Risk dashboard (limits + exposure)
- Regime detection
- Trade execution
- Briefing (morning summary)
- Backtest
- Compare (side-by-side)
- Rebalance (Sharpe-optimal)
- Options analysis
- Tax-loss harvesting

13 skills. The structure is here; the specifics are not.

## Prompt evolution

Moot's prompts evolve as the experiment runs. Major prompt revisions trigger a methodology-essay post on Substack and a new sample in this document.
