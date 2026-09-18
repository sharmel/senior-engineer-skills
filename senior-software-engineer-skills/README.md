# Senior Software Engineer Skills

A language-agnostic collection of Agent Skills for planning, designing, building, reviewing, and operating production software. The pack is intentionally framework-neutral: each skill first inspects the repository and adapts to its conventions.

## Installation

Install the complete repository:

```bash
npx skills add sharmel/senior-engineer-skills
```

Preview all available skills before installation:

```bash
npx skills add sharmel/senior-engineer-skills --list
```

Install one skill by name:

```bash
npx skills add sharmel/senior-engineer-skills --skill senior-engineer
npx skills add sharmel/senior-engineer-skills --skill engineering-planning
```

Install from a local checkout:

```bash
git clone https://github.com/sharmel/senior-engineer-skills.git
cd senior-engineer-skills
npx skills add .
```

## Using the skills

After installation, open your coding agent inside the software project you want to change:

```bash
cd my-project
claude
```

Or, for Codex:

```bash
cd my-project
codex
```

Invoke a skill by naming it in your request:

```text
Use $senior-engineer to add password-reset functionality to this application.

Inspect the existing architecture first, create an implementation plan,
implement the change, add tests, and verify it.
```

Explicit invocation is recommended when you require a particular workflow:

```text
Use $systematic-debugging to investigate the failing payment integration tests.
```

Compatible agents may also select an installed skill automatically from its description. Explicitly naming the skill remains the clearest way to request a specific process.

## Skills

| Skill | Purpose |
| --- | --- |
| `senior-engineer` | Routes work through discovery, planning, implementation, and verification |
| `engineering-planning` | Produces evidence-based, executable implementation plans |
| `requirements-analysis` | Turns requests into testable scope and acceptance criteria |
| `architecture-design` | Makes consequential architecture decisions and ADRs |
| `system-design` | Designs systems from workload, data, reliability, and cost needs |
| `clean-code` | Implements maintainable changes aligned with repository conventions |
| `api-engineering` | Designs safe, evolvable APIs and contracts |
| `data-engineering` | Designs schemas, migrations, transactions, and data access |
| `distributed-systems` | Handles partial failure, consistency, messaging, and resilience |
| `security-engineering` | Threat-models and hardens application changes |
| `testing-strategy` | Chooses risk-based tests across the testing pyramid |
| `systematic-debugging` | Diagnoses root causes before applying minimal fixes |
| `code-review` | Performs severity-ranked, evidence-based reviews |
| `refactoring` | Improves design while preserving observable behaviour |
| `performance-engineering` | Measures and removes verified bottlenecks |
| `delivery-engineering` | Builds safe CI/CD, containers, IaC, and release workflows |
| `kubernetes-production` | Designs and reviews production Kubernetes workloads |
| `production-readiness` | Runs operational readiness and release-risk reviews |
| `incident-response` | Coordinates evidence-led incident mitigation and recovery |
| `frontend-engineering` | Builds accessible, responsive, resilient user interfaces |
| `ai-engineering` | Builds evaluated, secure, observable LLM/RAG systems |
| `technical-documentation` | Creates accurate docs, ADRs, runbooks, and API guidance |

## Workflow

`senior-engineer` is the entry point. It requires a proportional planning stage, selects only the specialists relevant to the change, and finishes with evidence from tests or other checks. Specialist skills can also be used independently.

For substantial development work, use this request template:

```text
Use $senior-engineer for this task.

Requirement:
[Describe the required outcome]

Constraints:
[List technical or business constraints]

Acceptance criteria:
[List the expected observable behaviour]

Inspect the repository, create a plan, implement the smallest coherent
change, run the relevant tests, and report remaining risks.
```

The orchestrator leads work through:

```text
Repository discovery
→ Requirements
→ Planning
→ Relevant specialist skills
→ Implementation
→ Verification
→ Handoff
```

## Usage examples

### Plan without implementing

```text
Use $engineering-planning to create a detailed implementation plan for
adding multi-tenant authentication. Do not modify the code yet.
```

### Clarify requirements

```text
Use $requirements-analysis to turn this feature request into bounded,
testable requirements, assumptions, non-goals, and acceptance criteria.
```

### Debug a defect

```text
Use $systematic-debugging to investigate why the login API occasionally
returns HTTP 500.

Reproduce the failure, collect evidence, identify the root cause, and do not
change the code until the cause is established.
```

### Review a pull request

```text
Use $code-review to review the current branch against main.

Focus on correctness, security, regressions, performance, and missing tests.
Do not modify the code.
```

### Design an API

```text
Use $api-engineering to design the account-management REST API.

Cover authentication, authorization, validation, errors, pagination,
idempotency, compatibility, and contract tests.
```

### Review an architecture

```text
Use $architecture-design to review this microservices architecture.

Compare credible alternatives and document the selected approach as an ADR.
```

### Plan a database migration

```text
Use $data-engineering to plan a zero-downtime migration that adds tenant IDs
to existing customer records.

Include constraints, backfill, compatibility, validation, rollout, and recovery.
```

### Review security

```text
Use $security-engineering to review the authentication and authorization
changes on this branch.

Identify trust boundaries, abuse cases, vulnerable paths, and verification.
```

### Define a testing strategy

```text
Use $testing-strategy to create a risk-based test strategy for checkout.

Map each important risk and acceptance criterion to the appropriate test level.
```

### Investigate performance

```text
Use $performance-engineering to investigate why the search endpoint's p95
latency increased from 300 ms to 2 seconds.

Establish a baseline, profile the request path, and optimize only the verified
bottleneck.
```

### Review Kubernetes workloads

```text
Use $kubernetes-production to review the manifests in the k8s directory.

Check probes, resources, autoscaling, disruption handling, graceful shutdown,
security, configuration, storage, rollout, and observability.
```

### Assess production readiness

```text
Use $production-readiness to assess whether this service is ready for production.

Classify findings as release blockers, time-bound follow-up work, or accepted risks.
```

### Build a frontend feature

```text
Use $frontend-engineering to build the account settings interface.

Follow the existing design system and cover responsive behaviour, accessibility,
loading, empty, validation, permission, and error states.
```

### Build an AI or RAG feature

```text
Use $ai-engineering and $security-engineering to implement tenant-aware document
retrieval for this RAG application.

Include access filtering, retrieval evaluation, prompt-injection protection,
citations, observability, latency, and cost controls.
```

### Write technical documentation

```text
Use $technical-documentation to create an operations runbook for this service.

Ground every instruction in the repository and include diagnosis, mitigation,
verification, rollback, and escalation.
```

## Combining skills

For large or high-risk work, specify the skills and their order:

```text
Use these skills in order:

1. $requirements-analysis
2. $engineering-planning
3. $architecture-design
4. $api-engineering
5. $testing-strategy
6. $production-readiness

Build tenant-aware document ingestion for this application.
Start with requirements and planning before modifying code.
```

Select only the skills that materially improve the task; do not load every specialist for every change.

## Design principles

- Evidence before assumptions.
- Plans before non-trivial implementation.
- Small, reversible changes.
- Security, operability, and compatibility are design inputs.
- Verification claims include the command or observation that supports them.
- Existing project conventions win unless there is a documented reason to change them.

## Contributing

Keep skills concise and operational. A skill should change agent behaviour, not duplicate a textbook. Validate every changed skill before opening a pull request.

## License

MIT
