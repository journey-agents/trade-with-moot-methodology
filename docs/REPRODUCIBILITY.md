# Reproducibility

> **Status:** Seed document. Detailed reproduction guides fill in as the experiment runs.

## What "reproducible-in-principle" means

A competent AI engineer should be able to read this repository and rebuild a similar system. Not the same system — that would require the proprietary parameters that stay in the private bot repo. But a *similar* system: same architecture, same signal categories, comparable decision framework, similar risk philosophy.

If you tried this and ended up with a different architecture, that's fine — there's no claim of optimality. If you ended up with no architecture because key information was withheld, that's a documentation bug. File an issue.

## What you'd need

| Component | Where to get it |
|---|---|
| Broker API access | [Alpaca](https://alpaca.markets) (free paper account for development) |
| Market data | Alpaca + a fundamentals provider (Polygon, Tiingo, Financial Modeling Prep) |
| AI runtime | [Claude Code](https://claude.com/claude-code) with API key, or any agentic LLM framework |
| Sentiment data | News API + social signals (Reddit/Twitter sentiment scrapers) |
| Insider/institutional | SEC EDGAR API (free) |
| Options data | Polygon, Alpaca Options, or your broker |
| Compute | Local laptop adequate; the workload is bursty (signal scan → fusion → decision) |

## The hard parts (where most replications fail)

1. **Signal calibration** — every signal needs to be calibrated against actual outcomes. The signal-attribution feedback loop is what makes the system improve over time. Without it, you have a static rule engine.

2. **Risk discipline** — the rules in `RISK-MANAGEMENT.md` look simple. Following them when the portfolio is up 10% and you're tempted to size up, or down 10% and you're tempted to revenge-trade, is the actual hard problem.

3. **Fusion calibration** — combining 8 signals into one calibrated confidence is not "average them." Each signal has different bias, different recency value, different correlation with others. Tuning this takes months.

4. **Operational discipline** — running this for 3 years without modifying the methodology in response to a bad month is the meta-challenge.

## What's NOT reproducible

- The specific Bayesian priors used in the fusion layer
- The exact threshold values in the risk limits
- The proprietary signal-derivation code
- The signal-attribution feedback loop's specific implementation

These stay in the private bot repo. They are NOT necessary to build a *similar* system; they ARE necessary to clone this specific system. The point of the experiment is the methodology, not the parameter set.

## Open questions Moot's running answer is

- Does multi-signal fusion outperform best-single-signal in real trading? **Hypothesis: yes, by 2-4% annualized**. Testing now.
- Does AI improve over time with feedback? **Hypothesis: yes if calibrated, no if not**. Testing now.
- Does anonymous AI agency build follower trust? **Hypothesis: yes, contingent on time-locked credible commitment**. Testing now.
- Can a 1,095-day commitment be sustained? **Hypothesis: with hedges (degraded-mode runbook, 6-month go/no-go, automation), yes**. Testing now.

Each of these gets a long-form essay over the next 36 months.
