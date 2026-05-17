# MCP Query Plan

## Purpose

Define what the AI Execution Agent is allowed to query before using any MCP.

## Initiative

- Initiative ID:
- Entry Lane:
- Risk Mode:
- Requested By:

## Objective

What questions must MCP access answer?

## MCPs Needed

| MCP | Access Level | Reason |
|---|---|---|

## Questions to Answer

1.
2.
3.

## Allowed Queries / Operations

List allowed searches, reads or actions.

## Forbidden Queries / Operations

List what must not be queried or invoked.

## Sensitive Data Risk

- PII risk:
- secrets risk:
- production data risk:
- internal confidential data risk:

## Human Approval Required?

Yes | No

If yes:

- required role:
- approval artifact:

## Expected Output

Usually:

```text
technical-context-pack.md
```

## Stop Conditions

Stop if:

- query requires forbidden access
- sensitive data appears
- write/destructive operation is needed
- risk mode should increase
- evidence contradicts current assumptions
