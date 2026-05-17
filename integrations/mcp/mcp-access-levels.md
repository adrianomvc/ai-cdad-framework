# MCP Access Levels

## Purpose

Classify MCP operations by risk.

## Access Levels

### Read-only

Allowed to read or search information.

Examples:

- read docs
- search issues
- inspect PRs
- query logs/metrics
- inspect schemas

Default behavior:

- allowed when listed in the execution brief
- must avoid copying sensitive data
- must summarize and reference evidence

### Write

Allowed to create or update information.

Examples:

- create issue
- comment on PR
- update documentation
- create pull request
- update task status

Default behavior:

- requires explicit approval unless pre-approved in execution brief

### Destructive

Allowed to delete, disable, deploy, apply infrastructure or modify sensitive operations.

Examples:

- delete resources
- change IAM
- deploy production
- apply terraform
- modify production database
- rotate secrets
- stop services

Default behavior:

- hard stop
- requires explicit human approval
- requires rollback/backup plan
- usually SAFE mode

## Hard Stop Operations

Always stop before:

- production deploy
- IAM/security change
- destructive operation
- cost-impacting cloud action
- access to sensitive secrets
- copying sensitive customer data
