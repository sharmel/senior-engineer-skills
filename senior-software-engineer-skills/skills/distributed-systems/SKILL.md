---
name: distributed-systems
description: Design or review communication between processes, services, regions, queues, or replicas. Use when partial failure, retries, consistency, ordering, duplication, or coordination affects correctness.
---

# Distributed Systems

Assume networks delay, reorder, duplicate, and drop messages; processes pause or restart; clocks differ; dependencies fail independently.

## Decision workflow

1. State invariants and required consistency per operation.
2. Identify every remote boundary and failure outcome, including ambiguous completion.
3. Assign end-to-end deadlines and bounded retries with jitter; retry only transient, safe operations.
4. Make operations idempotent or deduplicate with a durable identity and defined retention.
5. Define ordering scope, concurrency, backpressure, overload behaviour, and poison-message handling.
6. Choose availability versus consistency explicitly during partitions.
7. Avoid distributed transactions unless their cost and failure model are justified. Consider outbox/inbox, sagas, or reconciliation.
8. Add correlation, lag, retry, saturation, and invariant-violation telemetry.

Test duplicate delivery, out-of-order events, timeouts after commit, dependency outage, consumer restart, replay, and recovery. “Exactly once” requires a precise boundary and proof; otherwise describe the effective guarantee honestly.
