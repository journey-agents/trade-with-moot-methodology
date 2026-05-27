# trade-with-moot-methodology

**This documents how Moot thinks. It is not Moot.**

Moot is an AI trading experiment running publicly on Alpaca. This repository documents the architecture, signals, decision framework, risk management, and reproducibility material behind that experiment — what an outside engineer or researcher needs to understand how the system makes decisions, without exposing the live trading code itself.

We are running this experiment to answer one question: **Can AI really make money on stocks?** We'll find out over 1,095 days. The trades go out publicly to Alpaca. The methodology goes here.

## What this repo is

- A reproducible-in-principle account of the experiment's architecture
- Monthly long-form essays (companion to Substack publication)
- Performance reports tied to verifiable Alpaca portfolio share links
- The contractual artifact of the 3-year experiment

## What this repo is NOT

- The trading bot's source code (closed-source by design)
- Real-time signal alerts (none exist — there is no paid product)
- Investment advice (it isn't, ever)

## Reading order

1. `docs/ARCHITECTURE.md` — high-level system architecture
2. `docs/DECISION-FRAMEWORK.md` — how Moot weighs signals into actions
3. `docs/SIGNALS.md` — what signals Moot reads (8 categories)
4. `docs/RISK-MANAGEMENT.md` — position sizing, max drawdown, daily-loss limits
5. `docs/PROMPTS.md` — sanitized prompts (architecture without parameters)
6. `docs/REPRODUCIBILITY.md` — what you'd need to rebuild a similar system
7. `essays/` — monthly long-form essays
8. `performance/` — month-end P&L summaries

## Status

Repository seeded 2026-05-27. Content evolves as the experiment runs. See [trade-with-moot Substack](https://tradewithmoot.substack.com) (coming) for parallel publication.

## License

Documentation is CC-BY-SA-4.0. Code samples (if any) are MIT. See [LICENSE](LICENSE).

## Contribution

Issues open for questions, corrections, methodology challenges. Pull requests closed (single-author project). See [CONTRIBUTING.md](CONTRIBUTING.md).

## Not advice

Watching this experiment is not investment advice. The experiment may produce positive returns, may produce negative returns, may produce nothing notable. The whole point is finding out.
