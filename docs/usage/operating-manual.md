# AI-CDAD Operating Manual

## Daily usage

For each demand:

1. Identify Entry Lane.
2. Create or update `normalized-entry.md`.
3. Run triage if needed.
4. Create `delivery-assessment.md`.
5. Classify risk mode: FAST, HYBRID or SAFE.
6. Create or update `00-flow-index.md`.
7. Create `04-execution/runtime-context.md`.
8. Create `04-execution/ai-execution-brief.md`.
9. Run AI Execution Agent.
10. Validate.
11. Review.
12. Deploy or resolve.
13. Observe and archive.

---

## Entry Lane decision

| Lane | Examples |
|---|---|
| Product | feature, product evolution, business enhancement |
| Operational | bug, incident, hotfix, alert |
| Engineering | tech debt, refactor, upgrade, observability |
| Compliance | security, audit, privacy, regulatory remediation |

---

## Risk Mode decision

| Mode | Use when |
|---|---|
| FAST | local, low risk, simple rollback |
| HYBRID | integration with existing systems |
| SAFE | production, contract, PII, IAM, compliance, migration, low confidence |

Safe default:

```text
FAST → HYBRID → SAFE
```

when uncertainty exists.

---

## Required human gates

| Situation | Human gate |
|---|---|
| Product value/priority | Product owner / PM |
| Architecture/risk | Tech Lead |
| Execution readiness | Developer |
| Security/privacy | Security/Risk |
| Production critical change | Tech Lead + Developer |
| Destructive operation | Tech Lead + rollback/backup plan |

---

## Initiative folder phases

Application repositories should organize local initiative artifacts by phase:

```text
.cdad/initiatives/<initiative-id>/
  00-flow-index.md
  01-intake/
  02-assessment/
  03-design/
  04-execution/
  05-validation/
  06-governance/
  07-closure/
```

Official execution paths:

```text
04-execution/runtime-context.md
04-execution/ai-execution-brief.md
04-execution/relevant-files-list.md
05-validation/validation-report.md
06-governance/approval-record.md
```

---

## Human Interaction Rule

Human interaction happens primarily through chat or the active collaboration interface.

Humans should not be required to manually edit AI-CDAD artifacts for routine clarification.

When a human provides a clarification, decision or approval, the AI Execution Agent must record it in the appropriate artifact.

For SAFE mode, approvals must be recorded in `06-governance/approval-record.md` with approver, decision, timestamp and conditions.

If organizational policy requires approval outside chat, link the external approval evidence instead of copying sensitive content.

---

## AI-CDAD Status Update

Every meaningful step should return:

```markdown
## AI-CDAD Status Update

**Current Stage:**  
<stage>

**Created/Updated Artifacts:**  
- <file> — <location>

**Human Action Required:**  
- <who must do what>

**Blocking Issues:**  
- <if any>

**Next Step:**  
<next action>

**Confidence:**  
High | Medium | Low
```

---

## Language and Locale

The AI Execution Agent should infer the human-facing language from the user's request, existing artifacts and repository/team conventions.

If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default for questions, status updates, summaries, validation reports and human action requests.

Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.

If the language preference is unclear or conflicting, ask one short clarification question before creating human-facing artifacts.

---

## When the AI must stop

The AI Execution Agent must stop if it detects:

- production impact not approved
- API/schema/contract/event impact
- PII or sensitive data
- IAM/security change
- destructive operation
- low confidence
- missing required approval
- scope change
- conflicting initiative

---

## Minimum artifact set for execution

```text
00-flow-index.md
04-execution/runtime-context.md
04-execution/ai-execution-brief.md
04-execution/relevant-files-list.md
05-validation/validation-report.md
05-validation/pr-summary.md
```

For SAFE mode, also require:

```text
03-design/impact-analysis.md
03-design/lean-sdd.md
03-design/rollback-plan.md
06-governance/approval-record.md
05-validation/observability-checklist.md
```

---

## Using MCPs and Skills

During execution, the AI Execution Agent must check:

```text
integrations/mcp/mcp-registry.md
integrations/skills/skill-registry.md
```

Then it must follow the current:

```text
04-execution/ai-execution-brief.md
```

The brief must explicitly list:

- allowed MCPs
- forbidden MCPs
- required skills
- optional skills

If not listed, the agent should not use them.
