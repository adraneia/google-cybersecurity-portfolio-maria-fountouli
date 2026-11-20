# Course 5: Assets, Threats, and Vulnerabilities

## Module 1: Introduction to asset security
- **Asset inventory** = list of all assets so you know what to protect.
- **Asset classification:** **public**, **internal-only**, **confidential**, **restricted**.
- Data states: **in use**, **in transit**, **at rest**.
- **Information security (InfoSec)** policies and **data custodians/owners**.
- Cloud security: shared responsibility, identity access management, configuration, **cloud security posture management (CSPM)**.
- **Security plans** have 3 parts: **policies** (rules), **standards** (references for implementation), **procedures** (step by step).
- **NIST CSF** components: **core**, **tiers** (level 1 to 4 maturity), **profiles**.

## Module 2: Protecting assets
**Safeguards:**
- **Cryptography:** turns plaintext into ciphertext.
  - **Symmetric** = one key for both (e.g. **AES**, 3DES). Fast.
  - **Asymmetric** = public + private key (e.g. **RSA**). Used for key exchange.
  - **PKI** = digital certificates from Certificate Authorities. HTTPS uses TLS.
- **Hashing:** one way function. **MD5** (weak, collisions), **SHA-256**. Used for integrity and passwords. **Salting** prevents rainbow table attacks.
- Non-repudiation, digital signatures.

**Access controls / IAM:**
- **AAA framework:** **Authentication**, **Authorization**, **Accounting**.
- Authentication factors: something you **know**, something you **have**, something you **are**.
- **SSO** (single sign on), **MFA**.
- Authorization: **least privilege**, **separation of duties**.
- **HTTP basic auth** vs **OAuth** (tokens, API keys).
- Access control models: **MAC** (mandatory), **DAC** (discretionary), **RBAC** (role based).
- **User provisioning**: creating and maintaining users' access.

## Module 3: Vulnerabilities
- **Exploit** = a way to take advantage of a vulnerability.
- **Defense in depth**, 5 layers: **perimeter**, **network**, **endpoint**, **application**, **data**.
- **CVE list** (Common Vulnerabilities and Exposures) and **CVSS** score (0 to 10).
- **OWASP Top 10**: broken access control, cryptographic failures, injection, insecure design, security misconfiguration, vulnerable components, auth failures, software and data integrity failures, logging failures, SSRF.
- **Vulnerability assessment:** identification → analysis → risk assessment → remediation.
- Scanners: **external vs internal**, **authenticated vs unauthenticated**, **limited vs comprehensive**.
- **Attack surface:** physical and digital. **Attack vectors** = paths into a system (e.g. USB, email, weak passwords).
- Threat actor approach: understand the attacker's mindset.

## Module 4: Threats
- **Social engineering** stages: prepare → establish trust → use persuasion → disconnect. Types: baiting, phishing, quid pro quo, tailgating, watering hole, smishing, vishing.
- **Malware:** virus, worm, trojan, adware, spyware, scareware, fileless malware, rootkit, botnet, ransomware, cryptojacking.
- **Web based exploits:**
  - **XSS** (cross site scripting): reflected, stored, DOM based.
  - **SQL injection:** in-band, out-of-band, inferential. Prevented with **prepared statements**, input sanitization, input validation.
- **Threat modeling:** define scope → identify threats → characterize environment → analyse threats → mitigate risks → evaluate findings.
  - Frameworks: **STRIDE**, **PASTA** (7 stages), **Trike**, **VAST**.
