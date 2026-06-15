\# Risk Assessment Methodology



\## Framework Used

This risk assessment follows the \*\*NIST SP 800-30\*\* risk assessment methodology, tailored to HandmadeHub’s environment by focusing on three critical asset groups identified in the register:



\- \*\*Asset A:\*\* Webstore (eCommerce site \& database)

\- \*\*Asset B:\*\* Customer Payment Data (payment gateway / PCI-related processing)

\- \*\*Asset C:\*\* Product Images \& Marketing Content (cloud-stored digital assets)



Risks were identified per asset, documented with business impact context, and assigned an accountable \*\*asset/risk owner\*\* for follow-through.



\## Risk Scoring

Each risk was scored using a \*\*Probability × Impact\*\* model on a \*\*1–5\*\* scale:



\- \*\*Likelihood (1–5):\*\* 1 (Rare) → 5 (Almost Certain)

\- \*\*Impact (1–5):\*\* 1 (Negligible) → 5 (Catastrophic)

\- \*\*Risk Score = Likelihood × Impact\*\*



Scores were assigned based on the scenario details in the register (for example: common attack vectors like phishing, realistic exposure like plugin/CMS patch gaps, and operational dependency on cloud/payment providers).



\## Risk Ratings

Risk ratings were determined directly from the calculated score (L×I):



| Score | Rating | Action Required |

|---|---|---|

| 20–25 | Critical | Immediate remediation |

| 12–19 | High | Remediate within 30 days |

| 6–11 | Medium | Remediate within 90 days |

| 1–5 | Low | Monitor and review quarterly |



\## Risk Treatment Options

Each risk includes a response decision aligned to the register’s approach:



\- \*\*Avoid\*\* — Eliminate the activity causing the risk

\- \*\*Mitigate\*\* — Reduce likelihood or impact using controls (e.g., MFA, WAF, backups, patching, RBAC, audit logging)

\- \*\*Transfer\*\* — Shift part of the risk to a third party (e.g., vendor SLA, cyber insurance, managed protections like DDoS services)

\- \*\*Accept\*\* — Acknowledge residual risk and monitor (used when impact/likelihood and cost/benefit justify acceptance)



\## Control Selection (How mitigations were chosen)

Controls/mitigations in the register were selected using a “practical + high-impact” approach appropriate for a small business:



\- \*\*Preventive controls\*\* (MFA, WAF, TLS/HSTS, secrets management, least privilege/RBAC)

\- \*\*Detective controls\*\* (audit log reviews, alerting, secret-scanning)

\- \*\*Corrective/Recovery controls\*\* (off-site backups with testing, versioning/object lock, failover planning)



\## Governance (Ownership and tracking)

\- Each entry includes a \*\*Risk Owner\*\* tied to the asset owner (IT, Finance, Marketing).

\- Each asset section includes “\*\*Top risks for immediate attention\*\*” to prioritize remediation based on highest scores and most likely real-world attack paths.

\- Status is tracked as \*\*Open\*\* or \*\*In Progress\*\* to show execution progress of mitigations.

