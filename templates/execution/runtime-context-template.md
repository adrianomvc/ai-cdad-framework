# Runtime Context

## Purpose

This is the primary context loaded into the AI execution session.

It must be concise, evidence-based and sufficient for the current phase.

---

## Goal

What must be achieved in this execution.

---

## Language and Locale

- Preferred human-facing language:
- Inferred from:
- Use Portuguese Brazilian (`pt-BR`) by default when the user communicates in Portuguese.
- Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.
- Ask one short clarification question if the language preference is unclear or conflicting.

---

## Entry Lane

Product | Operational | Engineering | Compliance

---

## Risk Mode

FAST | HYBRID | SAFE

---

## Scope

What may be changed.

---

## Out of Scope

What must not be changed.

---

## Required Gates

- [ ] Developer feasibility
- [ ] Tech Lead approval, if required
- [ ] Security/Risk approval, if required
- [ ] Contract validation, if required
- [ ] Rollback plan, if required

---

## Critical Constraints

List constraints that must not be violated.

---

## Evidence References

Link to evidence instead of copying everything.

| Evidence | Location | Why it matters |
|---|---|---|

---

## Stop Conditions

Stop if:

- contract/schema/API/event impact is discovered
- production impact is higher than expected
- PII/sensitive data is found
- IAM/security permission change is needed
- scope becomes unclear
- tests indicate unexpected regression
- context is insufficient

---

## Human Owners

| Role | Name | Responsibility |
|---|---|---|

---

## Validation Requirements

- tests:
- contract validation:
- regression:
- observability:
- PR review:

---

## Relevant Files

Use `04-execution/relevant-files-list.md` for details.

---

## Context Budget

- target:
- max:
- estimated:
- context-reduction-plan needed? yes/no
