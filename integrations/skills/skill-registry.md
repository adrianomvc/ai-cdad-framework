# Skill Registry

## Purpose

List reusable skills available to AI-CDAD.

| Skill | Purpose | Entry Lane | Risk Modes | Owner |
|---|---|---|---|---|
| Bugfix Skill | Analyze, fix and validate bugs | Operational | FAST/HYBRID/SAFE | Developer |
| Incident Triage Skill | Analyze incidents and guide mitigation | Operational | SAFE | Tech Lead / SRE |
| Brownfield Analysis Skill | Assess impact in existing systems | Product/Engineering | HYBRID/SAFE | Tech Lead |
| Data Quality Skill | Validate data quality rules and evidence | Product/Engineering | HYBRID/SAFE | Data Engineer |
| Observability Skill | Validate logs, metrics, traces and alerts | Operational/Engineering | HYBRID/SAFE | Developer/SRE |
| PR Review Skill | Review code against AI-CDAD constraints | Any | FAST/HYBRID/SAFE | Developer |

## How to Add a New Skill

Create:

```text
integrations/skills/<skill-name>.md
```

Use:

```text
integrations/skills/skill-template.md
```

Then register the skill here.
