# Failure Handling Policy

## Purpose

Define what Devin must do when something goes wrong or when context is insufficient.

AI-CDAD must prevent silent improvisation.

---

## Exception Types

### 1. Retry

Use for transient failures:

- temporary MCP/source unavailability
- flaky tests
- temporary network/tool error
- temporary repository access issue

Retry must be limited. If repeated, escalate.

### 2. Missing Context

Use when critical information is missing.

Examples:

- impacted repository is unknown
- component is unknown
- production impact is unknown and relevant
- contract/schema impact is unclear
- data sensitivity is unclear
- owner is unknown
- required approval is missing

Behavior:

1. stop
2. explain what is missing
3. ask only for the minimum information needed
4. create/update `cdad-exception-report.md`

Required message pattern:

```text
I cannot continue safely because <missing context> is missing.

To continue, I only need:
1. ...
2. ...
```

### 3. Escalation

Use when human judgment is needed.

Examples:

- architecture risk
- security/privacy risk
- business scope ambiguity
- production incident
- low AI confidence
- hard stop
- conflict with another active initiative

### 4. Stop

Use when continuing is unsafe.

Examples:

- destructive operation without approval
- production change without rollback
- SAFE without Tech Lead approval
- contract change without validation
- PII exposure risk
- secrets detected

---

## Required Artifact

Create or update:

```text
cdad-exception-report.md
```

---

## Decision Rule

If the issue changes risk classification, return to Delivery Assessment.

If the issue changes technical direction, return to Tech Lead Design.

If the issue changes execution scope, return to Developer Feasibility Gate.
