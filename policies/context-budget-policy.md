# Context Budget Policy

## Purpose

Define target and maximum token budgets by Risk Mode.

This policy protects the framework from hypercontextualization.

---

## Token Budgets

| Mode | Target | Maximum |
|---|---:|---:|
| FAST | 20k tokens | 40k tokens |
| HYBRID | 50k tokens | 100k tokens |
| SAFE | 100k tokens | 180k tokens |

---

## Budget by Phase

### Intake

Load only:

- original input
- normalized-entry template
- minimal routing policy

### Delivery Assessment

Load only:

- normalized-entry.md
- triage-report.md if applicable
- routing policy summary
- known repo/component indexes if needed

### Tech Lead Design

Load:

- delivery-assessment.md
- mcp-query-plan.md
- technical-context-pack.md or summary
- Tech Lead playbook core + overlay for current mode

### Execution

Load:

- runtime-context.md
- devin-execution-brief.md
- local-shaping-plan.md
- relevant-files-list.md
- Developer playbook core + overlay for current mode
- relevant source files only

### Validation

Load:

- diff/PR
- validation requirements
- validation-report template
- test output summaries
- evidence references

---

## If Budget Is Exceeded

Before continuing, Devin must generate:

```text
context-reduction-plan.md
```

The plan must explain:

- current context estimate
- what will be summarized
- what will be excluded
- what evidence remains referenced
- remaining risks

---

## Safety Constraint

Budget reduction must never remove:

- risk mode
- scope
- out of scope
- hard stops
- required gates
- stop conditions
- human owner
- validation requirements
- evidence references
