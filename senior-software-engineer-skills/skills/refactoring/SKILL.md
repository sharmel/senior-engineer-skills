---
name: refactoring
description: Improve internal software design while preserving intended observable behaviour. Use for reducing duplication, coupling, complexity, poor boundaries, or technical debt without adding product scope.
---

# Refactoring

Establish the behaviour boundary before changing structure.

## Workflow

1. Identify the concrete pain: change friction, defects, duplication, unclear ownership, or test difficulty.
2. Characterise current behaviour with existing tests and focused characterization tests where coverage is weak.
3. Define invariants and explicitly exclude unrelated feature changes.
4. Choose a small sequence of named transformations: extract, move, rename, introduce boundary, replace conditional, or remove duplication.
5. Keep each step reviewable and the system runnable.
6. Run focused tests after each risky transformation and the broader relevant suite at the end.
7. Remove obsolete paths and update documentation after consumers migrate.

Avoid simultaneous rewrites, speculative abstractions, broad formatting churn, and mixing schema/API breaks into a behaviour-preserving change. Measure success by simpler change paths and preserved behaviour, not by new layers or fewer lines alone.
