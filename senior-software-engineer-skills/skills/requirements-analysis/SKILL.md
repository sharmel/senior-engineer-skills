---
name: requirements-analysis
description: Clarify software requests and convert them into bounded, testable requirements. Use when behaviour, users, constraints, edge cases, or success criteria are incomplete or conflicting.
---

# Requirements Analysis

Turn intent into a contract without inventing product policy.

## Method

1. Identify actors, desired outcomes, current behaviour, and business rules.
2. Extract functional requirements and quality attributes: security, latency, availability, accessibility, compliance, cost, and maintainability.
3. List inputs, outputs, state transitions, permissions, failures, and boundary cases.
4. Resolve contradictions with repository evidence or the requester. Ask only questions whose answers materially change the design.
5. Define scope and non-goals.
6. Write observable acceptance criteria, preferably as Given/When/Then or equivalent examples.
7. Map each criterion to a verification method.

## Guardrails

Distinguish requirements from implementation ideas. Do not turn an example into a universal rule. Record assumptions with their consequence and validation path. Escalate legal, regulatory, or domain-policy uncertainty rather than encoding a guess.

Deliver a compact requirement brief plus unresolved decisions. It is ready when engineering and product can independently tell whether the change succeeds.
