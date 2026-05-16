# Roteiro de Execução no Devin — CDAD v1

Use estes prompts em sequência. A recomendação é NÃO pedir para o Devin fazer tudo de uma vez sem checkpoints.

---

## PASSO 0 — Contexto inicial para o Devin

Cole este prompt primeiro para alinhar a missão e pedir um plano antes de alterar arquivos.

```markdown
You are going to help me implement an enterprise delivery framework called CDAD — Context-Driven Adaptive Delivery.

Before changing files, read and understand this mission:

CDAD must support:
- Greenfield delivery
- Brownfield evolution
- Hybrid delivery
- Bugs
- Incidents
- Hotfixes
- Engineering work
- Compliance / security remediation

CDAD integrates with AWS AI-DLC workflows as the execution engine:
https://github.com/awslabs/aidlc-workflows

Important:
The PM Agent already exists outside this framework.
It runs in Microsoft Teams and is responsible for:
- product discovery
- requirement elicitation
- inception
- story creation
- acceptance criteria
- prioritization

Do not implement the PM Agent.

CDAD starts after a demand enters the framework, either from the PM Agent or from another entry lane such as bug, incident, tech debt, or compliance.

Core philosophy:
- CDAD governs
- AI-DLC executes
- Devin acts as a guided orchestrator
- humans retain ownership
- AI accelerates

Human role boundaries:
- PM defines WHAT, WHY, VALUE and PRIORITY
- Tech Lead owns architecture, technical strategy, risk, contracts, migration and rollout
- Developer owns execution, implementation, edge cases, tests and PR readiness
- Developer is an AI-Augmented Engineer, not a prompt operator
- AI does not own decisions, does not approve risk and does not bypass gates

Before creating files, produce an implementation plan with:
1. repository structure you will create
2. files you will create
3. assumptions
4. questions only if truly blocking
5. risks you see
6. how you will keep the framework lightweight and avoid token bloat

Do not create files yet.
```

### O que esperar
O Devin deve devolver um plano.  
Valide se ele entendeu:

- PM é externo
- CDAD governa
- AI-DLC executa
- Devin é guided orchestrator
- existem Entry Lanes e Risk Modes
- Dev mantém ownership

Se estiver correto, siga para o Passo 1.

---

## PASSO 1 — Criar o scaffold do framework

```markdown
Proceed with creating the CDAD v1 scaffold.

Create the full folder and file structure below, with useful initial content in every file. Do not leave empty placeholders.

Repository/folder to create:

cdad-framework/
  README.md

  architecture/
    cdad-overview.md
    operating-model.md
    ai-dlc-integration.md
    devin-guided-orchestrator.md
    entry-lanes-and-risk-modes.md
    repository-model.md
    context-management.md

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
    delivery-routing-policy.md
    governance-policy.md
    failure-handling-policy.md
    context-lifecycle-policy.md
    context-budget-policy.md
    context-minimization-policy.md
    mcp-consumption-policy.md
    human-approval-policy.md
    artifact-ownership-policy.md
    parallel-initiatives-policy.md
    parallel-execution-policy.md
    validation-policy.md
    deployment-policy.md
    definition-of-ready-policy.md
    definition-of-done-policy.md

  templates/
    intake/
      normalized-entry-template.md
      triage-report-template.md
      delivery-assessment-template.md

    design/
      mcp-query-plan-template.md
      technical-context-pack-template.md
      impact-analysis-template.md
      lean-sdd-template.md
      rollout-plan-template.md
      rollback-plan-template.md

    execution/
      runtime-context-template.md
      relevant-files-list-template.md
      context-reduction-plan-template.md
      shaping-plan-template.md
      parallel-execution-plan-template.md
      devin-execution-brief-template.md
      validation-report-template.md
      observability-checklist-template.md
      pr-summary-template.md
      implementation-notes-template.md

    governance/
      approval-record-template.md
      governance-hard-stop-template.md
      cdad-exception-report-template.md
      initiative-summary-template.md

    indexes/
      initiative-registry-template.md
      repo-impact-index-template.md
      component-impact-index-template.md

  agent-roles/
    cdad-intake-agent.md
    delivery-assessment-agent.md
    techlead-design-agent.md
    solution-shaping-agent.md
    workstream-organizer.md
    devin-guided-orchestrator.md
    validation-evaluator-agent.md
    knowledge-update-agent.md

  prompts/
    devin-master-prompt.md
    devin-execution-brief-prompt.md
    techlead-design-prompt.md
    shaping-prompt.md
    validation-prompt.md
    knowledge-update-prompt.md

  examples/
    fast-greenfield-example/
    hybrid-example/
    safe-brownfield-example/
    operational-incident-example/
    local-bugfix-example/

Important content requirements:
- Explain purpose, when to use, required inputs, expected outputs and human validation requirements in each file.
- Do not over-engineer executable software.
- This is an operational framework repository.
- Use clear Markdown.
- Make it enterprise-ready but lightweight enough for adoption.
```

### O que esperar
O Devin deve criar a estrutura.  
Confira se existem os 2 playbooks principais:

```text
playbooks/techlead/core.md
playbooks/developer/core.md
```

E os overlays:

```text
fast-overlay.md
hybrid-overlay.md
safe-overlay.md
```

---

## PASSO 2 — Reforçar regras centrais do framework

