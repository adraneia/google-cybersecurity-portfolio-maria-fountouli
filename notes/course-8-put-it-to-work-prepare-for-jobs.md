# Course 8: Put It to Work, Prepare for Cybersecurity Jobs

## Module 1: Protect data and communicate incidents
- Security mindset = always thinking about what could go wrong and what assets need protection.
- Assets the analyst protects: **PII**, **SPII**, financial data, intellectual property, network infrastructure.
- Important to understand that decisions should be based on the **impact** to the business.
- Low level incidents (e.g. one employee's phishing email) vs high level incidents (e.g. data breach, ransomware).

## Module 2: Escalate incidents
- **Escalation** = passing an incident to a higher level when it is beyond your role.
- Incident classification:
  - **Malware infection**
  - **Unauthorized access**
  - **Improper usage**
- Small issues can become huge problems if they are ignored. When in doubt, escalate.
- Know the **escalation policy** of your organization: who to contact, when, and how.

## Module 3: Communicate effectively with stakeholders
- **Stakeholders:** e.g. CISO, operations manager, risk manager, legal, HR.
- Communication should be **short and clear**, with the most important information first. Visuals (charts, dashboards) help a lot.
- Choose the right channel: email, call, meeting, chat.
- Explain the risk and the impact, not only the technical details.

## Module 4: Engage with the cybersecurity community
- Join security organizations, follow security news (CISA, Krebs on Security, etc.), go to conferences and meetups.
- Organizations: **ISC2**, **ISACA**, **OWASP**, **Women in CyberSecurity (WiCyS)**, **CSA (Cloud Security Alliance)**.
- LinkedIn and GitHub to show your work. This repository is part of that.

## Module 5: Use AI in security work
- AI can help with: summarizing logs, explaining unfamiliar code, writing scripts and queries, drafting reports.
- Always **check the output** and don't paste sensitive data (PII, credentials) into AI tools.

## Extra notes
**Common network protocols and ports**

| Protocol | Port | Use |
|---|---|---|
| HTTP | 80 | web traffic, not encrypted |
| HTTPS | 443 | web traffic with TLS |
| DNS | 53 | domain name → IP address |
| SSH | 22 | secure remote access |
| FTP | 20/21 | file transfer |
| SMTP | 25 | sending email |
| DHCP | 67/68 | assigns IP addresses |
| RDP | 3389 | Windows remote desktop |

**How DNS works:** browser asks the **resolver** → resolver asks the **root server** → root sends it to the **TLD server** (.com) → TLD sends it to the **authoritative name server** → the IP address goes back to the browser, which connects to the website.
