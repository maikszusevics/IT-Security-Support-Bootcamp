
# Risk Management

Risk management is a crucial process for organisations to address potential threats and ensure the continuity of their mission. It involves understanding, assessing, treating, and continuously monitoring risks to prevent undesirable disruption.

### Defining Risk and its Elements

Risk, particularly in the context of information and system security, is a loaded term that often lacks clear definitions. While IT departments tend to view risk negatively, as problems and inconveniences to be avoided, businesses may see it as an opportunity.

Risk is often defined by the likelihood-severity contrast of a threat. A threat is something or someone that can cause harm by exploiting a vulnerability, which is a weakness in a system that creates a potential attack vector. The elements of risk can be understood through:

Risk is also understood as a **combination** of several elements:

- **Assets** that an organisation owns. In risk management, frameworks are built with people's safety as a primary concern.
- **Threat Agents** (e.g., a hacker) and **Threat Sources** (e.g., malware). These are those seeking to disrupt, damage, or steal assets.
- **Vulnerabilities** which are openings or holes that can be exploited. Intriguingly, safeguards themselves can also contain vulnerabilities or be vulnerabilities (e.g., a VPN, while a primary safeguard for remote access, is also a target for cybercriminals).
- **Impact** resulting from successful exploitation of vulnerabilities by threats.
- **Safeguards** and **Countermeasures** implemented to protect against threats.

Attackers are also subject to economics; they balance the cost of an attack, the ease of exploiting vulnerabilities, and potential repercussions against the opportunity and potential value of a successful attack. Understanding **attacker economics** helps determine the likelihood of a threat successfully exploiting a vulnerability to affect the Confidentiality, Integrity, or Availability (CIA) of an asset.

### Risk Identification

Identifying risks involves a structured way to understand what can lead to an undesirable disruption event and how likely it is to occur. This process considers:

- **Organisational Drivers**: High-level security requirements that direct risk assessments.
- **Thinking Like an Attacker**: Approaching risk by considering an adversary's mindset rather than just a protector's. Attackers aim to cause a **loss of Confidentiality, Integrity, or Availability (CIA)** to achieve their objectives.
    - **Confidentiality**: Preventing unauthorised access to information, such as admin credentials or secret designs. A breach of this principle means violating "no or least privileged principles".
    - **Integrity**: Ensuring information is accurate and trustworthy. Attackers might modify existing data or introduce incorrect data.
    - **Availability**: Ensuring information is accessible when needed. This could involve encrypting data for ransom or delaying information release. A loss of confidentiality can sometimes lead to unavailability, as systems might need to be taken offline for forensic analysis.
- **Threat Intelligence**: Reviewing existing threat intelligence to understand the current landscape. The capability of attackers is increasing due to the commoditisation of attack tools, known as "Cybercrime as a Service".
- **Information Gathering**: Researching industry and education resources.
    - **Vertical Industry Groups**: Such as Information Sharing and Analysis Centres (ISACs), which provide a central resource for sharing cyber incident and threat information (e.g., Aviation ISAC, FS-ISAC).
    - **Horizontal Information Sharing**: From technology service providers, vendors, and hyperscalers (e.g., cloud service providers like Cloudflare, AWS Shield). National agencies (e.g., US CISA) often list approved security vendors.
    - **Standards**: Clear, unambiguous documents providing best advice for situations, containing controls for common risk scenarios. For example, PCI-DSS offers baseline protection recommendations. Controls can be reverse-engineered to understand the risk scenarios they aim to treat.
    - **Internal Company Information**: Consulting CIO, COO, enterprise and business architects, or compliance functions. Reviewing the enterprise risk management framework, information policies, and risk taxonomy. Operational Management Information (MI) like risk registers, post-incident reports, intelligence reports, and board papers provide insights into current and past disruption events.
- **Business Lifecycle**: Risk assessments should be performed throughout a business's lifecycle.
    - In the **early stages** (discovery, change initiation), top-down baseline risk assessments are performed due to limited information, combined with threat analysis. Inherent risk assessments typically use a top-down approach.
    - In **later stages** (design, build, test, deploy), risk assessments become more bottom-up, focusing on design decisions and testing against requirements.

### Risk Assessment

Risk assessment is the process of identifying, estimating, and prioritising risks to an organisation's operations, mission, function, image, and reputation. It considers threats, vulnerabilities, and the mitigations provided by security controls.

Risk assessments often use a **2D grid** that executives understand, plotting risk based on impact (x-axis) and likelihood (y-axis). This helps determine if a risk is within appetite, tolerable, or outside comfort.

**1. Business Impact Assessment (BIA)** A BIA systematically determines how a business can be impacted. It involves understanding:

