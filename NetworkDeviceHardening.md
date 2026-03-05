# Network Hardening Notes

---

## Common Threat and Attack Vectors

**Notes**
- Network devices manage the network, while endpoint devices simply interact with it.

**Questions**
- Both questions are fill-in-the-blank and are straightforward based on the reading.

---

## Common Hardening Techniques

**Notes**

Hardening techniques include:
- Updating and patching systems regularly
- Disabling unnecessary ports and services
- Applying the principle of least privilege and monitoring logs
- Maintaining backups, enforcing strong password policies, and enabling MFA

Ensure the use of secure protocols such as HTTPS, SSH, SSL/TLS, and IPsec. Remove or replace insecure protocols, including FTP, HTTP, Telnet, and SMTP. Configure or remove inherently insecure protocols such as LDAP and RDP.

**Logging Controls**
- **Syslog** — Standardizes log messages
- **SNMP** — Sends notifications from network devices to management systems
- **NetFlow** — Analyzes network traffic patterns
- **Packet Capture** — Captures network traffic for analysis (e.g., Wireshark)

**Questions**
- FTP is an insecure protocol.
- Syslog sends log messages.

---

## Hardening Virtual Private Networks

**Notes**
- Following the first step is sufficient to find both flags and the port number needed to answer all questions in this room; however, the remaining steps are worth reviewing regardless.

---

## Hardening Switches, Routers, and Firewalls

**Notes**
- OpenWRT is a free, open-source OS for IoT devices.
- Log in via the web interface using the provided credentials.
- Always fill in all device details, as this aids with logging.
- Always change default credentials.
- Enable secure network protocols.
- Disable unnecessary scripts.

**Questions**
- The first two answers are found by walking through the steps outlined in the notes section.
- The flag is located in the specified settings.
- The next answer is found in the log settings.
- The last answer is found in the startup scripts settings.

---

## More Techniques

**Notes**
- Manage traffic rules carefully, especially when blocking known malicious IPs.
- Monitor traffic through graphs to identify anomalies.
- Configure port forwarding with caution, as it exposes internal devices to the public.
- Oversee scheduled tasks to ensure no unauthorized activity is occurring.
- Always keep firmware up to date.

**Questions**
- For the first question, check the firewall rules — locate `Allow-Ping`.
- For the second question, check the forwarding rules — locate `THM_PORT`.
- For the last question, navigate to the software section and find the version number for the APK.

---

## Network Monitoring Tools

**Notes**
- **Nagios** — Monitors systems, networks, and infrastructure
- **PRTG** — All-in-one network monitoring solution
- **Zabbix** — Open-source alternative to PRTG

**Questions**
- No notable questions for this section.
