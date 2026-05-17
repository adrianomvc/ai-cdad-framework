# Local Bugfix Example

## Scenario

A developer found a bug where `customer-service-api` returns HTTP 500 when `correlation_id` is null.

## Human Input

```text
Temos um bug na aplicação customer-service-api.
Repo principal: customer-service-api.
Possível repo relacionado: customer-service-pipeline.
Erro: HTTP 500 quando correlation_id vem nulo.
Evidência: NullPointerException em CustomerCorrelationService.java.
Impacto: homologação; produção ainda não confirmada.
```

## Entry Lane

Operational.

## Triage

Required.

Questions:

- Já ocorreu em produção?
- O repo principal é `customer-service-api`?
- Existe contrato/API/schema que não pode mudar?

## Risk Mode

Initial recommendation:

```text
FAST
```

If production impact or contract/schema impact is confirmed:

```text
SAFE
```

## Expected Local Artifacts

```text
.cdad/initiatives/2026-045-fix-null-protocol-id/
  initiative-ref.md
  normalized-entry.md
  triage-report.md
  runtime-context.md
  relevant-files-list.md
  local-shaping-plan.md
  devin-execution-brief.md
  local-validation-report.md
  implementation-notes.md
  pr-summary.md
```

## Human Approvals

- Developer validates execution readiness.
- Tech Lead only if contract/schema/production impact appears.

## Devin Behavior

1. Create normalized-entry.md.
2. Create triage-report.md.
3. Inspect local repo context.
4. Generate relevant-files-list.md.
5. Check central hub indexes lightly.
6. Generate runtime-context.md.
7. Generate devin-execution-brief.md.
8. Wait for developer feasibility confirmation.
9. Implement fix and tests.
10. Generate validation-report and PR summary.

## Stop Conditions

Stop if:

- contract/schema is impacted
- production criticality is confirmed
- PII is involved
- scope becomes unclear
- tests indicate wider regression

## AI-CDAD Status Update Example

```markdown
## AI-CDAD Status Update

**Current Stage:**  
Developer Feasibility Gate

**Created/Updated Artifacts:**  
- `runtime-context.md` — `.cdad/initiatives/2026-045-fix-null-protocol-id/`
- `devin-execution-brief.md` — `.cdad/initiatives/2026-045-fix-null-protocol-id/`

**Human Action Required:**  
Developer must confirm scope and allowed files.

**Blocking Issues:**  
Production impact not confirmed.

**Next Step:**  
After developer validation, start Devin execution.

**Confidence:**  
Medium
```
