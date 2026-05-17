# Prompt 09 — Tabletop Local Bugfix

Use the AI-CDAD framework to simulate a local bugfix in an application repository.

Do not implement code.

Scenario:

A developer found a bug where `customer-service-api` returns HTTP 500 when `correlation_id` is null.

Run the AI-CDAD flow and generate simulated artifacts:

- normalized-entry.md
- triage-report.md
- delivery-assessment.md
- runtime-context.md
- relevant-files-list.md
- local-shaping-plan.md
- devin-execution-brief.md
- validation-report.md
- AI-CDAD Status Update

Validate:

- Entry Lane
- Risk Mode
- human gates
- stop conditions
- token minimization
- local repo vs central hub usage

Return issues found in the framework before changing framework files.
