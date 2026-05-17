# Application Repository Setup

## Goal

Apply AI-CDAD to an application repository without copying the entire framework.

---

## Create

```text
repo-da-aplicacao/
  .cdad/
    README.md
    framework-ref.md
    initiatives/
```

---

## Do Not Create

Do not copy these into the application repo:

- full `policies/`
- full `playbooks/`
- full `templates/`
- full `architecture/`
- all examples

The application repo should reference the framework.

---

## Local Initiative Structure

```text
.cdad/
  initiatives/
    <initiative-id>/
      initiative-ref.md
      normalized-entry.md
      triage-report.md
      runtime-context.md
      relevant-files-list.md
      local-shaping-plan.md
      parallel-execution-plan.md
      ai-execution-brief.md
      devin-execution-brief.md, if using Devin-specific compatibility
      validation-report.md
      implementation-notes.md
      pr-summary.md
```

---

## When to Update Central Hub

Update the hub when:

- initiative is HYBRID or SAFE
- more than one repo is involved
- production impact exists
- contract/schema/API/event is involved
- another initiative touches the same repo/component
- Tech Lead approval is required

---

## AI Execution Brief Naming

Generic artifact:

```text
ai-execution-brief.md
```

Devin-specific compatibility artifact:

```text
devin-execution-brief.md
```

Use `ai-execution-brief.md` when working with multiple tools.

Use `devin-execution-brief.md` when running specifically with Devin.

Both follow the same contract.
