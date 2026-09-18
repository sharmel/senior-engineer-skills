---
name: system-design
description: Design a software system or major subsystem from requirements through APIs, data, scaling, reliability, security, observability, and cost. Use for greenfield designs and material capacity changes.
---

# System Design

## Design sequence

1. Confirm functional scope, users, consistency needs, and quality targets.
2. Estimate orders of magnitude for traffic, payload, storage, growth, and peak-to-average ratio. State assumptions.
3. Define external contracts and core data model.
4. Draw the request, asynchronous, and data flows; show trust and failure boundaries.
5. Assign ownership and choose storage and communication patterns from access needs.
6. Design for partial failure: deadlines, retries, idempotency, backpressure, isolation, recovery, and degraded modes.
7. Address scaling, caching, partitioning, hotspots, and lifecycle management only where estimates justify them.
8. Define authentication, authorization, encryption, audit, privacy, and abuse controls.
9. Define SLIs/SLOs, telemetry, capacity signals, deployment, backup, restore, and disaster recovery.
10. Compare alternatives and identify the first bottleneck or risk likely to invalidate the design.

Deliver a coherent design with assumptions, decisions, trade-offs, and an evolutionary path. Do not imply precision unsupported by inputs.
