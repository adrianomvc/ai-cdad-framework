# GitHub Copilot Instructions — AI-CDAD

This repository uses AI-CDAD — AI Context-Driven Adaptive Delivery.

When helping with this repository:

1. Look for `.cdad/initiatives/<initiative-id>/runtime-context.md`.
2. Look for `.cdad/initiatives/<initiative-id>/ai-execution-brief.md`.
3. Respect scope and out of scope.
4. Do not suggest changes to blocked files.
5. Do not bypass hard stops.
6. Do not modify APIs, schemas, contracts, IAM/security or production behavior unless explicitly approved.
7. Suggest tests and validation evidence for every meaningful change.
8. Keep changes small and explainable.
9. Never include secrets, customer data or sensitive logs.
10. Infer the human-facing language from the user's request, existing artifacts and repository/team conventions.
11. If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default.
12. Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.

The Developer owns execution and review.
