# AI Execution Brief

## Purpose

This is the generic execution contract for any AI Execution Agent.

Use this artifact for Devin, Claude Code, Codex, Cursor, Copilot, Amazon Q, StackSpot AI, ResolveAI or internal agents.

For Devin-specific compatibility, this may also be named:

```text
devin-execution-brief.md
```

## Initiative

- Initiative ID:
- Title:
- Entry Lane:
- Risk Mode:
- Current Stage:

## Execution Agent

- Tool:
- Mode:
- Human operator:
- Repository:
- Branch:

## Execution Goal

What the AI Execution Agent should accomplish.

## Required Inputs

- 00-flow-index.md
- 04-execution/runtime-context.md
- 03-design/local-shaping-plan.md
- 04-execution/relevant-files-list.md
- 02-assessment/delivery-assessment.md
- 06-governance/approval-record.md, if applicable
- 03-design/rollback-plan.md, if applicable

## Playbooks to Use

- developer/core.md
- developer/<fast|hybrid|safe>-overlay.md

If technical design is still active:

- techlead/core.md
- techlead/<fast|hybrid|safe>-overlay.md

## Approved Technical Direction

Summarize approved design or state FAST/local execution.

## Execution Scope

Allowed changes.

## Out of Scope

Forbidden changes.

## Allowed Files

List files the agent may inspect/change.

## Blocked Files / Areas

List files, folders or components the agent must not change.

## Hard Stops

List applicable hard stops.

## Stop Conditions

Stop if:

- context is insufficient
- scope is unclear
- architecture direction changes
- contract/schema/API/event is impacted
- sensitive data is found
- tests fail in a way that changes the plan
- required approval is missing

## Expected Outputs

- code changes
- tests
- PR/diff summary
- 05-validation/validation-report.md
- 05-validation/pr-summary.md
- 04-execution/implementation-notes.md

## Evidence Requirements

- test results:
- diff summary:
- validation evidence:
- links/references:

## Human Ownership

- Developer owner:
- Tech Lead approver:
- Security/Risk approver, if applicable:

## Communication Rules

- Infer the human-facing language from the user's request, existing artifacts and repository/team conventions.
- If the user communicates in Portuguese, use Portuguese Brazilian (`pt-BR`) by default for questions, status updates, summaries, validation reports and human action requests.
- Keep code, commands, filenames, logs, stack traces, API names and existing technical terms in their original language.
- If the language preference is unclear or conflicting, ask one short clarification question before creating human-facing artifacts.

## Final Instruction to AI Execution Agent

Do not improvise outside this brief.

If something does not fit the brief, stop and ask for the minimum required human decision.


---

## MCP Access

Allowed MCPs:

| MCP | Access Level | Purpose |
|---|---|---|

Forbidden MCPs:

| MCP | Reason |
|---|---|

MCP Query Plan:

```text
mcp-query-plan.md
```

MCP Output:

```text
technical-context-pack.md
```

Rules:

- MCP access is read-only by default.
- Write/action access requires approval.
- Destructive access is a hard stop.

---

## Skills to Use

Required Skills:

| Skill | Purpose |
|---|---|

Optional Skills:

| Skill | When to Use |
|---|---|

Skill Registry:

```text
integrations/skills/skill-registry.md
```
