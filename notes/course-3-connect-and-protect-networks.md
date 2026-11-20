# Course 3: Connect and Protect, Networks and Network Security

## Module 1: Network architecture
- **Network** = group of connected devices. **LAN** (small area) vs **WAN** (large area, e.g. the internet).
- Devices: **hub** (sends to all devices), **switch** (sends only to the right device, uses MAC addresses), **router** (connects networks, uses IP addresses), **modem** (connects router to the internet), **wireless access point**.
- **Cloud computing**: IaaS, PaaS, SaaS. **SDN** = software defined networks.
- **Data packet** = header (IP addresses, MAC, protocol), body (data), footer.
- **TCP/IP model**, 4 layers:
  1. Network access (physical, MAC, ARP)
  2. Internet (IP, ICMP)
  3. Transport (TCP, UDP)
  4. Application (HTTP, DNS, SMTP, SSH...)
- **OSI model**, 7 layers: Physical, Data link, Network, Transport, Session, Presentation, Application.
- **IPv4** = 32 bits (e.g. 192.168.1.1). **IPv6** = 128 bits, hexadecimal.
- **MAC address** = unique hardware address of a network card.
- Public vs private IP addresses.

## Module 2: Network operations
- **Protocols** in 3 categories:
  - **Communication:** TCP, UDP, HTTP, DNS
  - **Management:** SNMP, ICMP
  - **Security:** HTTPS, SFTP
- Ports to remember: **22** SSH, **25** SMTP, **53** DNS, **80** HTTP, **443** HTTPS, **3389** RDP.
- **TCP** = connection oriented, three-way handshake **SYN → SYN-ACK → ACK**. **UDP** = connectionless, faster, no guarantee.
- **ARP** = finds the MAC address for an IP. **DHCP** = assigns IP addresses automatically.
- **Wi-Fi security:** WEP (old, insecure) → WPA → WPA2 → **WPA3**.
- **Firewall:** filters traffic based on rules. Types: hardware, software, cloud. **Stateful** (remembers connections) vs **stateless**. **NGFW** = next generation firewall with deep packet inspection.
- **VPN** = encrypts traffic and hides IP (encapsulation). Protocols: **WireGuard**, **IPSec**.
- **Security zones:** uncontrolled zone (internet), controlled zone with **DMZ**, internal network, restricted zone.
- **Proxy servers:** forward proxy (users → internet), reverse proxy (internet → internal servers).

## Module 3: Network attacks
- **DoS** = floods a server so it stops working. **DDoS** = from many devices at once.
  - **SYN flood:** many SYN packets, the handshake never completes, the server runs out of resources.
  - **ICMP flood:** many ICMP packets overload the network.
  - **Ping of death:** ICMP packet bigger than 64KB crashes the system.
- **Packet sniffing:** capturing packets (passive = just reading, active = changing them).
- **IP spoofing:** pretending to be a trusted IP.
  - **On-path attack** (man in the middle)
  - **Replay attack**
  - **Smurf attack** (ICMP + spoofing)
- **tcpdump** = command line packet analyzer. I used it to analyse DNS/ICMP traffic (see project 03).

## Module 4: Security hardening
- **Security hardening** = reducing vulnerabilities and attack surface.
- **OS hardening:** patch updates, baseline configurations, removing unused software, strong passwords, MFA.
- **Network hardening:** port filtering, firewall rules, network segmentation, encryption, network log analysis, keeping network access list up to date.
- **Penetration test** = simulated attack to find weaknesses.
- **Cloud hardening:** shared responsibility model, IAM, misconfiguration risks, hypervisors, baselines.
- **Brute force attacks** and how to prevent them: salting and hashing, MFA/2FA, CAPTCHA, password policies. Tools to test: virtual machines, sandboxes.
