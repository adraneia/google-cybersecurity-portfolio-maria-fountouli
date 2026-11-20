# Security Incident Report: Brute Force Attack and Malicious Redirect

**Course 3: Connect and Protect, Networks and Network Security**

**Skills:** DNS and HTTP traffic analysis (tcpdump), brute force attacks, malware redirection, remediation

## Scenario
Visitors to a recipe website were asked to download a file, and after running it their computers slowed down and their browsers were sent to a fake site. I analysed the tcpdump log captured in a sandbox and documented what happened.

## Section 1: Network protocol involved
The incident involved several network protocols. First, the browser used the DNS protocol to request the IP address of the website. After receiving the correct DNS response, the browser used the HTTP protocol to load the webpage and download the malicious file. DNS was also used again when the malware redirected the browser to the fake website, followed by another HTTP request to load the malicious webpage.

## Section 2: Documenting the incident
A former employee gained unauthorized access to the web host by performing a brute force attack against the administrative account, successfully guessing the default password. After logging in, the attacker modified the website's source code by inserting malicious JavaScript that prompted visitors to download an executable file. When users downloaded and ran the file, their browsers were silently redirected to a fake website, greatrecipesforme.com, which contained malware.

Multiple customers reported that the legitimate website was prompting them to download a file and that their computers slowed down after running it. During analysis in a sandbox environment, the browser first performed a DNS request for yummyrecipesforme.com, received the correct IP address, and loaded the webpage using HTTP. The malicious script triggered the download of the executable, which then caused the browser to perform another DNS request for greatrecipesforme.com and load the fake, malicious site via HTTP.

A senior analyst confirmed that the web server had been compromised and that the attacker altered the source code. The root cause of the incident was the lack of password security controls and the use of a default administrative password, which allowed the brute force attack to succeed.

## Section 3: Remediation for brute force attacks
One security measure the team plans to implement to protect against brute force attacks is to disallow previous passwords from being used. Since the vulnerability that led to this attack was the attacker's ability to use a default password to log in, it's important that we prevent any old passwords such as default passwords from being used to reset the password. Another supportive measure is to require more frequent password updates, so in case any unauthorized person becomes aware of the password, they are less likely to be able to use it. Finally, another helpful solution is to implement two-factor authentication (2FA). 2FA requires authentication via a password and also by confirming a one-time passcode (OTP) sent to either email or phone. Any malicious actor that attempts a brute force attack will not likely gain access to the system because it requires additional authentication.
