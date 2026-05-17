# Prompt 07 — Setup Central Community Hub

You are applying AI-CDAD to a central community/domain repository.

Do not copy the full AI-CDAD framework into this repo.

Create only the hub structure:

```text
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

Rules:

- Use AI-CDAD framework as reference.
- Do not store secrets or customer data.
- Create useful starter content, not empty placeholders.
- Keep hub focused on global/cross context.
- Do not create local execution artifacts here unless the initiative is cross-repo or global.
