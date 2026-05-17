# Prompt 04 — Apply Corrections

Apply the corrections from the architecture review.

Prioritize safety, developer clarity, token minimization, brownfield governance, runtime simplicity, lightweight FAST mode, and clear AI-DLC integration.

Return files changed, why each change was made, and remaining risks.


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
