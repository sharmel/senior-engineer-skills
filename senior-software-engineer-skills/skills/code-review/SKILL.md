---
name: code-review
description: Review a proposed software change for correctness, regressions, security, maintainability, performance, and missing tests. Use for diffs, pull requests, patches, or pre-merge review.
---

# Code Review

Prioritise findings that can change the merge decision.

## Review method

1. Read the requirement, repository instructions, and complete diff in context.
2. Trace changed behaviour through callers, dependencies, persistence, concurrency, and failure paths.
3. Check correctness, compatibility, security, data integrity, reliability, performance, operability, and test adequacy.
4. Validate suspected issues against code or executable evidence; do not report style preferences as defects.
5. Rank findings: critical, high, medium, or low based on realistic impact and likelihood.

Each finding must identify the location, concrete failure scenario, consequence, and smallest useful remediation. Keep summaries separate from blocking findings. If no actionable defect is found, say so and note meaningful residual risk or untested areas. Do not modify code unless the requester also asked for fixes.
