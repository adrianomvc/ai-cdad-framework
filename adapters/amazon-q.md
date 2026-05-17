# Amazon Q Developer Adapter

## Purpose

Use Amazon Q Developer as an AI Execution Agent under AI-CDAD.

## Best For

AWS architecture assistance, infrastructure guidance, code assistance and cloud troubleshooting.

## Required Inputs

- runtime-context.md
- ai-execution-brief.md
- relevant-files-list.md
- applicable playbooks
- applicable policies

## Rules

- Do not execute before the required human gate.
- Do not bypass hard stops.
- Do not approve own work.
- Do not change blocked files.
- Stop if scope changes.
- Stop if sensitive data is found.
- Produce AI-CDAD Status Updates.

## Evidence

Return:

- files inspected
- files changed
- commands run, if applicable
- tests run
- validation result
- remaining risks
