# Delivery Routing Policy

## Purpose

Define how AI-CDAD classifies work into FAST, HYBRID or SAFE.

The classification must be policy-based, not based on model intuition.

---

## Inputs

- `normalized-entry.md`
- `triage-report.md`, when applicable
- known impacted repositories
- known impacted components
- known production impact
- known contract/schema/API/event impact
- known data sensitivity
- known rollback complexity
- known confidence level

---

## FAST

Use FAST when all or most of the following are true:

- low risk
- isolated/local change
- simple bug fix
- small refactor
- no production criticality
- no API/data contract/schema/event change
- no PII/sensitive data
- no IAM/security permission change
- simple rollback
- limited blast radius
- high AI confidence
- clear owner

### FAST Required Gates

- Developer review
- minimal tests
- validation report
- PR summary, when code is changed

### FAST Must Not Be Used When

- production impact is unknown and relevant
- contract/schema impact is unknown and relevant
- PII sensitivity is unknown
- rollback is unclear
- ownership is unclear
- confidence is low

---

## HYBRID

Use HYBRID when:

- new work integrates with existing systems
- there are known dependencies
- there are known internal consumers
- production impact exists but is limited and controlled
- rollout should be controlled
- technical risk exists but is understood
- Tech Lead review may be useful but not always mandatory

### HYBRID Required Gates

- Developer feasibility
- integration validation
- observability readiness
- selective Tech Lead review when architecture, integration or contract risk appears

---

## SAFE

Use SAFE when any of the following is true:

- existing production capability is changed
- API/data contract/schema/event may change
- multiple consumers may be impacted
- PII or sensitive data is involved
- IAM/security permissions are involved
- destructive operation is involved
- migration is required
- rollback is complex
- compliance/security remediation is involved
- production incident is relevant
- AI confidence is low
- context is insufficient
- ownership is unclear
- conflict exists with another active initiative on critical component/contract

### SAFE Required Gates

- Tech Lead approval
- Developer feasibility
- rollback plan
- validation plan
- contract validation, if applicable
- regression validation, if applicable
- security/risk approval, if applicable
- approval record

---

## Safe Default

If relevant uncertainty exists, increase rigor:

```text
FAST → HYBRID → SAFE
```

Examples:

| Unknown | Default Behavior |
|---|---|
| unknown production impact | treat as potential production impact |
| unknown contract impact | require assessment before execution |
| unknown data sensitivity | stop and ask |
| unknown owner | stop and ask |
| low confidence | classify SAFE or stop |
| unclear rollback | classify SAFE |

---

## Output

The Delivery Assessment Agent must create:

```text
delivery-assessment.md
```

Required sections:

- recommended risk mode
- rationale
- triggered rules
- required gates
- safe defaults applied
- open questions
- human review required
- confidence
