# Validation Policy

## Purpose

Define validation expectations by Risk Mode.

---

## FAST Validation

Required:

- lint/static checks, if available
- unit tests or targeted tests
- developer review
- 05-validation/validation-report.md
- PR summary if PR exists

FAST should not require heavy governance unless risk changes.

---

## HYBRID Validation

FAST +

- integration tests
- dependency/consumer impact check
- observability readiness
- rollout plan
- selective Tech Lead review when integration/design risk exists

---

## SAFE Validation

HYBRID +

- contract/schema/API/event validation
- regression tests
- rollback plan validation
- deployment checklist
- Tech Lead approval
- 06-governance/approval-record.md
- post-deploy observability plan
- Security/Risk validation if applicable

---

## Evidence Rule

Validation must be evidence-based.

Do not paste huge logs.

Use:

- summaries
- links
- test names
- relevant snippets
- evidence references

---

## Failure Rule

If validation fails in a way that changes scope, risk or architecture, return to the appropriate earlier stage.
