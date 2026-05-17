# GitHub Copilot Adapter

## Purpose

Use GitHub Copilot as an AI Execution Agent under AI-CDAD.

## Best For

pair programming, small scoped changes, inline code generation, tests and documentation snippets.

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
