# Parallel Execution Policy

## Purpose

Enable speed through governed parallel execution without creating unsafe conflicts.

---

## Principle

Execute in parallel only when tasks are:

- independent
- scoped
- safe
- validatable

---

## Workstream Organizer

The Workstream Organizer creates:

```text
parallel-execution-plan.md
```

when parallel execution is applicable.

---

## Each Workstream Must Define

- goal
- owner
- allowed files
- blocked files
- dependencies
- expected outputs
- validation needs
- merge/integration order
- conflict risks

---

## Mode Behavior

### FAST

High parallelism allowed when files/components are independent.

Examples:

- implementation
- tests
- documentation
- validation draft

### HYBRID

Moderate parallelism.

Allowed:

- tests
- observability
- docs
- validation
- independent implementation components

### SAFE

Controlled parallelism.

Allowed:

- analysis
- tests
- validation
- observability
- documentation

Avoid parallel critical changes involving:

- contracts
- schemas
- migrations
- production paths
- IAM/security
- destructive operations
- critical business logic

---

## Conflict Rules

| Conflict | Action |
|---|---|
| same repo only | warning |
| same file | coordinate or sequential |
| same component | human alignment |
| contract/schema/critical path | hard stop |
| unclear ownership | stop and ask |

---

## Consolidation Rule

All workstreams must be consolidated before final validation.

No deploy before consolidated validation.
