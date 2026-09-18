---
name: engineering-planning
description: Create or maintain an implementation plan grounded in an existing codebase. Use before non-trivial features, migrations, refactors, integrations, or fixes spanning multiple concerns.
---

# Engineering Planning

Produce a plan another engineer can execute without rediscovering the problem.

## Discover before planning

- Read repository instructions and relevant configuration.
- Trace the current behaviour from entry point through dependencies and tests.
- Identify affected interfaces, data, deployment, and operational paths.
- Separate confirmed facts, reasonable inferences, and open questions.
- Check working-tree state so the plan does not overwrite unrelated changes.

## Plan structure

Define:

1. Outcome and non-goals.
2. Current-state evidence, citing concrete files or components.
3. Proposed approach and why it fits existing conventions.
4. Ordered implementation slices, each independently verifiable where possible.
5. Contract, schema, security, compatibility, rollout, and rollback implications.
6. Test strategy mapped to risks and acceptance criteria.
7. Open decisions that materially change implementation.

Each step must name the intended change, location, dependencies, and observable completion check. Avoid vague steps such as “update backend” or “add tests.”

## Proportionality

- Small edit: short inline plan.
- Multi-file change: tracked checklist with explicit verification.
- High-risk migration: phases, compatibility window, monitoring, rollback, and ownership.

Update the plan when evidence invalidates it; do not preserve a stale plan for appearance. Planning is complete when the approach is executable and remaining uncertainty is explicit.
