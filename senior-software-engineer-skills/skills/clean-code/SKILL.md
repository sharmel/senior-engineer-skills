---
name: clean-code
description: Implement maintainable software changes that fit an existing codebase. Use when adding or modifying production code where naming, cohesion, dependencies, error handling, and readability matter.
---

# Clean Code

Read neighbouring code and tests before writing. Match established language, framework, formatting, typing, and error conventions unless they are the issue being fixed.

## Implementation rules

- Give modules, types, functions, and variables names that expose intent.
- Keep each unit cohesive; split by responsibility, not arbitrary line count.
- Make dependencies and side effects explicit.
- Prefer composition and existing abstractions; add an abstraction only after a real variation point appears.
- Validate at boundaries and preserve domain invariants internally.
- Handle errors where useful context or recovery exists; do not swallow them.
- Avoid boolean parameter traps, hidden global state, premature genericity, and duplicated business rules.
- Comment decisions and constraints, not syntax.

After implementation, reread the diff as a reviewer. Remove accidental complexity, dead code, speculative hooks, misleading comments, and unrelated formatting churn. Verify behaviour with focused tests and repository-standard static checks.
