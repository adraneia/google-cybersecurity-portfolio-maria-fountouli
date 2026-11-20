# Course 6: Sound the Alarm, Detection and Response

## Module 1: Introduction to detection and incident response
- **Incident** = event that harms or threatens the CIA of information. Every incident is an event, not every event is an incident.
- **NIST incident response lifecycle:** Preparation → Detection and Analysis → Containment, Eradication and Recovery → Post-incident activity. It's a cycle, not a straight line.
- **CSIRT** (computer security incident response team) roles: security analyst, technical lead, incident coordinator. **SOC** tiers: L1 (triage), L2 (investigation), L3 (threat hunting), SOC lead, SOC manager.
- **Incident response plan** = procedures, system info, contact lists.
- Tools: **documentation** (playbooks, incident handler's journal), **detection** (IDS, IPS), **EDR**, **SIEM**, **SOAR**.
- **IDS** = alerts on suspicious activity. **IPS** = also blocks it.

## Module 2: Network monitoring and analysis
- Know what **normal** looks like (baseline), so you can spot abnormal traffic.
- **Data exfiltration**: unauthorized transfer of data out of the organization.
- **Indicators of compromise (IoC)** vs **indicators of attack (IoA)**.
- **Packet capture (pcap)** with **tcpdump** and **Wireshark**.
- tcpdump basics:
```bash
sudo tcpdump -i eth0 -v -c 5          # 5 packets, verbose
sudo tcpdump -i eth0 port 80 -w capture.pcap
sudo tcpdump -r capture.pcap -nn      # read file, no name resolution
```
- Header fields to read: source/destination IP, ports, TTL, flags, protocol.

## Module 3: Incident investigation and response
- **Detection and analysis:**
  - **Threat hunting**, **threat intelligence** (IoCs, TTPs).
  - **Pyramid of Pain**: hash values (easy for the attacker to change) → IP addresses → domain names → network/host artifacts → tools → **TTPs** (hardest). (see project 08)
  - **VirusTotal** for checking file hashes, IPs, URLs.
- **Alert triage:** receive and assess the alert → assign priority → collect and analyse data. Then escalate if needed (project 07).
- **Documentation:** chain of custody, timeline, incident handler's journal.
- **Containment, eradication, recovery**: isolating systems, removing the threat, restoring systems.
- **Post-incident:** lessons learned meeting, final report (executive summary, timeline, investigation, recommendations).

## Module 4: Network traffic and logs with IDS and SIEM
- **Logs:** firewall, network, server logs. Log formats: **Syslog**, **JSON**, **XML**, **CSV**, **CEF**.
- Overlogging is a problem too: too much noise, more storage.
- **Telemetry** = collection and transmission of data (e.g. packet captures).
- **IDS types:** **host based (HIDS)** and **network based (NIDS)**. Detection methods: **signature based** (known patterns, can't catch new threats) and **anomaly based** (baseline, more false positives).
- **Suricata** = open source IDS/IPS. Rule structure: **action** (alert, drop, pass, reject) + **header** (protocol, IPs, ports, direction) + **rule options** (msg, flow, content, sid, rev).
```
alert http $HOME_NET any -> $EXTERNAL_NET any (msg:"GET on wire"; flow:established,to_server; content:"GET"; http_method; sid:12345; rev:3;)
```
- Output in `eve.json` and `fast.log`.
- **SIEM search:**
  - **Splunk** uses **SPL**: `index=main fail`, wildcards with `*`.
  - **Chronicle** uses **UDM search** and raw log search: `metadata.event_type = "USER_LOGIN"`.
