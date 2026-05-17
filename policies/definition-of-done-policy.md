# Definition of Done Policy

## Purpose

Define when a delivery or initiative can be considered complete.

---

## Principle

Code delivered does not mean the initiative is done.

Done requires implementation, validation, evidence, required approvals, observability when applicable and knowledge capture.

---

## General Definition of Done

A delivery is Done only when:

1. implementation is complete
2. required validations are executed
3. evidence is recorded
4. human approval is completed when required
5. deployment or resolution is completed
6. observability is checked when applicable
7. artifacts are updated
8. next state is defined: observing, closed or archived

---

## FAST DoD

Required:

- implementation complete
- minimal tests executed
- `05-validation/validation-report.md`
- developer review
- PR/deploy/resolution recorded
- `05-validation/pr-summary.md` if PR exists

---

## HYBRID DoD

FAST +

- integration tests
- rollout plan updated
- observability checklist
- integration impact checked
- selective Tech Lead review if required

---

## SAFE DoD

HYBRID +

- contract validation
- regression tests
- rollback plan approved
- deployment checklist
- Tech Lead approval
- approval record updated
- post-deploy observability evidence
- security/risk evidence if applicable

---

## Entry Lane Additions

### Product

- functional acceptance ready for PM/Product validation

### Operational

- bug/incident resolved or mitigated
- evidence of normalization/workaround recorded

### Engineering

- technical objective achieved
- collateral impact checked

### Compliance

- evidence of remediation captured
- audit/finding updated if applicable

---

## Archive Requirement

Before archiving, AI must generate:

```text
initiative-summary.md
```

SAFE initiatives require human validation before archive.
