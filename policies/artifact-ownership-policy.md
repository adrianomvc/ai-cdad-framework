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
| 00-flow-index.md | application repo |
| 04-execution/runtime-context.md | application repo |
| 04-execution/ai-execution-brief.md | application repo |
| local validation evidence | application repo |
| archived summary | central community repo |

---

## Ownership Matrix

| Artifact | AI Drafts | Human Owner |
|---|---|---|
| normalized-entry.md | Intake Agent | requester / lane owner |
| triage-report.md | AI Execution Agent | Dev/TL/Security depending on lane |
| delivery-assessment.md | Delivery Assessment Agent | TL if ambiguous/critical |
| mcp-query-plan.md | Tech Lead Design Agent | Tech Lead |
| technical-context-pack.md | Tech Lead Design Agent | Tech Lead |
| impact-analysis.md | Tech Lead Design Agent | Tech Lead |
| lean-sdd.md | Tech Lead Design Agent | Tech Lead |
| 00-flow-index.md | AI Execution Agent | Developer |
| 04-execution/runtime-context.md | AI Execution Agent | Developer |
| 03-design/local-shaping-plan.md | Shaping Agent | Developer |
| 04-execution/ai-execution-brief.md | AI Execution Agent | Developer |
| 05-validation/validation-report.md | Validation Agent | Developer |
| 06-governance/approval-record.md | AI Execution Agent | approver |
| 03-design/rollback-plan.md | AI Execution Agent / Tech Lead Agent | Tech Lead |
| initiative-summary.md | Knowledge Update Agent | Dev/TL depending on risk |

---

## Communication Rule

When an AI Execution Agent creates or updates an artifact, it must state:

- what was created/updated
- where it is located
- why it exists
- who must validate it
- next step
