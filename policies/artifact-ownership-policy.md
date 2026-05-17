# Artifact Ownership Policy

## Purpose

Define who creates, owns and validates AI-CDAD artifacts.

---

## Principle

```text
AI drafts.
Human owns.
```

The human does not fill long documents from scratch.

AI creates drafts and asks for validation only when necessary.

---

## Location Rules

| Artifact Type | Location |
|---|---|
| framework methods | ai-cdad-framework |
| policies/templates/playbooks | ai-cdad-framework |
| domain/product context | central community repo |
| cross-repo initiative artifacts | central community repo |
| local execution artifacts | application repo |
| runtime-context.md | application repo |
| devin-execution-brief.md | application repo |
| local validation evidence | application repo |
| archived summary | central community repo |

---

## Ownership Matrix

| Artifact | AI Drafts | Human Owner |
|---|---|---|
| normalized-entry.md | Intake Agent | requester / lane owner |
| triage-report.md | Devin | Dev/TL/Security depending on lane |
| delivery-assessment.md | Delivery Assessment Agent | TL if ambiguous/critical |
| mcp-query-plan.md | Tech Lead Design Agent | Tech Lead |
| technical-context-pack.md | Tech Lead Design Agent | Tech Lead |
| impact-analysis.md | Tech Lead Design Agent | Tech Lead |
| lean-sdd.md | Tech Lead Design Agent | Tech Lead |
| runtime-context.md | Devin | Developer |
| local-shaping-plan.md | Shaping Agent | Developer |
| devin-execution-brief.md | Devin | Developer |
| validation-report.md | Validation Agent | Developer |
| approval-record.md | Devin | approver |
| rollback-plan.md | Devin/TL Agent | Tech Lead |
| initiative-summary.md | Knowledge Update Agent | Dev/TL depending on risk |

---

## Communication Rule

When Devin creates or updates an artifact, it must state:

- what was created/updated
- where it is located
- why it exists
- who must validate it
- next step
