# Operational Incident Example

## Scenario

A production pipeline is failing and consumers are not receiving updated atendimento events.

## Entry Lane

Operational.

## Risk Mode

SAFE by default.

## Expected Artifacts

- normalized-entry.md
- triage-report.md
- delivery-assessment.md
- runtime-context.md
- rollback-plan.md
- devin-execution-brief.md
- validation-report.md
- observability-checklist.md
- approval-record.md
- initiative-summary.md

## Human Approvals

- Dev on-call validates triage.
- Tech Lead approves mitigation and rollback.
- Security/Risk if sensitive data or regulatory impact exists.

## Devin Behavior

- Organize incident context.
- Identify affected components.
- Generate mitigation plan.
- Prepare safe execution brief.
- Support fix or rollback.
- Capture validation evidence.
- Generate post-incident summary.

## Stop Conditions

- destructive operation without approval
- production deploy without rollback
- unknown consumer impact
- contract/schema uncertainty
