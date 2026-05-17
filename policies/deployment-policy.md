# Deployment Policy

## Purpose

Define deployment behavior by Risk Mode.

---

## FAST

Allowed strategies:

- direct deploy
- simple canary, optional
- quick rollback

Required:

- validation report
- developer review
- PR/deploy record

---

## HYBRID

Recommended strategies:

- canary
- feature flags
- controlled rollout
- staged enablement

Required:

- rollout plan
- integration validation
- observability readiness

---

## SAFE

Recommended strategies:

- blue/green
- feature flags
- shadow mode
- parallel run
- staged migration
- controlled rollback window

Required:

- Tech Lead approval
- rollback plan
- deployment checklist
- contract validation when applicable
- regression validation
- post-deploy monitoring plan

---

## Production Rule

Any production deployment with unclear rollback or unclear owner is a hard stop.

---

## Post-deploy

Observe:

- errors
- latency
- logs
- metrics
- consumers
- business impact
- cost impact when relevant
