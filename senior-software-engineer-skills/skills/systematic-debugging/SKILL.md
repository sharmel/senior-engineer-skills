---
name: systematic-debugging
description: Diagnose reproducible or intermittent defects using evidence and controlled hypotheses. Use for failing tests, crashes, incorrect behaviour, regressions, production symptoms, or unexplained performance changes.
---

# Systematic Debugging

Do not begin with speculative edits.

## Workflow

1. Define expected versus observed behaviour, scope, severity, and earliest known occurrence.
2. Reproduce with the smallest reliable case. Preserve exact inputs, environment, versions, and timestamps.
3. Gather evidence from tests, logs, traces, metrics, state, recent diffs, and dependency boundaries. Redact sensitive data.
4. Trace the bad value or control flow backward to its origin.
5. Form ranked, falsifiable hypotheses. Change one variable at a time.
6. Identify the root cause and explain why it produces all important symptoms.
7. Add a regression test that fails for the cause when feasible.
8. Apply the smallest durable fix at the correct abstraction boundary.
9. Re-run the reproducer, focused tests, relevant suite, and operational checks.

If reproduction is unsafe or impossible, improve telemetry and state the uncertainty. Stop after repeated disproven hypotheses and reassess assumptions rather than stacking unverified changes.
