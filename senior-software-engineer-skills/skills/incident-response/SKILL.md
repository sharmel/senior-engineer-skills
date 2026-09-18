---
name: incident-response
description: Coordinate technical diagnosis, mitigation, recovery, and follow-up during a live or recent software incident. Use for outages, severe degradation, data integrity events, or security-impacting operational failures.
---

# Incident Response

Prioritise safety, user impact, and restoration over elegant diagnosis.

## Response

1. Declare severity, impact, affected scope, start time, and incident owner. Establish one timeline and communication channel.
2. Preserve relevant evidence while protecting sensitive data.
3. Stop harm using the safest reversible mitigation: rollback, feature disablement, traffic shift, capacity relief, or dependency isolation.
4. Track hypotheses and evidence; avoid simultaneous uncoordinated changes.
5. Verify recovery with user-facing signals, not a single green dashboard.
6. Monitor for recurrence and explicitly close or downgrade the incident.

Communicate facts, actions, next checkpoint, and uncertainty without blame. For suspected security incidents, preserve chain of custody and follow the organisation's escalation process.

After recovery, build a timestamped timeline, root cause and contributing factors, detection/response gaps, and corrective actions with owners and dates. Prefer systemic safeguards over reminders to “be careful.” Do not run destructive remediation without explicit authority.
