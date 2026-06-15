# NIST CSF Control Mapping

## Framework Version: NIST CSF 2.0

| CSF Function | Category | Subcategory | Control Implemented | Status |
|---|---|---|---|---|
| Identify | Asset Management | ID.AM-1 | Asset inventory maintained and reviewed quarterly | ✅ Implemented |
| Identify | Risk Assessment | ID.RA-1 | Risk register maintained using Likelihood × Impact scoring and reviewed on a defined cadence | ✅ Implemented |
| Identify | Governance | ID.GV-1 | Documented security policies (AUP, IR) approved and reviewed annually | ✅ Implemented |
| Identify | Supply Chain Risk Management | ID.SC-1 | Vendor/SaaS risks tracked (e.g., payment gateway, cloud providers) with SLAs and breach notification requirements | 🔄 In Progress |
| Protect | Identity Management, Authentication & Access Control | PR.AC-1 | MFA enforced for all privileged accounts | ✅ Implemented |
| Protect | Identity Management, Authentication & Access Control | PR.AC-4 | Role-based access control (RBAC) enforced for sensitive systems/data and reviewed quarterly | 🔄 In Progress |
| Protect | Data Security | PR.DS-1 | Full-disk encryption required on managed endpoints (BitLocker/FileVault) | ✅ Implemented |
| Protect | Data Security | PR.DS-2 | Sensitive data stored only in approved, access-controlled storage; prevent use of personal cloud storage for institutional data | ✅ Implemented |
| Protect | Platform Security | PR.PS-1 | Patch/vulnerability management: critical updates applied within 72 hours; routine vulnerability scanning performed | 🔄 In Progress |
| Protect | Technology Infrastructure Resilience | PR.IR-1 | DDoS protection / rate limiting enabled for public-facing services (e.g., WAF/CDN protections) | 🔄 In Progress |
| Protect | Awareness & Training | PR.AT-1 | Annual security awareness training for all staff (plus periodic phishing awareness) | 🔄 In Progress |
| Detect | Security Continuous Monitoring | DE.CM-1 | Centralized logging/monitoring (SIEM) for key systems and security events | ✅ Implemented |
| Detect | Anomalies & Events | DE.AE-1 | SIEM deployed (Microsoft Sentinel) with alert triage and escalation workflow | ✅ Implemented |
| Respond | Response Planning | RS.RP-1 | Incident Response Policy documented with severity levels, response times, and PICERL workflow | ✅ Implemented |
| Respond | Communications | RS.CO-1 | Defined escalation contacts and notification procedures (SOC/IT/GRC/Legal/HR as needed) | ✅ Implemented |
| Respond | Mitigation | RS.MI-1 | Standard containment actions supported (endpoint isolation, IOC blocking, credential/key rotation) | 🔄 In Progress |
| Recover | Recovery Planning | RC.RP-1 | DR/BCP plan documented and tested annually | 🔄 In Progress |
| Recover | Improvements | RC.IM-1 | Post-incident lessons learned performed; corrective actions tracked to closure | 🔄 In Progress |
