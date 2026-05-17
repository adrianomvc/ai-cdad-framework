# Definition of Ready Policy

## Purpose

Define the minimum information required before a phase can advance.

The goal is to avoid heavy forms while preventing unsafe execution.

---

## Principle

```text
Minimum required information to move safely.
Maximum lightness for the human.
```

---

## Ready for Intake

Minimum:

- problem or request
- source/origin
- urgency if known
- impacted system/repo if known
- evidence if available

If missing, Devin asks only for the minimum needed.

---

## Ready for Triage

Required for Operational, Compliance or ambiguous Engineering requests.

Minimum:

- normalized entry
- issue type or suspected issue type
- affected system or unknown marker
- urgency
- available evidence
- production impact if known

---

## Ready for Delivery Assessment

Minimum:

- `normalized-entry.md`
- `triage-report.md`, if required
- known or unknown impacted repos
- known or unknown production impact
- known or unknown contract/schema impact
- known or unknown data sensitivity

---

## Ready for Tech Lead Design

Required for HYBRID/SAFE or technical ambiguity.

Minimum:

- `delivery-assessment.md`
- risk mode
- entry lane
- impacted repositories/components
- known open questions
- MCP query plan if external technical context is needed

---

## Ready for Shaping

Minimum:

- design direction or explicit FAST decision
- impact analysis if HYBRID/SAFE
- Tech Lead approval if required
- known execution constraints
- known validation requirements

---

## Ready for AI Execution

Minimum:

- `runtime-context.md`
- `local-shaping-plan.md` or equivalent
- `ai-execution-brief.md`
- risk mode
- developer owner
- scope
- out of scope
- hard stops
- stop conditions
- validation requirements
- allowed/relevant files

Developer must validate execution readiness.

---

## Ready for Validation

Minimum:

- implemented change or change set
- tests created/updated
- test execution plan
- PR or diff available
- expected validation artifacts

---

## Ready for Deploy / Resolve

FAST:

- validation report
- tests passed
- developer review

HYBRID:

- FAST requirements
- integration validation
- rollout plan
- observability readiness

SAFE:

- HYBRID requirements
- rollback plan
- contract validation if applicable
- regression validation if applicable
- Tech Lead approval
- approval record

---

## Missing Context Rule

If not ready, the AI Execution Agent must stop and say:

```text
I cannot continue safely because <missing context> is missing.

To continue, I only need:
1. ...
2. ...
```
