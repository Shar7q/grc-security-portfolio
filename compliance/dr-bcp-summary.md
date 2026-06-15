# DR/BCP Summary (Unit 39)

## Overview (DR vs BCP)
- **Disaster Recovery (DR)** focuses on restoring **IT systems and data** after an outage (ransomware, power loss, hardware failure, cloud outage).
- **Business Continuity Planning (BCP)** focuses on keeping **critical business operations running** while IT is degraded or offline using alternate workflows, people/process plans, and fallback capabilities.

## RTO (Recovery Time Objective)
**RTO** is the *maximum acceptable downtime* for a system/service before the impact becomes unacceptable (financial, operational, legal, reputational).

**How it’s set (per Unit 39):**
- Start with a **Business Impact Analysis (BIA)** to identify critical processes and quantify downtime impact.
- Assign **shorter RTOs** to Tier 1 / mission-critical services and **longer RTOs** to non-critical systems.

## RPO (Recovery Point Objective)
**RPO** is the *maximum acceptable data loss*, measured in time (how far back restored data can be).

**How it’s set (per Unit 39):**
- Tighter RPO = more frequent backups or **real-time replication**
- Looser RPO = less frequent backups (lower cost), but more tolerated data loss

## Backup Strategy (what Unit 39 emphasized)
A resilient backup approach includes:
- **Cloud backups** (scheduled, automated, off-site) for cost-effective recovery
- **Offline / air-gapped backups** to reduce ransomware impact
- **Immutable backups** (cannot be altered/deleted by an attacker)
- **Backup testing** (regular restore tests) to validate backups actually work
- **Tier-based protection:**
  - Tier 1 systems may require **real-time replication** (near-zero RPO)
  - Tier 2/3 systems may be fine with daily/weekly backups

## Recovery Procedures (high-level runbook flow)
Unit 39’s recovery procedure approach is “runbook-driven” and includes:

1. **BIA + Dependency Mapping**
   - Identify critical services and map what they depend on (apps → databases → network → vendors)

2. **Failover (if available)**
   - Switch production to a secondary environment (hot/warm site or cloud failover)
   - Can be **automatic** or **manual**, depending on design

3. **Restore / Rebuild**
   - Restore systems and data from the most recent valid backup (aligned to RPO)
   - If compromised (e.g., ransomware), rebuild from known-good images before restoring data

4. **Validation**
   - Confirm integrity, access, and functionality (data checks, application tests, authentication verification)

5. **Failback**
   - After primary is repaired and validated, migrate operations back carefully (planned + tested to avoid a second outage)

## Testing & Continuous Improvement
Unit 39 emphasized that DR/BCP plans must be tested and updated:
- **Tabletop exercises** (walkthrough scenario + decisions)
- **Partial failover drills** (validate switching for a non-critical service)
- **Full recovery drills** (end-to-end restore)
- Update RTO/RPO targets and runbooks after tests or real incidents

## Example targets (illustrative)
*(These are example values consistent with Unit 39 concepts—swap with your chosen numbers if you defined specific targets in your submission.)*
- **Tier 1 (critical services):** RTO = 1–4 hours, RPO = 15–60 minutes (replication or frequent backups)
- **Tier 2 (important services):** RTO = 8–24 hours, RPO = 4–24 hours (daily backups)
- **Tier 3 (non-critical services):** RTO = 2–7 days, RPO = 1–7 days (weekly backups / lower cost)
