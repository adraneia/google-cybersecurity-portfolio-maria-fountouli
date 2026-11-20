# Network Traffic Analysis: DNS and ICMP (tcpdump)

**Course 3: Connect and Protect, Networks and Network Security**

**Skills:** tcpdump, DNS, UDP, ICMP, network troubleshooting

## Scenario
Customers reported that they could not reach the website www.yummyrecipesforme.com and got a "destination port unreachable" error. I analysed a tcpdump capture of the DNS queries to find the cause.

## Part 1: Summary of the problem found in the DNS and ICMP traffic log
- The computer attempted to send DNS queries using UDP to port 53 on the DNS server to resolve the domain name yummyrecipesforme.com.
- The ICMP reply returned the error message **"udp port 53 unreachable"**, indicating that the DNS request could not be delivered.
- Port 53 is used for DNS services, which resolve domain names into IP addresses.
- **Most likely issue:** the DNS server was not listening on port 53 or the DNS service was unavailable, preventing proper name resolution and causing the website to fail to load.

## Part 2: Analysis of the data and likely cause
**Time incident occurred:** The first failed DNS request occurred at 13:24:32, followed by repeated failed attempts at 13:26:32 and 13:28:32.

**How the IT team became aware of the incident:** Customers reported being unable to access www.yummyrecipesforme.com, receiving the error "destination port unreachable."

**Actions taken to investigate:** The IT department attempted to reproduce the issue and used a network analyzer (tcpdump) to capture network traffic during the DNS query process.

**Key findings:**
- DNS requests were sent over UDP to port 53 on the DNS server IP 203.0.113.2.
- The DNS server responded using ICMP with the error message "udp port 53 unreachable."
- No DNS response was received, so the domain could not be resolved.

**Likely cause:** The DNS service on the server was likely not running or misconfigured, or port 53 was blocked or unavailable, preventing proper resolution of the website's domain name.
