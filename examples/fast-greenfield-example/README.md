# FAST Greenfield Example

## Scenario

Create a new isolated internal utility with no production criticality and no external consumers.

## Entry Lane

Product or Engineering.

## Risk Mode

FAST.

## Expected Artifacts

- normalized-entry.md
- delivery-assessment.md
- runtime-context.md
- local-shaping-plan.md
- devin-execution-brief.md
- validation-report.md
- pr-summary.md

## Human Approvals

- Developer review.

## Devin Behavior

- Keep context minimal.
- Use developer core + FAST overlay.
- Generate tests and PR summary.
- Do not create heavy SDD unless risk changes.

## Stop Conditions

- external consumer discovered
- contract/schema impact discovered
- production risk discovered
