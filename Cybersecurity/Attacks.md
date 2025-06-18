# Common Cyber Attacks and Mitigation Methods

Cyber attacks are deliberate attempts to disrupt, damage, or gain unauthorized access to information systems, networks, or data. Understanding the different types of cyber attacks is essential to designing robust security strategies. Below is an overview of some of the most common and impactful cyber attack types.

---

## 1. Denial of Service (DoS)

A **DoS attack** overwhelms a system, server, or network with excessive requests, rendering it unavailable to legitimate users.

- **Goal:** Disruption of service availability.
- **Example:** Sending rapid requests to a website until the server crashes.

### Mitigation:

- Rate limiting
- Resource quotas
- Firewall filtering

---

## 2. Distributed Denial of Service (DDoS)

A **DDoS attack** is a more advanced form of DoS where multiple systems (often compromised and forming a botnet) flood the target with traffic.

- **Goal:** Large-scale disruption using multiple attack sources.
- **Example:** Botnets like Mirai flooding DNS servers.

### Mitigation:

- DDoS protection services (e.g., Cloudflare, AWS Shield)
- Traffic analysis and geo-blocking
- Anycast networks for load distribution

---

## 3. Brute Force Attacks

Brute force attacks involve systematically trying every possible password or credential combination until the correct one is found.

- **Goal:** Unauthorized access to accounts or systems.
- **Example:** Password cracking via SSH using a wordlist.

### Mitigation:

- Multi-Factor Authentication (MFA)
- Account lockout policies
- Use of CAPTCHA and login throttling

---

## 4. SQL Injection (SQLi)

An **SQL injection** attack occurs when an attacker injects malicious SQL code into an input field to manipulate a database query.

- **Goal:** Extract, modify, or delete database content.
- **Example:** Typing `' OR '1'='1` into a login form to bypass authentication.

### Mitigation:

- Prepared statements / parameterized queries
- Input validation and sanitization
- Web Application Firewalls (WAF)

---

## 5. Man-in-the-Middle (MitM)

In a **MitM attack**, the attacker intercepts and possibly alters communications between two parties without their knowledge.

- **Goal:** Eavesdropping, data theft, or manipulation.
- **Example:** Hijacking unencrypted Wi-Fi traffic to steal login credentials.

### Mitigation:

- End-to-end encryption (e.g., HTTPS, TLS)
- VPN usage on public networks
- Certificate pinning and strong DNS security

---

## 6. Phishing

Phishing is a type of social engineering attack where attackers impersonate legitimate sources to trick users into revealing sensitive information.

- **Goal:** Steal credentials, financial info, or distribute malware.
- **Example:** A fake login page mimicking a bank’s website.

### Mitigation:

- Security awareness training
- Email filtering and link scanning
- MFA to reduce impact

---

## 7. Cross-Site Scripting (XSS)

In **XSS attacks**, attackers inject malicious scripts into web pages viewed by others, often to steal session cookies or redirect users.

- **Goal:** Session hijacking, defacement, or data theft.
- **Example:** Inserting `<script>` tags into comment sections.

### Mitigation:

- Output encoding
- Content Security Policy (CSP)
- Input validation

---

## 8. Credential Stuffing

This attack uses previously leaked username-password pairs to attempt logins on other services, assuming users reuse credentials.

- **Goal:** Account takeover.
- **Example:** Using credentials leaked from a social media breach to access email accounts.

### Mitigation:

- MFA
- Login attempt monitoring
- User education on unique passwords

---

## 9. Zero-Day Exploits

These attacks exploit vulnerabilities that are unknown to vendors and have no available patches at the time of attack.

- **Goal:** Full compromise of a system before detection.
- **Example:** Exploiting a flaw in a browser before it's patched.

### Mitigation:

- Network monitoring and anomaly detection
- Behavioral analytics
- Patch management and threat intelligence

---