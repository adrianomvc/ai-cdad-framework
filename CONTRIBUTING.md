# Contributing to AI-CDAD

## Principles

When evolving this framework:

1. Preserve human ownership.
2. Preserve brownfield safety.
3. Preserve context minimization.
4. Avoid unnecessary process weight.
5. Keep FAST lightweight.
6. Keep SAFE safe.
7. Do not duplicate framework content inside application repos.

## Change Types

### Policy changes

Require review because they affect governance.

### Template changes

Should preserve required fields for evidence, owner, gates and stop conditions.

### Playbook changes

Must keep Tech Lead and Developer ownership boundaries clear.

### Prompt changes

Must not contradict README.md, architecture/source-of-truth.md or decisions-log.md.

## Compatibility

Avoid breaking existing artifact names unless there is a strong reason.

## Review Checklist

Before merging:

- Does this increase token bloat?
- Does this weaken hard stops?
- Does this confuse human ownership?
- Does this make FAST too heavy?
- Does this make SAFE too loose?
- Does this contradict source of truth?
