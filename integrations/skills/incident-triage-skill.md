# Incident Triage Skill

## Purpose

Analyze incidents, organize evidence and guide safe mitigation.

## When to Use

- Entry Lane: Operational
- Risk Mode: SAFE by default
- Typical triggers: production incident, outage, degraded service, alert storm

## Required Inputs

- normalized-entry.md
- triage-report.md
- runtime-context.md
- mcp-query-plan.md, if observability MCP is needed

## Steps

1. Clarify severity.
2. Identify affected users/systems.
3. Gather evidence safely.
4. Identify mitigation options.
5. Identify rollback/workaround.
6. Escalate required approvals.
7. Generate validation and observability notes.

## Stop Conditions

Stop if:

- mitigation is destructive
- production deploy is required without approval
- sensitive data appears
- rollback is unclear
