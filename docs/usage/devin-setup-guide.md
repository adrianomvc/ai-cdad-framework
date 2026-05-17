# Devin Setup Guide for AI-CDAD

## Purpose

This guide explains how to use AI-CDAD with Devin.

AI-CDAD remains tool-agnostic, but Devin is a strong fit for:

- autonomous repository work
- long-running tasks
- multi-file changes
- PR preparation
- code investigation
- repeated delivery workflows

This guide is not a replacement for Devin's official setup process.

It explains how to apply AI-CDAD on top of Devin.

---

## High-Level Model

```text
AI-CDAD Framework Repo
  → stores the method, policies, prompts, templates and playbooks

Central Community Hub
  → stores global/product/domain context and initiative indexes

Application Repository
  → stores code and local `.cdad/` execution artifacts

Devin
  → runs as AI Execution Agent under AI-CDAD rules
```

---

## Step 1 — Prepare the AI-CDAD framework repository

Upload this package to a Git repository.

Recommended repository name:

```text
ai-cdad-framework
```

Do not add:

- secrets
- customer data
- production logs
- proprietary corporate code
- confidential architecture details

---

## Step 2 — Open the framework repository in Devin

Start with:

```text
prompts/devin/00-plan-before-files.md
```

Important:

```text
Do not allow Devin to create or change files before it returns a plan.
```

After reviewing the plan, continue with:

```text
prompts/devin/01-create-scaffold.md
prompts/devin/02-strengthen-rules.md
prompts/devin/03-architecture-review.md
prompts/devin/04-apply-corrections.md
prompts/devin/05-create-examples.md
prompts/devin/06-final-audit.md
```

---

## Step 3 — Configure Devin access to repositories

In Devin, connect the repository provider and grant access only to the repositories Devin needs.

Recommended access strategy:

| Repository | Access |
|---|---|
| AI-CDAD framework repo | required |
| central community hub | required for hub setup |
| application repo | required for actual implementation |
| unrelated repositories | avoid |

Principle:

```text
Give Devin the minimum repository access needed for the current task.
```

---

## Step 4 — Index repositories / use repository knowledge

If Devin supports repository indexing or generated repository knowledge, index the relevant repositories before execution.

Recommended order:

1. AI-CDAD framework repo
2. central community hub
3. application repo
4. related repos only if needed

Do not rely on indexed knowledge alone.

The execution session must still use:

```text
runtime-context.md
ai-execution-brief.md
relevant-files-list.md
```

---

## Step 5 — Setup Devin environment for an application repo

When applying AI-CDAD to an application repo, ask Devin to create only:

```text
.cdad/
  README.md
  framework-ref.md
  initiatives/
```

Use:

```text
prompts/devin/08-install-ai-cdad-in-application-repo.md
```

Do not let Devin copy the entire AI-CDAD framework into the application repo.

---

## Step 6 — Start an initiative

For each initiative, create:

```text
.cdad/initiatives/<initiative-id>/
  initiative-ref.md
  normalized-entry.md
  triage-report.md
  delivery-assessment.md
  runtime-context.md
  relevant-files-list.md
  local-shaping-plan.md
  ai-execution-brief.md
  validation-report.md
  pr-summary.md
```

If using Devin-specific naming, this may also include:

```text
devin-execution-brief.md
```

The preferred generic artifact remains:

```text
ai-execution-brief.md
```

---

## Step 7 — Required first response from Devin

For implementation tasks, Devin's first response must include:

1. understanding of the task
2. detected Entry Lane
3. proposed Risk Mode
4. files it wants to inspect
5. hard stops
6. missing context, if any
7. whether it is ready to proceed
8. AI-CDAD Status Update

---

## Step 8 — Hard stops for Devin

Devin must stop if it detects:

- production change
- API/data contract/schema/event change
- PII/sensitive data
- IAM/security permission change
- destructive operation
- relevant cost impact
- low confidence
- SAFE mode without approval
- conflict with another active initiative
- scope change
- missing required human approval

---

## Step 9 — Pull request behavior

If Devin creates a PR, it must include:

- PR summary
- risk mode
- files changed
- tests run
- validation evidence
- remaining risks
- rollback note, if applicable
- human review required

Artifact:

```text
pr-summary.md
```

---

## Step 10 — Recommended Devin prompts

### Framework setup

```text
prompts/devin/00-plan-before-files.md
```

### Central hub setup

```text
prompts/devin/07-setup-central-community-hub.md
```

### Application repo installation

```text
prompts/devin/08-install-ai-cdad-in-application-repo.md
```

### Tabletop validation

```text
prompts/devin/09-tabletop-local-bugfix.md
```

### Full framework coverage validation

```text
prompts/devin/10-validate-framework-coverage.md
```

---

## Devin Session Starter

Use this message when starting a Devin execution session:

```markdown
You are Devin acting as an AI Execution Agent under AI-CDAD.

Before making changes, read:

1. runtime-context.md
2. ai-execution-brief.md or devin-execution-brief.md
3. relevant-files-list.md
4. applicable playbook
5. applicable policy summary

Do not change files yet.

First return:
- understanding of the task
- Entry Lane
- Risk Mode
- files to inspect
- hard stops
- missing context
- implementation plan
- AI-CDAD Status Update
```

---

## What not to do

Do not ask Devin to:

- work without runtime context
- inspect the whole repository by default
- copy the entire framework into an app repo
- skip human gates
- self-approve risk
- ignore hard stops
- include secrets or sensitive logs in artifacts
- deploy production changes without approval
