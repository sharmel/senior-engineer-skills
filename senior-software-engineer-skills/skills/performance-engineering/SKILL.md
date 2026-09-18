---
name: performance-engineering
description: Investigate and improve latency, throughput, resource use, startup time, or scalability using measurements. Use for performance regressions, capacity concerns, or explicit optimisation work.
---

# Performance Engineering

No optimisation without a workload, baseline, and target.

## Workflow

1. Define the user-visible metric, percentile, load shape, data size, environment, and success threshold.
2. Reproduce and establish a stable baseline.
3. Profile across client, network, application, runtime, database, cache, queue, and dependencies as relevant.
4. Find the dominant bottleneck and distinguish latency, saturation, contention, allocation, and algorithmic causes.
5. Propose options with expected benefit and trade-offs in complexity, cost, consistency, and reliability.
6. Change one dominant factor, then benchmark against the same baseline.
7. Validate correctness and watch for shifted bottlenecks or tail-latency regressions.

Prefer reducing work, round trips, and contention before adding hardware or concurrency. Treat caches, batching, parallelism, and indexes as consistency and operational decisions, not free speed. Record methodology and results so measurements are reproducible.
