# Prompts

## The closed-parameter posture

Prompt templates are not published. The shapes, structures, parameter slots, and routing decisions inside the agentic layer are part of the proprietary methodology and stay closed for the experiment's duration.

This is intentional. The recipe is closed; the architecture is open. See [../what-is-NOT-here.md](../what-is-NOT-here.md).

## Why this category specifically

There is a temptation, when writing about an LLM-based system, to publish "sanitized" prompt samples — the structure of the prompt with the parameter values redacted. That temptation is rejected here. A prompt's structure carries more of the methodology than the parameter values do; publishing the shape and redacting the numbers exposes the framework while pretending it doesn't.

The same principle applies to skill / subagent / routing inventories. The list of decision tasks the system routes through LLM reasoning is itself a proprietary parameter — it tells you what shape of work the system splits into LLM steps versus deterministic steps. That decomposition is methodology.

## What about the architecture diagram?

The architecture diagram in [ARCHITECTURE.md](ARCHITECTURE.md) is a single-page conceptual flow at the layer above prompts. It shows the gates a trade has to pass; it does not show the internal decomposition of the agentic layer, the specific routing decisions, or the prompts themselves. The diagram is the bounded reveal.

## Day-1,095

The Day-1,095 retrospective MAY include sanitized prompt samples in the final write-up, with the parameter slots empty and the structure clearly marked as one *instance* of how this work was decomposed. That decision is made at Day 1,095, not earlier and not promised earlier.
