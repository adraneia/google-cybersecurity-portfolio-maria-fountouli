# Course 1: Foundations of Cybersecurity

## Module 1: What is cybersecurity
- **Cybersecurity** = protecting networks, devices, people and data from unauthorized access or criminal exploitation, so that information stays **confidential, intact and available**.
- **Threat actor** = any person or group that poses a security risk.
- Threats can be **external** (outside the org) or **internal** (employees, ex-employees, vendors, partners). Internal ones are often accidental, e.g. clicking a malicious link.
- Why security matters for a company:
  - protection from internal and external threats
  - **compliance** with laws and regulations, avoiding fines and audits
  - business continuity and productivity
  - customer trust
- Entry level roles: security analyst, SOC analyst, IT security analyst, security operations specialist.
- **Transferable skills:** communication, collaboration, analysis, problem solving.
- **Technical skills:** programming (Python, SQL), SIEM tools, intrusion detection, computer forensics.

## Module 2: Evolution of cybersecurity
Important attacks in history:
- **Brain virus (1986):** first PC virus, spread through floppy disks, mostly slowed down computers. Showed how easily malware spreads.
- **Morris worm (1988):** meant to measure the size of the internet, but a bug made it copy itself again and again, and about 6,000 computers crashed. This led to the creation of **CERTs** (Computer Emergency Response Teams).
- **LoveLetter / ILOVEYOU (2000):** email attachment, stole passwords and sent itself to all contacts. Classic **social engineering**.
- **Equifax breach (2017):** personal data of about 143 million people leaked. Known vulnerabilities were not patched. Huge fines.

Common attack types:
- **Phishing:** fake emails, texts, calls to steal data or install malware. Variants: business email compromise (BEC), spear phishing, whaling, vishing, smishing.
- **Malware:** virus, worm, ransomware, spyware.
- **Social engineering:** social media phishing, watering hole attack, USB baiting, physical attacks.
- **Password attacks:** brute force, rainbow tables.
- **Physical attacks**, **adversarial AI**, **supply chain attacks**, **cryptographic attacks** (birthday, collision, downgrade).

Types of threat actors: APTs (long term, well funded), insider threats, hacktivists, and hackers in general (authorized/ethical, semi-authorized, unauthorized).

**8 CISSP security domains:**
1. Security and risk management
2. Asset security
3. Security architecture and engineering
4. Communication and network security
5. Identity and access management (IAM)
6. Security assessment and testing
7. Security operations
8. Software development security

## Module 3: Frameworks, controls and ethics
- **Framework** = guidelines for building plans to reduce risk (e.g. NIST CSF).
- **Controls** = safeguards that reduce specific risks (e.g. password policy, MFA).
- **CIA triad:**
  - **Confidentiality:** only authorized users access the data.
  - **Integrity:** data is correct, authentic, reliable.
  - **Availability:** data is accessible to those who are authorized.
- **NIST CSF**, 5 core functions: **Identify, Protect, Detect, Respond, Recover**.
- **Ethics in security:** confidentiality, privacy protections, following laws. Counterattacks (hack back) are illegal for private persons and companies.

## Module 4: Tools and programming languages
- **Logs:** records of events (firewall logs, network logs, server logs).
- **SIEM** = collects and analyses logs in real time, gives alerts and dashboards.
  - **Splunk Enterprise / Splunk Cloud**
  - **Google SecOps (Chronicle):** cloud native SIEM
- **Playbooks:** step by step manual for how to respond to an incident.
- **Network protocol analyzers (packet sniffers):** tcpdump, Wireshark.
- **Programming:** Python for automation, SQL for querying databases, Linux as an operating system.
