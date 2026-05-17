# FAQ

## Is AI-CDAD only for Devin?

No. Devin is the first supported implementation, but AI-CDAD is tool-agnostic.

It can work with Claude Code, Codex, Cursor, GitHub Copilot, Amazon Q, StackSpot AI, ResolveAI or internal agents.

## Is AI-CDAD a replacement for SDLC?

No. AI-CDAD complements existing SDLC/AI-DLC practices by adding context, risk routing, human gates and AI execution governance.

## Does AI-CDAD slow teams down?

It should not.

FAST mode is designed to be lightweight. SAFE mode is intentionally stronger for brownfield, production, contracts, PII and compliance.

## Who owns the final decision?

Humans.

- PM owns value and priority.
- Tech Lead owns architecture and risk.
- Developer owns execution and PR quality.
- Security/Risk owns security and compliance validation when applicable.

## What is the most important artifact?

`runtime-context.md`.

It is the primary context loaded into the AI execution session.

## What is the difference between runtime-context and execution brief?

`runtime-context.md` explains the current situation and constraints.

`ai-execution-brief.md` tells the AI Execution Agent exactly what it is allowed to do.

## Can I use this in a personal repo?

Yes, but never include corporate secrets, customer data, PII, production logs or proprietary internal information.

## What should I run first with Devin?

Run:

```text
prompts/devin/00-plan-before-files.md
```

Do not allow file changes before Devin returns a plan.
