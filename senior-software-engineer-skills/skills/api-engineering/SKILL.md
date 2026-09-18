---
name: api-engineering
description: Design, implement, or review HTTP, RPC, event, webhook, or streaming APIs. Use when contracts, compatibility, validation, authorization, idempotency, pagination, or error semantics matter.
---

# API Engineering

## Contract first

Identify consumers, use cases, protocol constraints, latency, authentication, authorization, and compatibility obligations. Model domain concepts rather than persistence details.

For each operation define inputs, outputs, validation, permissions, error taxonomy, deadlines, side effects, concurrency semantics, and observability. For mutations decide idempotency behaviour and duplicate-request storage. For collections define deterministic pagination, filtering, and sorting. For asynchronous APIs define delivery, ordering, deduplication, schema evolution, and replay semantics.

## Evolution

Prefer additive change. Do not silently change meanings, defaults, required fields, enum handling, or error shapes. When breaking change is unavoidable, specify migration, version coexistence, telemetry, and removal criteria.

## Safety and verification

Reject malformed input at the boundary, authorize the resource rather than only the route, limit payloads and rates, and never expose secrets or internal stack details. Keep the specification and implementation synchronized. Verify with contract tests, authorization tests, invalid-input cases, duplicate/retry cases, and representative consumer flows.
