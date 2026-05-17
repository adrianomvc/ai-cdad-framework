# Devin Execution Brief

## Purpose

This is the execution contract for Devin.

Devin must not execute outside this brief.

---

## Initiative

- Initiative ID:
- Title:
- Entry Lane:
- Risk Mode:
- Current Stage:

---

## Execution Goal

What Devin should accomplish in this run.

---

## Required Inputs

- runtime-context.md
- local-shaping-plan.md
- relevant-files-list.md
- delivery-assessment.md
- approval-record.md, if applicable
- rollback-plan.md, if applicable

---

## Playbooks to Use

- developer/core.md
- developer/<fast|hybrid|safe>-overlay.md

If technical design is still active:

- techlead/core.md
- techlead/<fast|hybrid|safe>-overlay.md

---

## Approved Technical Direction

Summarize approved design or state FAST/local execution.

---

## Execution Scope

Allowed changes.

---

## Out of Scope

Forbidden changes.

---

## Allowed Files

List files Devin may change.

---

## Blocked Files / Areas

List files, folders or components Devin must not change.

---

## Hard Stops

List hard stops applicable to this execution.

---

## Stop Conditions

Stop if:

- context is insufficient
- scope is unclear
- architecture direction changes
- contract/schema is impacted
- sensitive data is found
- tests fail in a way that changes the plan
- required approval is missing

---

## Expected Outputs

- code changes
- tests
- PR draft
- validation-report.md
- pr-summary.md
- implementation-notes.md

---

## Human Ownership

- Developer owner:
- Tech Lead approver:
- Security/Risk approver, if applicable:

---

## Communication Rules

- Infer the human-facing language from the user's request, existing artifacts and repository/team conventions.
- If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default for questions, status updates, summaries, validation reports and human action requests.
- Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.
- If the language preference is unclear or conflicting, ask one short clarification question before creating human-facing artifacts.

---

## Final Instruction to Devin

Do not improvise outside this brief.

If something does not fit the brief, stop and ask for the minimum required human decision.

---

## Generic Compatibility

This is a Devin-specific version of the generic:

```text
ai-execution-brief.md
```

Both artifacts must follow the same execution contract.

If AI-CDAD is used with another AI tool, prefer:

```text
ai-execution-brief.md
```


---

## MCP Access

Use the generic AI execution brief rules for MCP access.

Reference:

```text
templates/execution/ai-execution-brief-template.md
integrations/mcp/mcp-registry.md
```

---

## Skills to Use

List required skills from:

```text
integrations/skills/skill-registry.md
```
