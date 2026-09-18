---
name: architecture-design
description: Evaluate and document consequential software architecture choices. Use for service boundaries, platform shifts, cross-cutting integrations, major dependencies, or decisions costly to reverse.
---

# Architecture Design

Architecture is a set of trade-offs under constraints.

## Workflow

1. Establish business drivers, constraints, workload, data sensitivity, team capabilities, and existing system boundaries.
2. Prioritise quality attributes and define scenarios that make them measurable.
3. Generate at least two credible options, including improving the current design where viable.
4. Compare coupling, cohesion, failure modes, operability, security, delivery speed, migration effort, cost, and reversibility.
5. Select the simplest option meeting the drivers. Identify assumptions and rejected alternatives.
6. Define component responsibilities, interfaces, trust boundaries, data ownership, and deployment topology.
7. Plan incremental migration, compatibility, observability, and rollback.
8. Record a concise ADR when the decision is durable or cross-cutting.

Avoid technology selection before requirements, distributed boundaries without ownership, shared databases that undermine autonomy, and diagrams without failure paths. Validate risky assumptions with a spike or measurement rather than confidence alone.
