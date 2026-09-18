---
name: technical-documentation
description: Create or update engineering documentation grounded in the actual system. Use for READMEs, architecture notes, ADRs, API guides, runbooks, migration guides, and developer onboarding.
---

# Technical Documentation

Write for a named audience and task. Inspect the implementation and commands; do not document an imagined system.

## Document types

- README: purpose, prerequisites, setup, common workflows, verification, troubleshooting.
- ADR: context, decision drivers, considered options, decision, consequences, status.
- Runbook: trigger, impact, prerequisites, diagnosis, safe mitigation, verification, rollback, escalation.
- API guide: authentication, examples, errors, pagination/idempotency, compatibility, limits.
- Migration guide: prerequisites, staged procedure, compatibility window, data checks, rollback limits.

Use progressive disclosure: quick path first, details and rationale later. Prefer executable examples with safe placeholders. Mark destructive commands, required permissions, environment assumptions, and expected output. Keep a single source of truth and link to it instead of copying volatile details.

Verify commands where safe, links, filenames, configuration names, and consistency with the current code. State unverified instructions explicitly.