```markdown
Review the generated CDAD scaffold and strengthen it according to these non-negotiable rules:

1. CDAD governs; AI-DLC executes.
2. Devin is a guided orchestrator, not an unconstrained autonomous decision maker.
3. PM Agent is external and must not be implemented.
4. PM defines WHAT / WHY / VALUE / PRIORITY.
5. Tech Lead owns architectural direction and risk.
6. Developer owns execution and remains an AI-Augmented Engineer, not a prompt operator.
7. AI drafts artifacts; humans validate or approve when required.
8. FAST / HYBRID / SAFE must be clearly different.
9. Product / Operational / Engineering / Compliance lanes must be clearly different.
10. Brownfield / SAFE mode must be safe by default.
11. If relevant uncertainty exists, increase rigor: FAST → HYBRID → SAFE.
12. Do not load all context into Devin sessions.
13. runtime-context.md is the main runtime context.
14. Evidence references must preserve trust.
15. Hard stops must be explicit.
16. Stop conditions must be explicit.

Update files where necessary.
Return a summary of what you changed.
```

### O que esperar
O Devin deve melhorar o conteúdo, não apenas dizer “ok”.

---

## PASSO 3 — Revisão arquitetural obrigatória

```markdown
Now perform an architecture review of the generated CDAD framework.

Check for:

1. Missing policies
2. Duplicated concepts
3. Overly heavy process
4. Token bloat risks
5. Ambiguous human ownership
6. Unsafe brownfield assumptions
7. Missing references to AWS AI-DLC
8. Missing distinction between central community hub and application repository
9. Missing FAST/HYBRID/SAFE differences
10. Missing Devin stop conditions
11. Missing Definition of Ready
12. Missing Definition of Done
13. Missing context minimization
14. Missing parallel execution governance
15. Missing artifact ownership
16. Missing approval recording
17. Missing operational lane for bugs/incidents
18. Missing local application repository execution model

Return:
- Critical issues
- Important issues
- Nice-to-have issues
- Exact files that need changes

Do not change files yet.
```

### O que esperar
Ele deve listar problemas antes de corrigir.  
Se a lista fizer sentido, rode o Passo 4.

---

## PASSO 4 — Corrigir os problemas encontrados

```markdown
Apply the corrections from the architecture review.

Prioritize:
1. safety for brownfield
2. clarity for developers
3. clear Tech Lead / Developer ownership
4. token minimization
5. artifact location clarity
6. Devin stop conditions
7. AI-DLC integration clarity
8. lightweight FAST flow

After making changes, return:
- files changed
- why each change was made
- remaining risks
```

---

## PASSO 5 — Gerar exemplos de uso

```markdown
Create or improve the example flows under examples/.

Each example must include:
- scenario description
- entry lane
- risk mode
- expected artifacts
- human approvals
- Devin execution behavior
- validation gates
- status update example

Create these examples:

1. fast-greenfield-example
   Scenario: new isolated capability with low risk.

2. hybrid-example
   Scenario: new capability integrated with existing system.

3. safe-brownfield-example
   Scenario: change existing production capability with contract/schema risk.

4. operational-incident-example
   Scenario: production incident or critical bug.

5. local-bugfix-example
   Scenario: developer finds local bug in application repo and fixes it with Devin.

Make examples practical and concise.
```

---

## PASSO 6 — Criar o modelo de uso em repo da aplicação

```markdown
Create documentation explaining how an application repository should use CDAD.

Add or update a file:

architecture/repository-model.md

It must explain:

1. cdad-framework contains methods, playbooks, policies, templates and prompts.
2. central community repository contains global/cross initiative artifacts, indexes, product/domain context and governance.
3. application repository contains code and local CDAD execution artifacts under:

.cdad/initiatives/<initiative-id>/

Explain that:
- local execution artifacts stay close to code
- global/cross artifacts stay in the central hub
- both must link to each other
- local bug fixes start in the application repo but update hub indexes when needed

Include an example application repo structure:

repo-da-aplicacao/
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

---

## PASSO 7 — Validar redução de tokens

```markdown
Review the framework specifically for token bloat and context overloading.

Check whether each execution phase loads only what it needs.

Ensure the framework says:

- Do not load every artifact by default.
- Do not load full policies by default.
- Do not load archived initiatives by default.
- Do not load entire repositories.
- Use runtime-context.md as the primary context.
- Use summaries before full artifacts.
- Use relevant-files-list.md before reading many files.
- Generate context-reduction-plan.md if token budget is exceeded.

If any file contradicts this, fix it.

Return:
- files changed
- token bloat risks removed
- remaining recommendations
```

---

## PASSO 8 — Gerar checklist final de implantação

```markdown
Create a final implementation checklist called:

architecture/implementation-checklist.md

It must include:

1. Scaffold created
2. Policies created
3. Playbooks created
4. Templates created
5. Agent roles documented
6. Examples created
7. AI-DLC integration documented
8. Devin guided orchestrator documented
9. PM external assumption documented
10. Entry lanes documented
11. Risk modes documented
12. Human ownership documented
13. Context minimization documented
14. Hard stops documented
15. Definition of Ready documented
16. Definition of Done documented
17. Parallel execution documented
18. Hub/application repo model documented
19. Status UX documented
20. Ready for tabletop test

Mark each item as:
- Done
- Partial
- Missing

Then fix any Missing items.
```

---

# Quando considerar implantado

Considere o CDAD v1 implantado quando o Devin criar:

```text
cdad-framework/
  architecture/
  playbooks/
  policies/
  templates/
  agent-roles/
  prompts/
  examples/
```

E quando a checklist final mostrar tudo como `Done`.

---

# Próximo teste recomendado

Depois de criar o framework, rode uma simulação:

```markdown
Use the CDAD framework to simulate a local bugfix in an application repository.

Scenario:
A developer found a bug where the atendimento API returns 500 when protocol_id is null.

Run the CDAD flow:
- Entry Lane
- Risk Mode
- normalized-entry
- triage
- delivery assessment
- runtime-context
- shaping
- Devin execution brief
- validation
- status update

Do not implement code.
Only simulate the artifacts and decisions.
```
