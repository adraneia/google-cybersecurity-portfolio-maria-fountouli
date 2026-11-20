# Threat Intelligence: File Hash Investigation with VirusTotal

**Course 6: Sound the Alarm, Detection and Response**

**Skills:** VirusTotal, indicators of compromise (IoCs), Pyramid of Pain, threat intelligence

## Scenario
I investigated a suspicious file hash with VirusTotal, decided whether it was malicious, and mapped the indicators of compromise I found to the levels of the Pyramid of Pain.

## Has this file hash been reported as malicious?
Yes. The file hash has been reported as malicious by over 50 vendors. Upon further investigation, this file hash is known as the malware **Flagpro**, which has been commonly used by the advanced threat actor **BlackTech**.

## Indicators of compromise (Pyramid of Pain)

| Level | IoC found |
|---|---|
| TTPs | Command and Control |
| Tools | Input capture |
| Network/host artifacts | HTTP requests |
| Domain names | `org.misecure.com` |
| IP addresses | `207.148.109.242` |
| Hash values | `287d612e29b71c90aa54947313810a25` |
