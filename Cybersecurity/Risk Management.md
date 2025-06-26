### Risk Management

Risk management is a structured approach to identifying, assessing, and mitigating risks to an organisation’s assets, ensuring compliance with laws and regulations, and aligning IT with business objectives. Its core mission is to **prevent undesirable disruption to the organisation’s mission**. Risk management is one of the three components of GRC (Governance, Risk, and Compliance), which aims to align IT with business objectives while managing risk and ensuring compliance. Each component of GRC plays a distinct but interconnected role in maintaining the security and integrity of systems and data.

#### Understanding Risk and Attackers

**Risk** is often defined by the **likelihood-severity contrast** of a **threat**. A **threat** is something or someone that can cause harm by exploiting a **vulnerability**, which is a weakness in a system that creates a potential attack vector. The elements of risk can be understood through:

- **Threat agent/source**: The entity (e.g., a dog, a hacker) or mechanism (e.g., dog's teeth, malware) causing harm.
- **Safeguard**: A primary protection measure (e.g., a fence, a VPN).
- **Vulnerability**: A weakness, which can sometimes be inherent in a safeguard itself (e.g., a hole in the fence, a VPN being a target for cybercriminals).
- **Asset**: The valuable item at risk (e.g., a baseball, a human hand, data, systems).

To effectively manage cyber risk, it is crucial to **think like an attacker**. Attackers conduct their own risk assessments, balancing the cost of an attack, the ease of using available tools and procedures, and potential repercussions if they are caught, against the opportunity and potential value of a successful compromise. Their motivations can include political agendas, greed for financial gain, revenge for perceived wrongs, or a desire for notoriety. By understanding attacker economics, organisations can aim to **disrupt the attacker's economics** enough to make the cost outweigh their potential reward.

Cybersecurity efforts primarily focus on protecting the **CIA Triad**:

- **Confidentiality**: Ensuring information is accessible only to authorised individuals, maintaining privacy. Attackers might seek to gain admin credentials to access confidential information, or disclose secret designs to third parties. Encryption and Multi-Factor Authentication (MFA) are key controls for confidentiality.
- **Integrity**: Guaranteeing the consistency and accuracy of data. This involves preventing modification of existing data or introduction of incorrect data, such as changing pricing data or altering a government report. File permissions, access control, and version control support integrity.
- **Availability**: Ensuring information and systems are accessible when needed by authorised users. Attackers might encrypt data for ransom or delay the release of information. Patches, updates, backups, and disaster recovery/high availability solutions contribute to availability. It is important to note that a loss of confidentiality can also lead to some degree of unavailability (e.g., systems offline for forensic analysis), and delaying or preventing timely access to information can impact its integrity.

#### Risk Assessment Fundamentals

Risk assessment helps answer fundamental questions like "what information security is needed?" and "how much security is required?". It is the process of identifying, estimating, and prioritising risk to an organisation's operations, including its mission, function, image, and reputation. This involves understanding what could lead to an undesirable disruption event and how likely it is to occur. Most risk assessment reports utilise a **2D grid** which plots likelihood against impact, making it understandable for executives, who typically hold the budget. This grid helps determine if a risk is within appetite, tolerable for a period, or outside comfort levels.

##### Business Impact Assessment (BIA)

A **Business Impact Assessment (BIA)** is crucial for understanding the potential ways a business can be impacted. It helps contextualise what "impact" means for an organisation by providing a **risk impact matrix**. Key categories of impact often include:

- **Safety**: Direct harm to humans, including physical injury and mental health impacts on customers or staff. The focus is on human safety, which should always be a primary consideration.
- **Financial**: Direct and indirect monetary losses. This can include lost capital expenditure from badly managed strategic transformation (e.g., cloud migration with unaddressed security requirements), total cost of recovery, regulatory fines (e.g., for data breaches), legal action from insecure products/services, and costs from customer or staff attrition. Financial impact thresholds differ by organisation.
- **Reputational**: Damage to the organisation's public image and trustworthiness. This can be influenced by social media and rapid news cycles, requiring regular review of thresholds as society evolves.
- **Regulatory**: Penalties or sanctions due to non-compliance with laws and regulations. Regulatory impact often correlates with financial impact, as fines and sanctions can be quantified, and their upper limits or precedents may be known. When reviewing potential impact, all categories should be considered holistically. A service-oriented approach is often used in BIAs, viewing systems through the lens of the business services they provide (e.g., customer information portal, HR system, luggage screening).

Two critical concepts for specifying resilience requirements and understanding business impact are:

- **Recovery Time Objective (RTO)**: The maximum tolerable duration of time a service can be unavailable following a disruption. A higher business impact typically leads to stricter RTO requirements. RTO focuses on how soon a system needs to be brought back to an operational state. This can be dynamic and should be reviewed regularly based on business needs and context, such as critical operating hours.
- **Recovery Point Objective (RPO)**: The maximum tolerable amount of data loss, measured as a period of time from the last good backup to the disruption event. This indicates how much data the business can afford to lose. RPO is tied to the effort needed to manually reconstruct lost data. Understanding the interconnectedness of business services and their RTOs/RPOs is vital, as a disruption in one service can impact others. An additional metric, **impact tolerance**, defined in frameworks like DORA, specifies the point at which there could be catastrophic, widespread consequences for important business services.

##### Likelihood Determination

The likelihood of a compromise is often estimated qualitatively, based on the effectiveness of controls. It is a subjective estimate due to limited science and data in this young field. Information gathering is key, drawing from:

- **Industry intelligence**: Vertical industry groups (e.g., **ISACs** like the Aviation ISAC or FS-ISAC), technology service providers (who often educate and provide resources), and national agencies (e.g., the US **CISA**).
- **Standards and frameworks**: Documents like **PCI-DSS** (for baseline protection), **ISO/IEC 27002** (for implementation guidance and best practices, including control attributes), and **NIST** Special Publications 800-39 (for managing information security risk) provide controls for common risk scenarios. These can be reverse-engineered to understand target risk scenarios.
- **Company internal information**: Insights from CIOs, COOs, architects, compliance functions, enterprise risk management frameworks, risk registers, post-incident reports, and board papers. The **risk register** is a key place to compile and track all risks, their status, and resolution.

Controls can be categorised in various ways, including by their:

- **Themes**: People, physical, technology, organisational (e.g., policies).
- **Types**: Prevent, detect, or correct (respond).
- **InfoSec properties**: Confidentiality, Integrity, and Availability.
- **Cybersecurity concepts**: **NIST** control families (identify, protect, detect, respond, recover).
- **Security domains**: Defence or resilience.

**Defence in depth** is a fundamental principle, involving a layered approach to controls to reduce the likelihood of compromise:

- **External Interfaces and Endpoints**: Controls on internet-accessible attack surfaces (e.g., firewalls, strong authentication, patching, endpoint protection). Without this protection, compromise is almost certain.
- **Trust Boundaries**: Internal network segmentation (e.g., VLANs, internal firewalls) to limit lateral movement within systems. This helps define a "blast radius" for a compromise.
- **End-to-End Controls**: Such as end-to-end encryption, further reducing likelihood even if initial layers are breached.

**Attack surface analysis** is critical to understanding where controls are needed, factoring in the size, distribution, and volume of components. It is important to remember that controls themselves can also be part of the attack surface, potentially having flaws or vulnerabilities that attackers could exploit (e.g., distributed system controls, patching solutions, asset registers). **Asset management** is a key control for risk identification, assessment, and management, as it is difficult to secure what is unknown.

Creating a robust **controls environment** involves implementing specific measures to reduce likelihood and impact. Examples include:

- **Multi-Factor Authentication (MFA)**: A key defence against credential-based attacks like brute force and phishing, requiring two or more verification factors from different categories (e.g., password and fingerprint).
- **Security awareness training**: Educating staff to recognise deception tactics like phishing and social engineering.
- **Spam filtering and email security**: Deploying filters to block malicious domains and enabling protocols like SPF, DKIM, and DMARC.
- **Encryption**: Protecting data at rest, in transit (e.g., HTTPS, TLS, VPNs, SSH), and end-to-end to support confidentiality and integrity.
- **Firewalls**: Restricting incoming/outgoing traffic, preventing unauthorised access, and limiting lateral movement.
- **Regular patching and updates**: Closing known vulnerabilities in OS, applications, and firmware.
- **Behavioural analysis and monitoring against known good states**: Detecting anomalies and suspicious activity.
- **Least Privilege Access**: Users and systems granted only minimum access needed to perform tasks, limiting potential damage from compromise.

Controls should be assessed for both their **design suitability** and **operational effectiveness**. **Vulnerability assessments** focus on identifying known issues within systems, using techniques like OS fingerprinting, banner grabbing, privileged logon attempts, and host scanning for unencrypted information or patch levels. However, vulnerability assessments can have issues like **false positives** or **crash exposure** if not handled carefully, and they are temporal in nature. **Penetration testing** goes further, aiming to expose "unknown unknowns" by simulating real attacks. This can be done in various modes (zero knowledge, partial knowledge, full knowledge, blind) and follows phases from preparation and reconnaissance to enumeration, active exploitation, and reporting.

#### Risk Treatment and Lifecycle

Once risks are assessed, decisions must be made on how to treat them. Common **risk treatment options** include:

- **Mitigate (Modification)**: Implement controls to reduce likelihood or impact. This often involves technical, physical, environmental, or cultural controls. The cost of these countermeasures should be justified against the asset's value or the Annual Loss Expectancy (ALE).
- **Transfer (Sharing)**: Shift risk to a third party, such as through insurance or managed service providers. While responsibility may be transferred, accountability typically remains with the organisation.
- **Accept (Retention)**: Acknowledge the risk and proceed without further treatment, typically when the risk is within the organisation's appetite. This decision often requires certification by the business.
- **Avoid**: Change plans or operations to eliminate the risk entirely. This might involve not migrating a system if the risk is too high to absorb.

**Inherent risk** is the risk prior to applying specific risk treatments, often including controls that are inherently part of the environment or provided by third parties (e.g., cloud service providers). **Residual risk** is the risk that remains after controls have been implemented and operated.

Risk assessments are an ongoing process throughout a business lifecycle. In early stages (discovery, design), top-down assessments focus on overall business impact. As solutions are built and deployed, bottom-up assessments focus on the technology stack and control effectiveness, ultimately combining to determine residual risk during operational readiness reviews and ongoing business as usual. Program and project managers might primarily focus on delivery risk (meeting milestones) rather than inherent operational risks, which requires careful alignment and communication to ensure security is considered.

**Continuous monitoring** is essential for maintaining an effective risk management posture. This involves:

- **Log Management**: Core to monitoring and analysis, it requires clear policies on what devices and data to collect, where to store it, how long to retain it, and who has access to ensure integrity. Logs from various sources (compute, network, storage) are often collected and aggregated centrally.
- **Security Information and Event Management (SIEM)**: A security solution that provides real-time analysis of security alerts by collecting, normalising, and correlating log data from across an IT environment. **SIEM** is used for threat detection (e.g., brute-force attacks, unauthorised access, malware outbreaks), compliance reporting, and incident response.
- **Security Orchestration, Automation, and Response (SOAR)**: A suite of tools that streamlines security operations and automates incident response, often working in conjunction with **SIEM** solutions. SOAR uses predefined **playbooks** and an **automation engine** to execute actions (e.g., block IP, isolate host). Its purpose includes incident triage, response automation, orchestration of disparate security tools, and centralised case management.
- **Types of Monitoring**: Can be **real-time** (immediate identification and stopping of events, e.g., Network/Host Intrusion Detection/Prevention Systems - NIDS/HIDS/NIPS/HIPS) or **non-real-time** (saving information and monitoring integrity after the fact, e.g., system logging). Systems can use signature-based, anomaly-based, or policy-based engines.
- **Data Loss Prevention (DLP)**: Monitors the usage of data across locations and platforms, allowing administrators to define and enforce usage policies, and can be implemented at the client, network, or storage level.

Continuous monitoring, proactive patching, ongoing employee training, and regular audits are essential for maintaining an effective risk management posture. **Risk control self-assessments (RCSAs)** are a type of risk assessment reported top-down, with bottom-up assessments captured during controls testing.

#### Considerations for Confidence and Maturity

Several human factors and organisational dynamics can influence risk assessments, such as overconfidence (Dunning-Kruger effect), deference to senior opinions, or confirmation bias (deciding an outcome then seeking data to support it).

Increasing confidence in risk assessments involves:

- **Transparency**: Being clear about the level of confidence in an assessment and addressing unknown areas.
- **Repeatability**: Following a consistent method to ensure similar outcomes from different professionals.
- **Continuous Improvement**: Formalising feedback loops to track and enhance risk management maturity over time.
- **Industry Collaboration**: Leveraging external knowledge to understand "unknown knowns" (risks known to the wider industry or academia but not internally). **MITRE ATT&CK** knowledge base and **OWASP Top 10** vulnerabilities are examples of external intelligence sources that inform control choices.

A key principle is that as knowledge improves, subsequent risk assessments might appear to show risk "getting worse" not because the situation is deteriorating, but because the organisation is getting better at identifying and understanding its risks. Risk assessments are inherently point-in-time exercises, and a robust maturity process helps to continuously improve the understanding and management of risk.