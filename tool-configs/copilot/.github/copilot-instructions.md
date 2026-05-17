# GitHub Copilot Instructions — AI-CDAD

This repository uses AI-CDAD — AI Context-Driven Adaptive Delivery.

When helping with this repository:

1. Look for `.cdad/initiatives/<initiative-id>/00-flow-index.md`.
2. Look for `.cdad/initiatives/<initiative-id>/04-execution/runtime-context.md`.
3. Look for `.cdad/initiatives/<initiative-id>/04-execution/ai-execution-brief.md`.
4. Respect scope and out of scope.
5. Do not suggest changes to blocked files.
6. Do not bypass hard stops.
7. Do not modify APIs, schemas, contracts, IAM/security or production behavior unless explicitly approved.
8. Suggest tests and validation evidence for every meaningful change.
9. Keep changes small and explainable.
10. Never include secrets, customer data or sensitive logs.
11. Infer the human-facing language from the user's request, existing artifacts and repository/team conventions.
12. If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default.
13. Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.

The Developer owns execution and review.
