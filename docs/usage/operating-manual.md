# AI-CDAD Operating Manual

## Daily usage

For each demand:

1. Identify Entry Lane.
2. Create or update `normalized-entry.md`.
3. Run triage if needed.
4. Create `delivery-assessment.md`.
5. Classify risk mode: FAST, HYBRID or SAFE.
6. Create `runtime-context.md`.
7. Create `ai-execution-brief.md`.
8. Run AI Execution Agent.
9. Validate.
10. Review.
11. Deploy or resolve.
12. Observe and archive.

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
runtime-context.md
ai-execution-brief.md
relevant-files-list.md
validation-report.md
pr-summary.md
```

For SAFE mode, also require:

```text
impact-analysis.md
lean-sdd.md
rollback-plan.md
approval-record.md
observability-checklist.md
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
ai-execution-brief.md
```

The brief must explicitly list:

- allowed MCPs
- forbidden MCPs
- required skills
- optional skills

If not listed, the agent should not use them.
