---
name: kubernetes-production
description: Design, implement, or review Kubernetes workloads for production. Use for manifests, Helm/Kustomize, scaling, availability, networking, security, configuration, storage, or rollout concerns.
---

# Kubernetes Production

Apply Kubernetes only after understanding the application's runtime and failure model.

## Workload checklist

- Select the correct controller and service exposure.
- Set realistic resource requests and limits from measurements.
- Separate startup, readiness, and liveness semantics; probes must not amplify outages.
- Support graceful termination within the platform deadline.
- Define replicas, topology spread or anti-affinity, HPA signals, and a PDB consistent with real capacity.
- Keep configuration external; use an appropriate secret provider and avoid plaintext secrets.
- Run with least privilege: non-root, restricted capabilities, read-only filesystem where compatible, service-account RBAC, and network policies.
- Define storage class, access mode, backup, restore, and disruption behaviour for stateful workloads.
- Use immutable image references and safe rollouts with observable rollback criteria.
- Expose logs, metrics, traces, events, and workload/cluster saturation signals.

Render templates before applying, validate schemas and policies, inspect diffs, and test rollout, rescheduling, scale, and dependency-failure behaviour. Do not assume HPA or PDB alone creates availability.
