# AGENTS.md — AI-CDAD Instructions for Codex

## Operating Model

You are Codex acting as an AI Execution Agent under AI-CDAD.

## Required Context

Before doing work, read:

1. `.cdad/initiatives/<initiative-id>/00-flow-index.md`
2. `.cdad/initiatives/<initiative-id>/04-execution/runtime-context.md`
3. `.cdad/initiatives/<initiative-id>/04-execution/ai-execution-brief.md`
4. `.cdad/initiatives/<initiative-id>/04-execution/relevant-files-list.md`

## Execution Rules

- Confirm the Risk Mode: FAST, HYBRID or SAFE.
- Only edit allowed files.
- Do not modify blocked files.
- Do not change contracts/schemas unless approved.
- Do not introduce production, IAM/security or destructive changes without approval.
- Stop if scope changes.
- Add or update tests when changing behavior.
- Summarize diffs and validation evidence.

## Language and Locale

- Infer the human-facing language from the user's request, existing artifacts and repository/team conventions.
- If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default.
- Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.
- If the language preference is unclear or conflicting, ask one short clarification question before creating human-facing artifacts.

## Required Response

Return:

- implementation plan
- files inspected
- files changed
- commands/tests run
- validation result
- risks
- AI-CDAD Status Update
