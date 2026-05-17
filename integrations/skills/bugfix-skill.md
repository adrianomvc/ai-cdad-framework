# Bugfix Skill

## Purpose

Analyze, fix and validate bugs under AI-CDAD.

## When to Use

- Entry Lane: Operational
- Risk Modes: FAST/HYBRID/SAFE
- Typical triggers: bug, exception, wrong behavior, failing test

## Required Inputs

- normalized-entry.md
- triage-report.md, if available
- delivery-assessment.md
- runtime-context.md
- ai-execution-brief.md
- relevant-files-list.md

## Steps

1. Confirm the observed behavior.
2. Identify affected component.
3. Inspect only relevant files.
4. Reproduce or reason from evidence.
5. Propose fix.
6. Add or update tests.
7. Run validation.
8. Generate validation-report.md.
9. Generate pr-summary.md.

## Stop Conditions

Stop if:

- production impact is higher than expected
- contract/schema/API/event changes are required
- PII or secrets appear
- scope changes
- confidence is low
