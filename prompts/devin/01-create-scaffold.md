# Prompt 01 — Create Scaffold

Proceed with creating the AI-CDAD v1 scaffold.

Create all folders and files in this repository.

Populate every file with useful initial content.
Do not create empty placeholders.

Mandatory rules:
- Product Discovery Agent is external.
- AI-CDAD governs.
- AI-DLC structures the lifecycle.
- Devin is a guided orchestrator.
- Developer owns execution.
- Tech Lead owns architecture and risk.
- FAST / HYBRID / SAFE must be explicit.
- Product / Operational / Engineering / Compliance lanes must be explicit.
- runtime-context.md must be the primary runtime context.
- context minimization must be enforced.
- token budgets must exist.
- hard stops must exist.
- Definition of Ready must exist.
- Definition of Done must exist.
- parallel execution governance must exist.


---

## Source of Truth Rule

README.md is the source of truth for the framework.

If any file conflicts with README.md, architecture/source-of-truth.md or docs/notes/decisions-log.md, follow this priority:

1. README.md
2. architecture/source-of-truth.md
3. docs/notes/decisions-log.md
4. policies/
5. playbooks/
6. templates/
7. examples/

Do not contradict the source of truth.
