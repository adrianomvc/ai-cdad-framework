# Context Lifecycle Policy

## Purpose

Define how context is created, used, summarized, archived and retrieved.

---

## Context Layers

| Layer | Name | Purpose |
|---|---|---|
| L0 | Framework Context | AI-CDAD method, policies, templates and playbooks |
| L1 | Domain Context | glossary, capability map, business rules |
| L2 | Product Context | product overview, architecture, integrations, contracts |
| L3 | Initiative Context | active initiative artifacts and decisions |
| L4 | Repo Execution Context | local execution artifacts near code |

---

## Hot Context

Hot context is actively relevant to the current work.

Examples:

- current initiative
- current repo
- current runtime-context.md
- current execution brief
- current validation artifacts

Hot context can be loaded when needed.

---

## Cold Context

Cold context is historical or archived.

Examples:

- archived initiatives
- old SDDs
- postmortems
- old decisions
- deprecated assumptions

Cold context must not be loaded by default.

---

## Archive Rule

When an initiative closes:

1. generate `initiative-summary.md`
2. keep full artifacts in archive if needed
3. summarize reusable knowledge
4. mark deprecated/non-reusable knowledge
5. move initiative from active to archived

---

## Retrieval Rule

Archived context may be retrieved only when:

- a similar issue recurs
- a human asks for history
- an evidence reference points to it
- a risk decision requires historical context

---

## Staleness Rule

If context may be stale, Devin must mark it as uncertain and ask for confirmation or fresh evidence.
