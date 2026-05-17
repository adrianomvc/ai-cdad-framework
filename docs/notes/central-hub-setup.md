# Central Community Hub Setup

## Goal

Create the central repository for community/domain context, cross-repo initiatives and governance indexes.

---

## Recommended Structure

```text
central-community-repo/
  README.md

  ai-cdad/
    framework-ref.md
    adoption-guide.md
    community-working-agreement.md

  contexts/
    domain/
      glossary.md
      capability-map.md
      business-rules.md
      constraints.md

    products/
      <product-name>/
        product-overview.md
        architecture-current-state.md
        integrations.md
        contracts.md
        known-risks.md
        context-index.md

  initiatives/
    active/
    archived/

  indexes/
    initiative-registry.md
    repo-impact-index.md
    component-impact-index.md
```

---

## Hub Responsibilities

- official domain/product memory
- cross-repo initiative coordination
- initiative registry
- repo/component impact tracking
- global approvals
- archived summaries

---

## Hub Must Not Store

- secrets
- raw customer data
- unnecessary logs
- unrelated code dumps
- full application repo copies
