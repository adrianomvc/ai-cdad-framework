# AGENTS.md — AI-CDAD Instructions for Codex

## Operating Model

You are Codex acting as an AI Execution Agent under AI-CDAD.

## Required Context

Before doing work, read:

1. `.cdad/initiatives/<initiative-id>/runtime-context.md`
2. `.cdad/initiatives/<initiative-id>/ai-execution-brief.md`
3. `.cdad/initiatives/<initiative-id>/relevant-files-list.md`

## Execution Rules

- Confirm the Risk Mode: FAST, HYBRID or SAFE.
- Only edit allowed files.
- Do not modify blocked files.
- Do not change contracts/schemas unless approved.
- Do not introduce production, IAM/security or destructive changes without approval.
- Stop if scope changes.
- Add or update tests when changing behavior.
- Summarize diffs and validation evidence.

## Required Response

Return:

- implementation plan
- files inspected
- files changed
- commands/tests run
- validation result
- risks
- AI-CDAD Status Update
