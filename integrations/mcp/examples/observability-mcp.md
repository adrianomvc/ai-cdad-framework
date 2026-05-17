# Observability MCP Example

## Purpose

Use observability tools to inspect logs, metrics, traces and alerts.

## Access Level

read-only

## Allowed Uses

- inspect error rates
- inspect latency
- inspect traces
- inspect alert history
- summarize relevant logs

## Forbidden Uses

- copy raw sensitive logs
- expose customer identifiers
- change alerts without approval
- silence alerts without approval

## Required Approval

Required if logs contain sensitive data or if alert configuration will be changed.

## Stop Conditions

Stop if PII, secrets or customer data appear in logs.
