# Context Minimization Policy

## Purpose

Reduce token usage without reducing trust or safety.

---

## Core Principle

```text
Repositories store rich memory.
AI execution sessions use minimal runtime context.
```

The session must load the smallest sufficient context for the current phase.

---

## Primary Runtime Artifact

The main runtime artifact is:

```text
04-execution/runtime-context.md
```

It must contain:

- goal
- scope
- out of scope
- risk mode
- required gates
- critical constraints
- evidence references
- stop conditions
- human owners
- validation requirements
- relevant files

---

## Must Always Remain in Context

Never remove these items to save tokens:

- risk mode
- scope
- out of scope
- hard stops
- required gates
- stop conditions
- human owner
- validation requirements
- evidence references

---

## Load Strategy

### Must Load

- `00-flow-index.md`
- `04-execution/runtime-context.md`
- `04-execution/ai-execution-brief.md`
- `03-design/local-shaping-plan.md`, if execution
- `runtime-policy-summary.md`, if available
- relevant files identified in `04-execution/relevant-files-list.md`

### Load If Needed

- full `lean-sdd.md`
- full `impact-analysis.md`
- full `technical-context-pack.md`
- rollback plan
- approval record
- historical initiative summaries

### Never Load By Default

- full repository
- archived initiatives
- all policies
- all playbooks
- full product documentation
- unrelated logs
- unrelated code directories

---

## Summaries First

For large artifacts, use summaries first:

- `technical-context-summary.md`
- `impact-analysis-summary.md`
- `lean-sdd-summary.md`
- `rollback-summary.md`

Open full artifacts only if required by risk, ambiguity, hard stop or human request.

---

## Relevant Files First

Before reading many code files, the AI Execution Agent must create or update:

```text
04-execution/relevant-files-list.md
```

It must classify files as:

- Must Inspect
- Maybe Inspect
- Do Not Inspect Yet

---

## Token Budgets

| Mode | Target | Maximum |
|---|---:|---:|
| FAST | 20k | 40k |
| HYBRID | 50k | 100k |
| SAFE | 100k | 180k |

If estimated context exceeds the maximum, the AI Execution Agent must create:

```text
context-reduction-plan.md
```

before continuing.

---

## Context Reduction Plan Must Include

- current estimated context
- reduction actions
- artifacts replaced by summaries
- files excluded
- risks of reduction
- remaining evidence references
- approval needed, if any

---

## Safety Rule

Reducing context must never remove safety-relevant information.

If minimization creates uncertainty, the AI Execution Agent must stop and ask for the minimum missing context.
