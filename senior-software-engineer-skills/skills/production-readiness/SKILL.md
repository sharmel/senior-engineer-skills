---
name: production-readiness
description: Assess whether a service or change is safe to release and operate. Use for launch reviews, release gates, operational hardening, or requests to make software production-ready.
---

# Production Readiness

Evaluate evidence, not the presence of fashionable tooling.

## Review areas

1. **Correctness:** acceptance criteria, tests, migrations, compatibility, failure behaviour.
2. **Reliability:** SLOs, timeouts, retries, overload, graceful shutdown, redundancy, dependency budgets.
3. **Security:** threat model, access control, secrets, data protection, vulnerabilities, audit.
4. **Observability:** structured events, correlation, metrics, traces, dashboards, actionable alerts.
5. **Operations:** ownership, runbooks, capacity, backups, restore tests, disaster recovery, support hours.
6. **Delivery:** immutable artifacts, environment parity, staged rollout, rollback/forward-fix, feature controls.
7. **Cost and compliance:** expected spend, limits, retention, privacy, licensing, required approvals.

Classify gaps as release-blocking, time-bound follow-up, or accepted risk with an owner. A control is complete only when its operation has evidence—for example, a restored backup rather than a configured backup job. End with a release recommendation, conditions, residual risks, and monitoring plan.
