# Repository Model

AI-CDAD uses a three-layer repository model.

The goal is to avoid two opposite problems:

1. putting everything in the central hub, far from execution;
2. duplicating the whole framework inside every application repository.

---

## Layer 1 — `ai-cdad-framework`

Purpose:

```text
How we work.
```

This repository contains the reusable method.

Recommended structure:

```text
ai-cdad-framework/
  README.md

  architecture/
    ai-cdad-overview.md
    operating-model.md
    ai-dlc-integration.md
    devin-guided-orchestrator.md
    entry-lanes-and-risk-modes.md
    repository-model.md
    context-management.md
    source-of-truth.md
    implementation-checklist.md

  playbooks/
    techlead/
      core.md
      fast-overlay.md
      hybrid-overlay.md
      safe-overlay.md

    developer/
      core.md
      fast-overlay.md
      hybrid-overlay.md
      safe-overlay.md

  policies/
  templates/
  agent-roles/
  prompts/
  examples/
  docs/
```

What belongs here:

- framework documentation
- reusable playbooks
- reusable policies
- reusable templates
- Devin prompts
- agent role definitions
- example flows
- adoption guidance

What does **not** belong here:

- application-specific execution artifacts
- real production secrets
- private business data
- live incident evidence from work systems
- internal confidential implementation details unless approved

---

## Layer 2 — Central Community Repository / Hub

Purpose:

```text
Official memory, cross-repo governance and portfolio visibility.
```

Example names:

```text
repo-central-ai-delivery-community
central-community-repo
```

Recommended structure:

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
      customer-service-platform/
        product-overview.md
        architecture-current-state.md
        integrations.md
        contracts.md
        known-risks.md
        context-index.md

  initiatives/
    active/
      <initiative-id>/
        initiative-overview.md
        original-input.md
        normalized-entry.md
        delivery-assessment.md
        global-impact-analysis.md
        global-lean-sdd.md
        global-shaping-plan.md
        rollout-strategy.md
        approval-record.md
        consolidated-validation-report.md
        consolidated-observability-summary.md
        initiative-repos.md

    archived/
      <initiative-id>/
        initiative-summary.md
        archived-artifacts/

  indexes/
    initiative-registry.md
    repo-impact-index.md
    component-impact-index.md
```

What belongs here:

- community/domain context
- product context
- product architecture current state
- product contracts summary
- cross-repo initiatives
- global decisions
- initiative registry
- repo impact index
- component impact index
- archived initiative summaries

What does **not** belong here:

- local implementation details that only matter to one application repo
- huge code dumps
- full logs unless needed as evidence
- entire archived histories loaded as active context

---

## Layer 3 — Application Repository

Purpose:

```text
Local execution close to the code.
```

Recommended structure:

```text
repo-da-aplicacao/
  src/
  tests/
  infra/

  .cdad/
    README.md
    framework-ref.md

    initiatives/
      <initiative-id>/
        initiative-ref.md
        normalized-entry.md
        triage-report.md
        runtime-context.md
        relevant-files-list.md
        local-technical-context.md
        local-impact-analysis.md
        local-design.md
        local-shaping-plan.md
        parallel-execution-plan.md
        ai-execution-brief.md
        devin-execution-brief.md
        validation-report.md
        local-observability-checklist.md
        implementation-notes.md
        pr-summary.md
        cdad-exception-report.md
```

What belongs here:

- runtime-context.md
- ai-execution-brief.md
- devin-execution-brief.md, when using Devin-specific compatibility
- local shaping plan
- relevant files list
- validation report
- implementation notes
- PR summary
- local evidence
- local exception report

What does **not** belong here:

- full AI-CDAD framework copy
- all global product context
- all policies duplicated manually
- unrelated archived initiatives

---

## Linking Strategy

### Application repo → Hub

Each local initiative must include:

```text
.cdad/initiatives/<initiative-id>/initiative-ref.md
```

Example:

```markdown
# Initiative Reference

- Initiative ID: 2026-045-fix-null-protocol-id
- Entry Lane: Operational
- Risk Mode: FAST
- Central Hub Initiative: <hub-link>/initiatives/active/2026-045-fix-null-protocol-id
- Application Repo: customer-service-api
- Local Path: .cdad/initiatives/2026-045-fix-null-protocol-id
- Developer Owner:
- Tech Lead:
```

### Hub → Application repos

Each hub initiative must include:

```text
initiative-repos.md
```

Example:

```markdown
# Initiative Repositories

| Repo | Local CDAD Path | Owner | Status |
|---|---|---|---|
| customer-service-api | `.cdad/initiatives/2026-045-fix-null-protocol-id` | Squad A | Execution |
```

---

## Artifact Location Rule

```text
Framework method
→ ai-cdad-framework

Global/cross context
→ central community repository

Local execution
→ application repository
```

---

## Bug Example

For a local bug in `customer-service-api`:

```text
repo-customer-service-api/
  .cdad/
    initiatives/
      2026-045-fix-null-protocol-id/
        initiative-ref.md
        normalized-entry.md
        triage-report.md
        runtime-context.md
        relevant-files-list.md
        local-shaping-plan.md
        ai-execution-brief.md
        devin-execution-brief.md
        validation-report.md
        implementation-notes.md
        pr-summary.md
```

The central hub should be updated only if needed for:

- index registration
- cross-repo conflict
- production impact
- contract/schema impact
- SAFE/HYBRID coordination

---

## Anti-duplication Rule

Do not copy the entire framework into every application repo.

Application repos should reference the framework using:

```text
.cdad/framework-ref.md
```

Example:

```markdown
# AI-CDAD Framework Reference

- Framework repo: <link-to-ai-cdad-framework>
- Central hub: <link-to-central-community-repo>
- Community: AI Delivery Community
```
