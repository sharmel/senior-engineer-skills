---
name: testing-strategy
description: Plan, implement, or improve tests for a software change or system. Use when selecting test levels, coverage boundaries, fixtures, contracts, reliability checks, or release confidence.
---

# Testing Strategy

Optimise for confidence and useful failure diagnosis, not a coverage percentage.

## Workflow

1. Map requirements and major risks to observable behaviours.
2. Place each assertion at the lowest stable level that proves it.
3. Use unit tests for logic, integration tests for real boundaries, contract tests for independently deployed interfaces, and a small set of end-to-end tests for critical journeys.
4. Include failure, boundary, concurrency, authorization, migration, and retry cases relevant to the change.
5. Prefer deterministic fixtures, isolated state, controlled time/randomness, and realistic dependencies through containers or fakes where useful.
6. Avoid mocks that merely reproduce implementation details.
7. Keep tests readable: arrange context, perform behaviour, assert outcome and important side effects.

Run the narrowest tests while iterating, then the relevant suite and static checks. Investigate flaky tests as defects; do not normalise retries as the primary fix. Report what was and was not exercised.
