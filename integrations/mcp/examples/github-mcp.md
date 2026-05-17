# GitHub MCP Example

## Purpose

Use GitHub MCP to inspect repositories, branches, issues, PRs and code metadata.

## Access Level

read/write

## Default Mode

read-only

## Allowed Uses

- inspect repository structure
- inspect PRs
- inspect issues
- search files
- compare branches
- create PR comments when approved
- create PRs when approved

## Forbidden Uses

- force push
- delete branches
- merge without approval
- change protected branch rules
- expose secrets
- change repository permissions

## Required Approval

Write operations require Developer approval.

Repository administration requires Tech Lead approval.

## Stop Conditions

Stop if the operation affects protected branches, repository permissions or production release flow.
