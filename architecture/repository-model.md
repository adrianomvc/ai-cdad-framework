# Repository Model

## 1. ai-cdad-framework

Contém architecture docs, playbooks, policies, templates, agent roles, prompts e examples.

## 2. Central Community Repository / Hub

Contém contextos, produtos, iniciativas active/archived e índices.

```text
contexts/
  domain/
  products/

initiatives/
  active/
  archived/

indexes/
  initiative-registry.md
  repo-impact-index.md
  component-impact-index.md
```

## 3. Application Repository

Contém execução local perto do código.

```text
src/
tests/
infra/

.cdad/
  initiatives/
    <initiative-id>/
      initiative-ref.md
      normalized-entry.md
      triage-report.md
      runtime-context.md
      local-shaping-plan.md
      parallel-execution-plan.md
      devin-execution-brief.md
      local-validation-report.md
      implementation-notes.md
      pr-summary.md
```

## Regra

- Artefatos globais/cross ficam no hub.
- Artefatos locais de execução ficam no repo da aplicação.
- Ambos devem ter links bidirecionais.