- **Business Services**: Modelling the business through a "service-oriented approach" (e.g., customer-facing website as an information service, HR system providing multiple services like annual leave and payroll, luggage screening as a crucial safety service). This aligns with regulations like the European Digital Operational Resilience Act (DORA), which mandates identifying important business services.
- **Impact Categories**:
    - **Safety**: Paramount, often overlooked, given that humans are at the heart of most organisations as consumers, clients, or employees.
    - **Financial**: Determining the cost of an incident is complex. Considerations include:
        - Lost capital expenditure (e.g., from badly managed strategic transformation like cloud migration).
        - Technical debt resolution costs.
        - Total cost of recovery.
        - Fines from regulators for data breaches.
        - Legal action costs.
        - Attrition (loss of customers and revenue, or loss of key staff and replacement costs). Financial thresholds should be regularly reviewed.
    - **Reputational**: Very important, constantly changing with society and rapid news cycles (e.g., social media impact measurement).
    - **Regulatory**: Increasing in number and scope, often related to financial penalties. Contradictory financial and regulatory impacts signal a need for further investigation.
- **Recovery Time Objective (RTO)**: How soon a system or service needs to be brought back to an operational state after a disruption. The higher the business impact, the stricter the RTO requirements will be. RTO should be defined for each business service, typically during acute operations when disruption hurts the most, and reviewed regularly. For example, a customer information portal might have an RTO of "a few days" (very low impact), while an aviation security service might require "less than 1 hour" (very high impact).
- **Recovery Point Objective (RPO)**: The amount of data loss that an organisation can tolerate, specified as a length of time from the last good backup to the disruption event. It defines the point in time from which the system needs to be restored. RPO is also defined for each business service that depends on data, typically based on the effort needed to manually reconstruct lost data. For instance, a luggage screening system might have an RPO of "near 0" as data loss is not tolerated.
- **Data Types**: Understanding the sensitivity of data used by business services is crucial. Three general types include data used in delivery (e.g., luggage info), corporate internal data (e.g., CapEx plans), and systems data (e.g., passwords). Data classification labels (public, internal, restricted, highly restricted, secret) indicate sensitivity and the level of controls needed. Regulatory impact often stems from sensitive data.
- **Technology Operations (Tech Stack)**: Understanding the underlying infrastructure (buildings, networking, hardware), databases, applications, platforms, and processes that support services. Shared components across the tech stack can distribute impact. The **cloud shared responsibility model** dictates that the Cloud Service Provider (CSP) is responsible for the security _of_ the cloud, while the customer remains responsible for what they put _in_ the cloud; accountability always remains with the customer. Flaws and vulnerabilities exist throughout the tech stack.

**2. Qualitative Analysis** This is a subjective assessment that produces a **non-numeric view of impact**. It requires an expert view and focuses on the **likelihood** and **impact** of a given threat, often considering operational impacts, brand, and reputation. It is a great way to start analysis at an inception point.

**3. Quantitative Analysis** This objective approach uses **empirical processes**, often actuarial science, to determine the financial impact of a risk. It has three main components:

- **Single Loss Expectancy (SLE)**: The expected loss from a single threat event. Calculated as **Asset Value × Exposure Factor** (the percentage of the asset that could be lost).
- **Annual Rate of Occurrence (ARO)**: How often the event is expected to occur annually (e.g., 1 event every 5 years = 0.2 ARO).
- **Annual Loss Expectancy (ALE)**: The product of SLE and ARO (**SLE × ARO**). The ALE helps in justifying the cost of countermeasures; the cost should not exceed the ALE.

**4. Likelihood Based on Controls** Likelihood estimation in qualitative risk assessment is subjective due to limited scientific data. It is primarily based on the **controls** in place, as these can be influenced to change attacker economics.

- **Control Categories (ISO/IEC 27002)**: Controls can be categorised by themes (people, physical, technology, organisational), control types (prevent, detect, correct/respond), information security properties (CIA), cybersecurity concepts (NIST families like identify, protect, detect, respond, recover), operational capabilities (governance, asset management), and security domains (defence, resilience).
- **Attack Surface Analysis**: Understanding the external interfaces, endpoints, and human errors susceptible to attacks. A larger attack surface means more cost and effort for complete control coverage. Controls themselves can be part of the attack surface, potentially containing flaws (e.g., patching solutions, asset registers).
- **Defence in Depth**: A principle where multiple layers of controls are implemented to reduce the likelihood of compromise.
    - **External Interfaces and Endpoints**: No controls result in "almost certain" compromise. Incomplete coverage leads to "very probable" compromise. Even with fully effective controls, compromise is "possible" due to factors like zero-day exploits, dynamic threats, and human susceptibility to social engineering (e.g., phishing).
    - **Boundary Controls**: Internal firewalls, network segmentation, and cloud account management reduce likelihood further. These are important for managing shared risk distribution and the "blast radius" (systems affected by a single compromise).
    - **End-to-End Controls**: Such as end-to-end encryption, provide an additional layer of protection, further reducing likelihood.
- **Controls Environment**: Establishing controls to reduce both likelihood and impact. Examples include Multi-Factor Authentication (MFA), admin training, spam filters, encrypted credentials, firewalls to impede lateral movement, regular patching, two-person authorisation for security alerts, segmenting control planes, off-site backups, and behavioural analysis/monitoring.
- **Control Assessment**:
    - **Selection**: Using industry information like MITRE ATT&CK, OWASP Top 10, or bespoke intelligence reports from Managed Security Service Providers (MSSPs).
    - **Implementation**: Following standards and best practices.
    - **Effectiveness**: Controls can be "partially effective" if there's an issue with their design or operation (e.g., logs are collected but not reviewed).
    - **Assurance**: Performing activities like penetration testing before release into production.
    - **Continuous Monitoring**: To assess operating effectiveness (e.g., Risk Control Self-Assessments - RCSAs).
    - **Non-Direct Target**: Likelihood should also consider scenarios where the organisation is not a direct target but is affected by collateral damage or random attacks.

