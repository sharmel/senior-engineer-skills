---
name: security-engineering
description: Threat-model, implement, or review security-sensitive software and infrastructure changes. Use for identity, permissions, secrets, sensitive data, untrusted input, public endpoints, uploads, payments, or supply-chain changes.
---

# Security Engineering

Security review does not grant permission to access systems or perform intrusive testing.

## Workflow

1. Identify assets, actors, trust boundaries, entry points, data classification, and abuse cases.
2. Model likely threats and rank them by impact and feasibility.
3. Minimise attack surface and privileges. Deny by default.
4. Authenticate identities using established libraries and protocols; authorize every object/action server-side.
5. Validate untrusted input at boundaries and use safe APIs for queries, templates, commands, paths, URLs, and deserialization.
6. Protect data in transit and at rest; define secret storage, rotation, and redaction.
7. Address session/token expiry, revocation, replay, CSRF, origin policy, rate limits, and auditability as applicable.
8. Check dependency provenance, lockfiles, scanning, artifact integrity, and least-privilege CI credentials.

Do not create custom cryptography or expose sensitive values in logs or errors. Verify negative authorization paths, tenant isolation, injection cases, secret absence, dependency findings, and secure defaults. Clearly separate verified vulnerabilities from defence-in-depth suggestions.
