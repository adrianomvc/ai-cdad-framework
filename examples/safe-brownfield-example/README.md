# SAFE Brownfield Example

## Scenario

Change an existing production atendimento contract used by multiple downstream consumers.

## Entry Lane

Product or Engineering.

## Risk Mode

SAFE.

## Expected Artifacts

- normalized-entry.md
- delivery-assessment.md
- mcp-query-plan.md
- technical-context-pack.md
- global-impact-analysis.md
- global-lean-sdd.md
- rollout-strategy.md
- rollback-plan.md
- approval-record.md
- runtime-context.md
- devin-execution-brief.md
- validation-report.md
- consolidated-observability-summary.md
- initiative-summary.md

## Human Approvals

- Tech Lead approval mandatory.
- Developer feasibility mandatory.
- Security/Risk if PII or compliance involved.

## Devin Behavior

- Do not execute code before Tech Lead design approval.
- Use MCP in controlled mode.
- Generate technical-context-pack.
- Generate evidence-based runtime-context.
- Execute only scoped changes.
- Validate contracts and regression.
