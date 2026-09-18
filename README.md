# Senior Software Engineer Skills

A language-agnostic collection of Agent Skills for planning, designing, building, reviewing, and operating production software. The pack is intentionally framework-neutral: each skill first inspects the repository and adapts to its conventions.

## Install

Install the complete repository:

```bash
npx skills add YOUR_GITHUB_ORG/senior-software-engineer-skills
```

Install a single skill interactively:

```bash
npx skills add YOUR_GITHUB_ORG/senior-software-engineer-skills --skill engineering-planning
```

For a local checkout:

```bash
npx skills add ./senior-software-engineer-skills
```

Use `$senior-engineer` for end-to-end work, or invoke a specialist directly, such as `$systematic-debugging` or `$api-engineering`.

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
