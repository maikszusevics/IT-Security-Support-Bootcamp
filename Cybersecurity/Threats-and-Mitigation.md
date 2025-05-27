# Cybersecurity Threats and Mitigation Strategies

In cybersecurity, a **threat** is any potential danger that could exploit a vulnerability and cause harm to systems, data, or operations.

**Mitigation** refers to **reducing the risk** by lowering either the _**impact**_ or _**likelihood**_ of a threat occurring. It is a core component of risk management and forms the basis of a proactive security posture.

---

## Types of Threats
> Not all threats are created equal, and no single control can prevent everything.  
> Motivations and capabilities vary widely between threat actors.  
> A layered security approach, _defence in depth_, is essential for robust protection.

### Script Kiddies

- Typically amateurs with little understanding of how attacks work.
- Use pre-written scripts or automated tools obtained from the internet.
- Often act for thrill, boredom, reputation in online communities, or to "test" skills.
    
- **Threat Level:** Low to Medium  
    _(low sophistication, but can cause significant damage if undetected)_

### Hacktivists

- Ideologically or politically motivated attackers.
- Target organisations they perceive as unethical or oppressive.
- Use DDoS attacks, website defacements, and data leaks to further their cause.
    
- **Threat Level:** Medium  
    _(motivated and focused, but typically not well-resourced)_

### Organised Crime

- Structured groups with a clear hierarchy and financial motivations.
- Engage in ransomware, fraud, data theft, money laundering, and extortion.
- Operate professionally with advanced tactics (e.g., phishing, malware-as-a-service).
    
- **Threat Level:** High  
    _(well-funded, persistent, adaptable)_

### Nation-State Actors / Advanced Persistent Threats (APTs)

- Sponsored and directed by governments to achieve strategic objectives.
- Target critical infrastructure, research institutions, or corporations.
- Highly skilled and resource-intensive, with long-term goals and stealth tactics.
- Use zero-day exploits, custom malware, and extensive reconnaissance.
    
- **Threat Level:** Critical  
    _(highly persistent, extremely sophisticated, high impact)_

### Insider Threats

- Can be current or former employees, contractors, or trusted partners.
- Motivations include revenge, coercion, financial gain, or negligence.
- May have legitimate access and intimate system knowledge.
    
- **Threat Level:** Medium to High  
    _(difficult to detect, highly context-dependent)_

### Competitors (Industrial Espionage)

- Involve corporate actors seeking market advantage.
- Engage in theft of intellectual property, sabotage, or intelligence gathering.
- May use insiders, social engineering, or third-party vulnerabilities.
    
- **Threat Level:** Medium to High  
    _(depends on industry and value of proprietary data)_

---

## Mitigation Strategies per Threat Type

Security mitigation involves a combination of **preventive**, **detective**, and **responsive** controls. Below is a breakdown of recommended mitigations for each threat type:

### Script Kiddies
**Mitigation Tactics:**

- Harden systems by disabling unnecessary services and ports.
- Regularly update and patch operating systems and applications.
- Implement basic firewall rules and endpoint protection.
- Use rate limiting and automated IP blocking for brute-force protection.
- Conduct routine vulnerability assessments.
### Hacktivists
**Mitigation Tactics:**

- Use Web Application Firewalls (WAFs) to filter traffic and block malicious payloads.
- Employ DDoS protection services (e.g., Cloudflare, Akamai).
- Monitor social media and open-source intelligence (OSINT) for indicators of activism.
- Implement incident response plans for quick takedown and recovery.

### Organised Crime
**Mitigation Tactics:**

- Employ strong anti-malware and EDR (Endpoint Detection and Response) solutions.
- Enforce multi-factor authentication (MFA) across all systems.
- Conduct phishing simulations and user training.
- Back up data regularly and test recovery procedures (to combat ransomware).
- Implement robust Identity and Access Management (IAM) policies.

### Nation States / APTs

**Mitigation Tactics:**

- Segment networks and restrict lateral movement using Zero Trust principles.
- Deploy advanced threat detection platforms (e.g., SIEM, XDR).
- Monitor logs for unusual behaviour (e.g., exfiltration patterns, persistence mechanisms).
- Collaborate with government cybersecurity agencies (e.g., NCSC, CISA).
- Perform regular red team exercises and threat hunting activities.

### Insider Threats

**Mitigation Tactics:**

- Apply the principle of least privilege to limit access.
- Use Data Loss Prevention (DLP) and User and Entity Behaviour Analytics (UEBA).
- Monitor file transfers, print jobs, and email activity for anomalies.
- Foster a positive security culture and offer anonymous reporting channels.
- Revoke credentials and access promptly during offboarding.

### Competitors

**Mitigation Tactics:**

- Protect intellectual property using encryption and rights management.
- Secure third-party integrations and enforce supply chain security standards.
- Conduct background checks on employees and vendors.
- Use legal protections such as NDAs and non-compete agreements.
- Monitor for suspicious activity via intrusion detection systems (IDS).

---

## Final Notes

Mitigation is not a one-time event but an **ongoing process** involving:

- Continuous monitoring
- Proactive patching
- Ongoing employee training
- Regular audits and reviews

Understanding the **intent, capability, and access level** of a threat actor helps tailor a **risk-based security strategy**,enabling organisations to allocate resources effectively and prioritise protections where they matter most.