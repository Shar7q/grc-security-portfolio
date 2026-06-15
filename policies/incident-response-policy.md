# Incident Response Policy

## Purpose
This Incident Response (IR) Policy defines how the organization detects, triages, contains, eradicates, and recovers from security incidents. The goal is to minimize business impact, protect sensitive data, preserve evidence for investigation, and ensure consistent communication and escalation during events such as malware infections, account compromise, and data breaches.

## Scope
This policy applies to:
- All employees, contractors, and third parties with access to organizational systems
- All endpoints (laptops/desktops), servers, cloud services, email platforms, and SaaS applications
- All networks (on-prem, remote/VPN, and cloud environments)
- All data types, including sensitive data (PII, credentials, financial data, institutional records)

## IR Team Roles & Responsibilities

**SOC Analyst / Tier 1**
- Monitor alerts (SIEM/EDR/email security), validate indicators, and perform initial triage
- Open an incident ticket, document timeline/actions, and assign severity
- Escalate per classification table and playbooks

**SOC Analyst / Tier 2 (Incident Handler)**
- Lead investigation, scope affected users/systems, and confirm impact
- Execute containment actions (isolation, account disable/reset, blocking IOCs)
- Coordinate evidence collection and ensure chain-of-custody basics

**IR Lead / SOC Manager**
- Own incident command, decision-making, and prioritization
- Approve high-impact containment actions (service blocks, org-wide resets)
- Coordinate communications with executives, IT, legal, and stakeholders

**IT Operations / System Administrators**
- Apply technical fixes (patching, rebuilds, restores, configuration changes)
- Support containment (network blocks, firewall changes, endpoint remediation)
- Validate recovery and system health

**Security/GRC / Compliance**
- Determine reporting obligations (regulatory, contractual) and required documentation
- Ensure post-incident corrective actions are tracked to closure

**Legal / HR (as needed)**
- Support investigations involving insider activity, policy violations, or legal exposure
- Guide external notifications and evidence handling requirements

## Incident Classification

| Severity | Description | Response Time |
|---|---|---|
| P1 - Critical | Active breach, ransomware, data exfiltration | 15 minutes |
| P2 - High | Malware detected, account compromise | 1 hour |
| P3 - Medium | Suspicious activity, policy violation | 4 hours |
| P4 - Low | False positive, minor anomaly | 24 hours |

**Severity assignment considerations (SOC triage)**
- **Impact:** data sensitivity, business downtime, number of systems/users affected
- **Threat credibility:** confirmed malicious activity vs. suspected/low-confidence
- **Containment urgency:** active spread, active attacker presence, privilege level
- **Regulatory exposure:** PII, payment data, student records, research/IP

## IR Phases (PICERL)

1. **Preparation**
   - Maintain logging/monitoring (SIEM), endpoint protection (EDR), and alerting
   - Ensure playbooks exist for common events (phishing, malware, ransomware)
   - Maintain asset inventory, backup/restore procedures, and contact lists
   - Run periodic tabletop exercises and update lessons learned

2. **Identification**
   - Validate alert authenticity; determine incident type and entry vector
   - Identify affected users, hosts, IPs, domains, hashes, and timeline
   - Preserve key evidence (alerts, logs, email headers, screenshots, EDR telemetry)
   - Assign severity (P1–P4) and begin incident documentation

3. **Containment**
   - Short-term: isolate hosts in EDR, disable compromised accounts, block IOCs
   - Long-term: segment affected network areas, tighten access controls, add detections
   - Prevent spread (reset passwords/tokens, revoke sessions, disable risky services)

4. **Eradication**
   - Remove malware/persistence, close exploited vulnerabilities, remove rogue accounts
   - Patch systems, rotate credentials/API keys, and remediate misconfigurations
   - If necessary, reimage compromised endpoints/servers using known-good baselines

5. **Recovery**
   - Restore systems/services from clean backups; validate integrity and functionality
   - Monitor closely for re-infection/re-compromise (increased logging/alert thresholds)
   - Return to normal operations only after IR Lead approval for P1/P2 incidents

6. **Lessons Learned**
   - Conduct post-incident review within 5–10 business days (or sooner for P1)
   - Produce a concise report: root cause, impact, dwell time, controls gaps, actions
   - Create remediation tasks with owners and due dates (controls, training, tooling)

## Escalation Contacts
*(Replace with your real contacts in your repo/portfolio example.)*

- **SOC / Security Operations:** [soc@company.com](mailto:soc@company.com) | On-call: +1 (xxx) xxx-xxxx
- **IT Help Desk:** [helpdesk@company.com](mailto:helpdesk@company.com) | Ext. 5500
- **IR Lead / SOC Manager:** [ir-lead@company.com](mailto:ir-lead@company.com)
- **GRC / Compliance:** [grc@company.com](mailto:grc@company.com)
- **Legal (if needed):** [legal@company.com](mailto:legal@company.com)
- **HR (if policy/insider cases):** [hr@company.com](mailto:hr@company.com)

**Escalation rules**
- **P1:** Notify IR Lead immediately; executive notification as directed by IR Lead
- **P2:** Notify IR Lead within 1 hour; engage IT Ops for containment/remediation
- **P3/P4:** Handle via standard ticket workflow; escalate if scope/impact increases

## Review & Maintenance
- This policy is reviewed **annually** and after any **P1/P2** incident.
- SOC playbooks, escalation lists, and tooling assumptions (SIEM/EDR/email) must be updated whenever systems or vendors change.
- Metrics tracked (minimum): time to detect (TTD), time to contain (TTC), number of impacted assets/users, and recurrence rate.
