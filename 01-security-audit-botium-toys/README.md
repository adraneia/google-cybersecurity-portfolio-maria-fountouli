# Security Audit: Botium Toys

**Course 2: Play It Safe, Manage Security Risks**

**Skills:** NIST CSF, security controls, compliance (PCI DSS, GDPR, SOC 1/SOC 2), risk assessment

## Scenario
Botium Toys is a fictional small U.S. toy company with one physical location and a fast growing online store that serves customers in the U.S. and the E.U. The IT manager asked for an internal audit to find out which security controls and compliance requirements are missing, based on the scope, goals and risk assessment report she prepared.

## Controls assessment

| Control | In place? |
|---|---|
| Least privilege | ❌ No |
| Disaster recovery plans | ❌ No |
| Password policies | ❌ No |
| Separation of duties | ❌ No |
| Firewall | ✅ Yes |
| Intrusion detection system (IDS) | ❌ No |
| Backups | ❌ No |
| Antivirus software | ✅ Yes |
| Manual monitoring, maintenance and intervention for legacy systems | ✅ Yes |
| Encryption | ❌ No |
| Password management system | ❌ No |
| Locks (offices, storefront, warehouse) | ✅ Yes |
| CCTV surveillance | ✅ Yes |
| Fire detection/prevention | ✅ Yes |

## Compliance checklist
### PCI DSS

| Best practice | In place? |
|---|---|
| Only authorized users have access to customers' credit card information | ❌ No |
| Credit card information is stored, accepted, processed and transmitted internally, in a secure environment | ❌ No |
| Data encryption procedures secure credit card transaction touchpoints and data | ❌ No |
| Secure password management policies are adopted | ❌ No |

### GDPR

| Best practice | In place? |
|---|---|
| E.U. customers' data is kept private/secured | ❌ No |
| There is a plan to notify E.U. customers within 72 hours of a breach | ✅ Yes |
| Data is properly classified and inventoried | ❌ No |
| Privacy policies, procedures and processes are enforced to document and maintain data | ✅ Yes |

### SOC type 1 / SOC type 2

| Best practice | In place? |
|---|---|
| User access policies are established | ❌ No |
| Sensitive data (PII/SPII) is confidential/private | ❌ No |
| Data integrity: data is consistent, complete, accurate and validated | ✅ Yes |
| Data is available to individuals authorized to access it | ✅ Yes |

## Recommendations
To quickly reduce risks and strengthen Botium Toys' security posture, I recommend focusing on a few key areas first. We need to limit employee access to sensitive data and make sure only the right people can view or change it. Encrypting credit card and customer information should be a top priority to meet compliance and protect our users. We should also introduce an intrusion detection system to help spot potential threats earlier and set up reliable backups and a disaster recovery plan, since there's currently no way to recover critical data if something goes wrong. Updating our password policy and using a centralized password management system would make authentication both more secure and easier for employees. Finally, legacy systems should be monitored on a regular schedule with clear procedures in place to avoid unexpected issues. Addressing these areas first will greatly improve our resilience and show stakeholders that we're committed to protecting both the organization and our customers.
