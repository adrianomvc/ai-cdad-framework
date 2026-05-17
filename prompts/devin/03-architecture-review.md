# Prompt 03 — Architecture Review

Perform an architecture review of the generated AI-CDAD framework.

Check for missing policies, duplicated concepts, heavy process, token bloat, ambiguous ownership, unsafe brownfield assumptions, missing AI-DLC integration, missing runtime-context model, missing stop conditions, missing operational lane, missing hub vs application repo distinction, and missing parallel execution governance.

Return findings only. Do not change files yet.


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