### Risk Response and Treatment

Once risks are assessed, an organisation decides on a response or treatment. The aim of risk treatment is to disrupt the attacker's economics, making the cost of an attack outweigh the reward.

- **Modification (Mitigation)**: Implementing controls (technical, physical, environmental, cultural) to reduce the risk to an acceptable level. This was formerly known as mitigation.
- **Retention (Acceptance)**: Accepting the risk and doing nothing, meaning the financial harm is not deemed worthy of further action. This was formerly known as acceptance and requires certification from the business.
- **Avoidance**: Avoiding the activity or condition that precipitates the risk altogether, especially if the risk is too high for the business to absorb.
- **Sharing (Transfer)**: Sharing the risk with another party, such as through contracts, subcontracts, or insurance. This was formerly known as transfer. The annual cost of sharing should not exceed the ALE.

The risk management process is not linear; monitoring may expose new vulnerabilities or threats, necessitating a new assessment or even reframing the organisation's view of risk. All risk responses should be documented in a **risk register** and signed off by the risk owner.

**Risk Profile, Appetite, and Tolerance:**

- **Risk Appetite**: The acceptable level of business activities as defined by senior management.
- **Risk Tolerance**: A permissible deviation from the risk appetite. Different departments may have varying attitudes towards what is acceptable.
- **Risk Profile**: A description of the organisation's risk environment and the maturity/effectiveness of its risk program.

### Risk Monitoring and Analysis

Continuous risk monitoring and analysis are vital for maintaining an organisation's security posture. This involves:

- **Ongoing Investigation**: Looking for new vulnerabilities, emerging threats, changes in asset values, and modifications in laws and regulations.
- **Log Management**: Core to monitoring, involving policies and procedures for collecting, storing, and accessing logs from critical devices (compute, network, storage). A distributed log collector centralises this information.
- **Security Information and Event Management (SIEM)**: Systems that collect telemetry data from multiple sources and provide **correlation** (identifying related events), **normalisation** (mapping to common formats), and **aggregation** (enterprise-level understanding). SIEMs can leverage artificial intelligence for analysis but still require tuning and human oversight.
- **Monitoring Systems**:
    - **Real-time Monitoring**: Provides immediate identification and often stopping of events (e.g., Network Intrusion Detection Systems - NIDS, Host-based Intrusion Detection Systems - HIDS).
    - **Non-real-time Monitoring**: Saves information about system events for after-the-fact analysis (e.g., system logging).
    - **Intrusion Detection and Prevention Systems (IDPS)**: These include NIDS/HIDS (passive, detect/report) and Network Intrusion Prevention Systems (NIPS)/Host-based Intrusion Prevention Systems (HIPS) (active, stop attacks). They operate based on signatures of known attacks, anomalies (e.g., unusual traffic volume), and policies.
    - **Data Loss Prevention (DLP)**: Technologies for discovering, classifying, monitoring, and enforcing policies on data usage across locations and platforms. DLP architecture includes client-based (endpoint), network (gateway), and storage components.
- **Vulnerability and Security Assessment**:
    - **Vulnerability Assessment**: Focuses on discovering known issues within systems, using techniques like OS fingerprinting, banner grabbing, and privileged logon. Scanners are used for this, but can produce false positives and are only temporal in nature. This also includes host scanning (checking unencrypted authentication, patch levels, file permissions).
    - **Penetration Testing**: Helps expose "unknown unknowns" by simulating real-world attacks.
        - **Modes**:
            - **Zero Knowledge (Black Box)**: Simulates an external hacker with only publicly available information.
            - **Partial Knowledge (Grey Box)**: The tester is given some information (e.g., IP addresses, network layouts).
            - **Full Knowledge (White Box)**: Complete familiarity with the network and applications, useful for internal threat assessment.
            - **Blind Test**: Conducted without the IT department's knowledge to assess the security team's responsiveness.
        - **Phases**: Preparation (authorisation, defining outcomes), Reconnaissance (information gathering), Enumeration (risk analysis before active penetration), Active Exploitation (based on guidelines), and Reporting (documentation, analysis, remediation suggestions).
- **Communication**: Continuous communication of risk assessment reports is essential to demonstrate how security benefits the organisation and aligns with its mission. Data visualisation tools can help present audit findings and maturity over time.
- **Confidence in Assessments**: Transparency about the level of confidence in a risk assessment is important. Using a framework like the Johari window (known knowns, known unknowns, unknown knowns, unknown unknowns) helps understand knowledge gaps. As knowledge improves, risk assessments might show risks "getting worse," which indicates improved assessment rather than actual deterioration. Repeatability through consistent methods increases confidence.