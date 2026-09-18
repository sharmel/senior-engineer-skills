---
name: delivery-engineering
description: Design or modify CI/CD pipelines, build systems, containers, infrastructure as code, and release strategies. Use when software must be built, verified, packaged, promoted, deployed, or rolled back safely.
---

# Delivery Engineering

Create a reproducible path from source to a traceable immutable artifact.

## Workflow

1. Inspect existing build, environments, secrets, artifact registry, and deployment ownership.
2. Make builds deterministic, cached safely, and pinned where supply-chain risk warrants it.
3. Order fast feedback before expensive checks: format/type/static analysis, unit tests, integration/contract tests, security scans, packaging, deployment checks.
4. Build once and promote the same signed or checksummed artifact.
5. Keep credentials short-lived and least-privileged; never print secrets or accept untrusted code in privileged contexts.
6. Externalise configuration and validate it at startup.
7. Choose rolling, canary, blue/green, or feature-flag rollout based on risk and state compatibility.
8. Define health verification, migration ordering, rollback/forward-fix, and post-deploy monitoring.

Container images should be minimal, non-root where feasible, reproducible, and scanned. Infrastructure changes need plans, environment isolation, state protection, drift awareness, and review. Test the failure and rollback path, not only the happy deployment.
