---
name: data-engineering
description: Design or change application data models, persistence code, queries, transactions, indexes, caches, and migrations. Use when correctness, concurrency, performance, retention, or schema evolution is involved.
---

# Data Engineering

Start from invariants and access patterns, not a preferred database.

## Workflow

1. Define ownership, entities, relationships, lifecycle, sensitivity, volume, and read/write patterns.
2. Encode correctness with types and database constraints where possible.
3. Choose transaction boundaries and concurrency control deliberately; describe race behaviour.
4. Inspect query plans and measured workload before adding indexes or denormalisation.
5. Treat caches as derived state; define keys, invalidation, TTL, stampede control, and stale-read tolerance.
6. Design migrations for the real data size and deployment model.

For zero-downtime schema changes prefer expand, migrate/backfill, switch, then contract. Make backfills resumable, observable, bounded, and safe to rerun. Keep old and new application versions compatible during rollout. Specify rollback limits; destructive migrations often require restore or forward-fix rather than reversal.

Test constraints, transactions, migration from representative old state, rollback or recovery, query performance, and backup restoration where relevant. Never treat an ORM migration file as proof that production migration is safe.
