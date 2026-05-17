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

- runtime-context.md
- local-shaping-plan.md
- relevant-files-list.md
- delivery-assessment.md
- approval-record.md, if applicable
- rollback-plan.md, if applicable

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
- validation-report.md
- pr-summary.md
- implementation-notes.md

## Evidence Requirements

- test results:
- diff summary:
- validation evidence:
- links/references:

## Human Ownership

- Developer owner:
- Tech Lead approver:
- Security/Risk approver, if applicable:

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
