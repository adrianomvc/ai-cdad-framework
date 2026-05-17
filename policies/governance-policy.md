# Governance Policy

## Purpose

Define when AI-CDAD must stop, request human approval, escalate, or continue.

---

## Principle

AI may accelerate execution but cannot accept risk on behalf of humans.

---

## Hard Stops

Devin must stop when any of the following is detected:

1. production change
2. API/data contract/schema/event change
3. PII or sensitive data
4. IAM/security permission change
5. destructive operation
6. relevant cost impact
7. low AI confidence
8. SAFE mode without required approvals
9. critical conflict with another active initiative
10. migration without rollback strategy
11. deploy without validation evidence
12. unclear owner for a risky change

---

## Hard Stop Behavior

When a hard stop is triggered, Devin must:

1. stop execution
2. explain the risk
3. identify the required approver
4. create or update `governance-hard-stop.md` or `cdad-exception-report.md`
5. request the minimum decision needed
6. continue only after approval or plan adjustment

---

## Approval Matrix

| Trigger | Required Approval |
|---|---|
| SAFE technical design | Tech Lead |
| Developer execution readiness | Developer |
| Contract/schema change | Tech Lead |
| PII/security/privacy | Tech Lead + Security/Risk |
| Production deploy | Tech Lead + Developer |
| Compliance evidence | Security/Risk |
| Destructive operation | Tech Lead + rollback/backup plan |
| IAM/security permission | Tech Lead + Security/Risk |
| Cost-impacting change | Tech Lead / FinOps owner if applicable |

---

## Escalation Rules

| Situation | Escalate To |
|---|---|
| business scope ambiguity | PM / Product |
| architecture risk | Tech Lead |
| execution ambiguity | Developer |
| security/privacy risk | Security/Risk |
| production incident | Tech Lead + Dev on-call |
| cost risk | FinOps / Tech Lead |
| ownership unknown | responsible manager / Tech Lead |

---

## Safe Defaults

- Unknown production impact → treat as potential production impact.
- Unknown contract impact → require assessment.
- Unknown data sensitivity → stop and ask.
- Unknown ownership → stop and ask.
- Risk ambiguity → increase rigor.
- Missing approval → do not proceed.

---

## Evidence

Every critical decision must be recorded in:

```text
approval-record.md
```

or, for exceptions:

```text
cdad-exception-report.md
```
