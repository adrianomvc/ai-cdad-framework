# Parallel Initiatives Policy

## Purpose

Control multiple initiatives impacting the same repository, component or contract.

---

## Required Indexes

The central hub must maintain:

```text
indexes/
  initiative-registry.md
  repo-impact-index.md
  component-impact-index.md
```

---

## Conflict Levels

| Conflict | Action |
|---|---|
| same repo | warning |
| same component/module | coordination required |
| same file | coordinate or sequential execution |
| same contract/schema/API/event | hard stop |
| same critical path | hard stop |
| unclear ownership | stop and ask |

---

## Initiative Impact Declaration

Each initiative should declare:

- impacted repositories
- impacted components
- impacted contracts/schemas
- owners
- risk mode
- current stage

Example:

```yaml
impacted_repos:
  - repo: customer-service-api
    areas:
      - CustomerCorrelationService
      - protocol handling
    risk: medium
```

---

## Required Behavior

Before execution, Devin must check:

- initiative registry
- repo impact index
- component impact index

If there is conflict, Devin must report it in the AI-CDAD Status Update.

If hard stop conflict exists, execution must stop until Tech Lead alignment.
