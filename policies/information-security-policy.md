# Information Security Policy

## Purpose

Protect sensitive information when using AI-CDAD, especially when developing the framework in a personal GitHub repository before adopting it in a corporate environment.

---

## Core Rule

Do not put confidential corporate information in a personal repository.

---

## Never Commit to Personal Repos

- customer data
- PII
- production logs containing sensitive data
- secrets
- tokens
- passwords
- certificates
- private keys
- internal source code from work
- proprietary architecture details
- non-public contracts or schemas
- internal incident evidence
- names of confidential systems if not approved
- screenshots with sensitive information

---

## Allowed in Personal Repo

- generic framework documentation
- anonymized examples
- synthetic scenarios
- generic architecture patterns
- generic prompts
- non-confidential templates
- non-confidential Mermaid diagrams
- non-confidential presentations

---

## Corporate Adoption

When moving AI-CDAD to a work environment:

1. create an internal repository
2. remove personal assumptions
3. adapt naming and policies
4. add internal security rules
5. connect approved MCP sources only
6. keep secrets out of artifacts
7. anonymize logs before using them as evidence

---

## Logs and Evidence

Before adding logs to AI-CDAD artifacts:

- remove customer identifiers
- remove CPF/CNPJ/account numbers
- remove tokens and secrets
- remove internal URLs if required
- reduce stack traces to relevant snippets
- link to approved systems instead of copying sensitive content

---

## Devin Behavior

If Devin detects sensitive data, it must:

1. stop
2. warn the user
3. avoid committing the sensitive data
4. suggest redaction/anonymization
5. continue only with safe evidence

---

## Hard Stop

Sensitive data in a personal repo is a hard stop.
