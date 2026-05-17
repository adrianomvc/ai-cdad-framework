# Human Approval Policy

## Purpose

Define how human approvals happen and how they are recorded.

---

## Principle

```text
Approve where work happens.
Record officially in AI-CDAD artifacts.
```

Humans should not manually fill long approval documents from scratch.

AI drafts the approval record.

---

## Approval Channels

Approvals may happen in:

- Teams
- PR comments
- issue comments
- Devin session
- workflow tools
- repository checklist

---

## Official Record

Critical approvals must be recorded in:

```text
approval-record.md
```

---

## When Approval Is Required

| Situation | Required Approval |
|---|---|
| SAFE technical design | Tech Lead |
| Developer execution readiness | Developer |
| Contract/schema/API/event change | Tech Lead |
| Production deploy | Tech Lead + Developer |
| PII/security/privacy | Security/Risk + Tech Lead |
| Destructive operation | Tech Lead + rollback plan |
| Compliance evidence | Security/Risk |
| Low confidence | appropriate owner |

---

## Approval Record Must Include

- decision requested
- risk summary
- evidence references
- approver
- role
- channel
- date
- decision
- conditions

---

## Approval Types

- Approved
- Approved with conditions
- Rejected
- Needs more information

---

## Rule

If approval is required but missing, Devin must stop.
