# Incident Report: TCP SYN Flood (DoS)

**Course 3: Connect and Protect, Networks and Network Security**

**Skills:** TCP three-way handshake, log analysis, DoS/DDoS attacks, incident documentation

## Scenario
A company website started returning connection timeout errors. I reviewed the network logs from a packet analyzer to work out what kind of attack was taking place and how it was breaking the website.

## Section 1: Type of attack
One potential explanation for the website's connection timeout error message is a DoS attack.

The logs show that there were numerous TCP SYN requests coming from an unfamiliar IP address, suggesting that the server was receiving an excessive amount of connection attempts without completing the handshake process.

This event could be a TCP SYN flood attack, which is a type of Denial of Service (DoS) attack designed to exhaust server resources and disrupt normal access to the website.

## Section 2: How the attack causes the website to malfunction
When website visitors try to establish a connection with the web server, a three-way handshake occurs using the TCP protocol. The three steps are:

1. **SYN:** The client sends a SYN packet to the server to request a connection.
2. **SYN-ACK:** The server responds with a SYN-ACK packet to acknowledge the request.
3. **ACK:** The client sends an ACK packet back to the server, and the connection is successfully established.

During a SYN flood attack, a malicious actor sends a large number of SYN packets rapidly, causing the server to reserve resources for each incomplete connection. As a result, there are no resources left to handle legitimate TCP requests.

The logs show an unusually high volume of SYN packets without follow-up ACK responses. This overloads the server and prevents it from establishing new connections, leading to connection timeout errors for legitimate users.
