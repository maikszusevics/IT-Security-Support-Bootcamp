# System and Network Hardening

**Hardening** is the process of securing systems by reducing their vulnerability to threats. It involves modifying default configurations, disabling unnecessary components, and implementing controls to prevent unauthorised access or misuse. The goal is to reduce the system's "attack surface",the total number of ways it can be exploited,thereby improving its resilience against cyberattacks.

---

## Operating System (OS) Hardening

Operating System hardening secures the foundation of a computer system by locking down features and tightening access. The following methods help prevent attackers from exploiting weaknesses in the system:

- **Disable Unnecessary Services and Features**  
  Operating systems often come with many services enabled by default. Disabling unused services (e.g., Bluetooth, Print Spooler, or legacy network protocols) reduces the number of potential entry points that an attacker could target.

- **Apply Security Patches and Updates Regularly**  
  Vulnerabilities in the OS are frequently discovered and exploited. Keeping systems patched ensures known exploits are closed, particularly those that allow privilege escalation or remote code execution.

- **Enforce Strong Authentication and Password Policies**  
  Requiring complex passwords, enforcing regular password changes, and setting account lockout thresholds prevents brute-force attacks and limits unauthorised access attempts.

- **Configure File and Directory Permissions**  
  Misconfigured permissions can allow users or malware to access sensitive data or system files. Enforcing least privilege ensures users and applications can only access what they need, reducing the damage from compromised accounts.

- **Use Host-Based Firewalls**  
  A host-based firewall restricts incoming and outgoing traffic at the system level. It helps block unauthorised communication even if the network is compromised, isolating the machine from malicious connections.

- **Enable Security Logging and Auditing**  
  Logging allows you to detect unusual behaviour, identify failed login attempts, and trace the actions of a compromised account. This helps with incident response and forensic analysis.

- **Implement Antivirus/Endpoint Protection**  
  These tools detect and quarantine malicious files, monitor processes, and prevent malware from running. They add a critical layer of defence against threats that might bypass other controls.

---

## Network Hardening

Network hardening protects the pathways that connect systems. It focuses on securing the flow of data and limiting unauthorised access through exposed protocols or misconfigurations.

- **Segment Networks and Use VLANs**  
  By isolating critical systems into separate network segments (e.g., guest vs. internal vs. management), you limit lateral movement. If one segment is breached, attackers can't easily access other areas.

- **Deploy Firewalls and Intrusion Detection/Prevention Systems (IDS/IPS)**  
  Firewalls control traffic between network zones based on rules, blocking unauthorised access attempts. IDS/IPS systems monitor traffic for known attack patterns and can alert or actively block suspicious behaviour in real-time.

- **Disable Unused Network Protocols and Services**  
  Protocols like Telnet, NetBIOS, or SMBv1 are often insecure or outdated. Disabling them removes unnecessary services that could be exploited, especially if they transmit data unencrypted.

- **Use Secure Communication Protocols**  
  Replacing insecure protocols (like HTTP or FTP) with their encrypted alternatives (HTTPS, SFTP, SSH) ensures data in transit is not exposed to sniffing, tampering, or man-in-the-middle attacks.

- **Restrict Remote Access**  
  By limiting remote access to trusted IP ranges, using multi-factor authentication (MFA), and securing remote management portals, you significantly reduce the risk of unauthorised entry, especially from the internet.

- **Implement Network Access Control (NAC)**  
  NAC solutions verify device compliance (e.g., up-to-date antivirus, proper configuration) before granting access. This stops rogue, unmanaged, or compromised devices from connecting to internal networks.

---

## Network Device Hardening

Routers, switches, and firewalls are high-value targets. Hardening these devices protects the infrastructure that enables connectivity and data flow.

- **Change Default Credentials Immediately**  
  Default usernames and passwords are publicly known and commonly exploited. Changing them ensures attackers can't simply log in with factory credentials.

- **Limit Management Interface Access**  
  Restricting access to the device management interface (e.g., CLI, web GUI) to specific IP addresses or networks,and using secure protocols like SSH,prevents unauthorised configuration changes.

- **Disable Unused Ports and Services**  
  Unused ports on switches or services like HTTP/Telnet on routers can be exploited. Disabling them reduces entry points and potential exploits.

- **Keep Firmware Up to Date**  
  Just like OS patching, firmware updates close security holes and fix vulnerabilities in networking hardware, many of which are not patched in the OS layer.

- **Use Secure SNMP Configurations**  
  If SNMP (Simple Network Management Protocol) is used for monitoring, version 3 should be preferred as it includes encryption and authentication. Older versions are vulnerable to sniffing and configuration tampering.

- **Enable Logging and Monitor Logs**  
  Logs from network devices can reveal port scans, failed login attempts, and misconfigurations. Centralised log collection (e.g., via syslog) supports incident detection and auditing.

- **Apply Role-Based Access Control (RBAC)**  
  RBAC limits who can make changes based on job role,e.g., read-only access for monitoring staff and full access for senior engineers,reducing the risk of human error or insider threats.

---

## Summary

System and network hardening is a layered approach to security. By reducing what is exposed, enforcing strict access control, and maintaining vigilance through monitoring, organisations can significantly decrease their risk of compromise. Hardening is not a one-time task,it requires regular review, updates, and adaptation to evolving threats.
