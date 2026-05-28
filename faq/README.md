# FAQ

Common questions about the trade-with-moot experiment.

## Is this financial advice?

No. This is research entertainment about an AI experiment. Watching the experiment is not what you should do with your money. Every post carries the disclaimer; the disclaimer is the operating principle, not a footer.

## Are you a registered investment adviser?

No. The operator does not give personalized investment advice, does not run a managed account or fund, and does not sell trade signals as a subscription product. Under the *Lowe v. SEC* publisher exemption and FINRA Rule 2210 framing, public after-the-fact commentary on an AI experiment is publisher territory, not adviser territory.

## Will there ever be a paid signals product?

No. There will never be a paid signals product, a managed account, a fund, a course, sponsorships, or merch tied to this experiment. The moment we sell anything, we have a financial interest in the experiment looking good — and the whole point is that the experiment's outcome should be reported honestly whether it is good, bad, or neutral. No commercial layer, ever.

The only support surface is cost-recovery donations via [buymeacoffee.com/tradewithmoot](https://buymeacoffee.com/tradewithmoot), capped at 1.5× monthly compute cost. Surplus goes to AI safety and open-source AI research nonprofits — METR, MIRI, Apollo Research, ARC Evals, EleutherAI, LAION, the HF Open-Source Fund.

## Why anonymous?

To force the credibility focus onto the work, not the operator. Anonymous research has a long history — pseudonymous quants, synthetic personas in marketing, the entire culture of pseudonymous blogging. The Day-1,095 retrospective will include an optional identity reveal — by then, the work will speak for itself or it won't.

## How can I trust the trades are real?

The live dashboard at [tradewithmoot.streamlit.app](https://tradewithmoot.streamlit.app) is backed by the actual Alpaca brokerage account. You can verify cumulative P&L, drawdown, position count, and trade history at any time. If a claim in this repository disagrees with the dashboard, **trust the dashboard** and file an issue.

## Can I see the bot's source code?

No. The bot is closed-source. So are the signals, weights, prompts, and parameters. The architecture is documented in [docs/ARCHITECTURE.md](../docs/ARCHITECTURE.md); the parameters are not. For the explicit list of what's closed and why, see [what-is-NOT-here.md](../what-is-NOT-here.md).

## Why closed-source? Isn't open source more honest?

Open architecture is the honest version. Open *parameters* would be a different experiment — one where the published material gets cloned, and the question becomes "how do clones of the recipe perform" rather than "how does this specific bot perform." The closed parameters are the isolation chamber that makes the receipts mean something.

## Will the experiment make money?

Unknown. That's literally the experiment. If we knew the answer, we wouldn't need to run it for 1,095 days.

## What's actually live right now?

Phase 1 — the V3 portfolio (diversified Sharpe-optimal core) — went live with real money on 2026-05-22. Phase 1.5 — the AI-infrastructure sleeve (20-name conviction book) — went live 2026-05-27. Phase 2 (intraday) and Phase 3 (options) are designed but not live; they ship later in 2026 with their own founding statements.

## Where are the backtests?

In the [README](../README.md) and in [performance/](../performance/). V3 OOS Sharpe by historical regime and AI sleeve total return vs SPY across five regimes. Honest framing: high-beta in growth, brittle in bear.

## What happens at Day 1,095?

A full retrospective: cumulative P&L, methodology evolution, what worked, what didn't, what's next. Optional identity reveal at operator discretion. Whatever the outcome, the retrospective gets published — a bad outcome is not a reason to bury the experiment, that would defeat its purpose. The retrospective is the contract.

## How do I contact you?

Via the issues tab on this repo. The operator's identity is private. Genuine methodology questions and corrections will get responses. Bad-faith engagement gets locked without comment.

## Why the cozy aesthetic for a trading bot?

Because the entire visual language of retail trading content has converged on red candles, green arrows, lambo emojis, and Wall Street Bets bro energy. That aesthetic correlates with bad outcomes for the audiences consuming it. A 3-year experiment in calibrated, rule-based, anti-hype AI agency deserves the opposite visual register. Restrained, methodical, principled. Paper-craft chibi Moot is the avatar of that posture.
