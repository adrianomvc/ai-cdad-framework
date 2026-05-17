# Skills

## Purpose

Skills define reusable capabilities that an AI Execution Agent can apply under AI-CDAD.

Skills are not tools.

A skill describes *how to perform a type of work*.

Examples:

- bugfix analysis
- incident triage
- brownfield impact analysis
- data quality validation
- observability review
- PR review

## Files

```text
integrations/skills/
  README.md
  skill-registry.md
  skill-template.md
  bugfix-skill.md
  incident-triage-skill.md
  brownfield-analysis-skill.md
  data-quality-skill.md
  observability-skill.md
  pr-review-skill.md
```

## How Skills Are Selected

Skills are selected based on:

- Entry Lane
- Risk Mode
- execution objective
- affected system
- required validation

The selected skills must be listed in:

```text
ai-execution-brief.md
```
