# SOC Alert Ticket: Phishing Email with Malicious Attachment

**Course 6: Sound the Alarm, Detection and Response**

**Skills:** alert triage, phishing analysis, file hash verification, escalation (SOC Level 1)

## Scenario
As a level one SOC analyst I received an alert about a suspicious file downloaded on an employee's computer. I followed the phishing playbook, checked the attachment's hash and decided whether to escalate the ticket.

| Ticket ID | Alert message | Severity | Details | Ticket status |
|---|---|---|---|---|
| A-2703 | SERVER-MAIL Phishing attempt possible download of malware | Medium | The user may have opened a malicious email and opened attachments or clicked links. | **Escalated** |

## Ticket comments
The alert detected that an employee downloaded and opened a malicious file from a phishing email. There is an inconsistency between the sender's email address "76tguy6hh6tgftrt7tg.su", the name used in the email body "Clyde West", and the sender's name, "Def Communications". The email body and subject line contained grammatical errors. The email's body also contained a password protected attachment, "bfsvc.exe", which was downloaded and opened on the affected machine. Having previously investigated the file hash, it is confirmed to be a known malicious file. Furthermore, the alert severity is reported as medium. With these findings, I chose to escalate this ticket to a level two SOC analyst to take further action.

## Additional information
**Known malicious file hash (SHA256):** `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`

```
From: Def Communications <76tguyhh6tgftrt7tg.su> <114.114.114.114>
Sent: Wednesday, July 20, 2022 09:30:14 AM
To: <hr@inergy.com> <176.157.125.93>
Subject: Re: Infrastructure Egnieer role
Attachment: filename="bfsvc.exe"
```
