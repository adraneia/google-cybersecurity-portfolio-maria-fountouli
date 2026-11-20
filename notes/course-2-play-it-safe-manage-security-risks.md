# Course 2: Play It Safe, Manage Security Risks

## Module 1: Security domains and risk
Recap of the 8 CISSP domains, with what each one is about in practice:
- **Security and risk management:** goals, risk mitigation, compliance, business continuity, legal issues.
- **Asset security:** protecting physical and digital assets, data storage and disposal.
- **Security architecture and engineering:** tools and processes for securing systems (e.g. SIEM). Principles like least privilege and defense in depth.
- **Communication and network security:** securing physical networks and wireless communication.
- **IAM:** keeping data safe by controlling who has access. Identification, authentication, authorization, accountability.
- **Security assessment and testing:** audits, penetration tests, vulnerability assessments.
- **Security operations:** investigations, incident response, preventive measures.
- **Software development security:** secure coding practices across the SDLC.

Risk terminology:
- **Threat:** anything that can harm an asset.
- **Risk:** anything that can impact the CIA of an asset. Risk = likelihood × impact.
- **Vulnerability:** a weakness that can be exploited by a threat.
- **Asset:** an item that has value for the organization.

Risk levels: **low** (minor effect), **medium** (some impact on finances, reputation), **high** (serious effect on operations, finances or reputation).

Ransomware, SQL injection and phishing as typical threats. **Dark web** = part of the internet that requires special tools to access.

## Module 2: Frameworks and controls
**Security controls**, 3 types:
- **Administrative/managerial:** policies and procedures (e.g. least privilege, separation of duties).
- **Technical:** technology solutions (firewall, IDS, encryption, antivirus).
- **Physical:** locks, CCTV, fire detection.

Control purposes: **preventative, corrective, detective, deterrent**.

Frameworks and regulations to remember:
- **NIST CSF** (voluntary, 5 functions) and **NIST RMF** (7 steps: Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor).
- **NIST SP 800-53:** controls for federal information systems.
- **CTF (Cyber Threat Framework):** common language for describing threat activity.
- **ISO/IEC 27001:** international standard for managing information security.
- **GDPR:** EU data protection. Breach must be reported within **72 hours**.
- **PCI DSS:** protection of credit card data.
- **HIPAA:** US health data.
- **SOC 1 / SOC 2:** audits of an organization's controls (financial reporting / user access, confidentiality, integrity, availability).
- **FERPA, FedRAMP, SOX, CIS controls** etc.

**OWASP security principles:**
- Minimize attack surface area
- Principle of least privilege
- Defense in depth
- Separation of duties
- Keep security simple
- Fix security issues correctly

**Security audit** = review of the organization's controls, policies and procedures against a set of expectations.
Steps: define scope and goals → complete a risk assessment → controls assessment → assess compliance → communicate results. (This is my Botium Toys project.)

## Module 3: Security tools
- **Logs and SIEM dashboards** help analysts see what is happening in real time.
- SIEM types: **self hosted**, **cloud hosted**, **hybrid**.
- **Splunk Enterprise** (self hosted), **Splunk Cloud**, **Chronicle** (cloud native, Google).
- Other tools: **SOAR** (automates responses), open source tools like **Suricata**, **Zeek**, **MISP**.

## Module 4: Playbooks and incident response
- **Playbook** = a manual with the steps to respond to a specific incident.
- Incident response lifecycle (NIST):
  1. **Preparation**
  2. **Detection and analysis**
  3. **Containment, eradication and recovery**
  4. **Post-incident activity** (lessons learned, reports)
- SIEM + playbook work together: SIEM gives the alert, the playbook tells the analyst what to do.
- Playbooks must be updated after every incident or when new threats appear.
