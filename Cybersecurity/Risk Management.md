### Risk Management

Risk management is a structured approach to identifying, assessing, and mitigating risks to an organisation’s assets, ensuring compliance with laws and regulations, and aligning IT with business objectives. Its core mission is to **prevent undesirable disruption to the organisation’s mission**.

---

#### Understanding Risk and Attackers

**Risk** is often defined by the likelihood and impact of a threat. A **threat** is something or someone that can cause harm by exploiting a **vulnerability**, which is a weakness in a system that creates a potential attack vector.

To effectively manage cyber risk, it is crucial to **think like an attacker**. Attackers conduct their own risk assessments, balancing the cost of an attack, the ease of using available tools and procedures, and potential repercussions, against the opportunity and potential value of a successful compromise. By understanding attacker economics, organisations can aim to **disrupt the attacker's economics** enough to make the cost outweigh their potential reward.

Cybersecurity efforts primarily focus on protecting the **CIA Triad**:

- **Confidentiality**: Ensuring information is accessible only to authorised individuals, maintaining privacy.
- **Integrity**: Guaranteeing the consistency and accuracy of data.
- **Availability**: Ensuring information and systems are accessible when needed by authorised users.

---

#### Risk Assessment Fundamentals

Risk assessment helps answer fundamental questions like "what information security is needed?" and "how much security is required?". This involves understanding what could lead to an undesirable disruption and how likely it is to occur.

Most risk assessment reports utilise a **2D grid** which plots likelihood against impact, making it understandable for executives. This grid helps determine if a risk is within appetite, tolerable for a period, or outside comfort levels.

##### Business Impact Assessment (BIA)

A **Business Impact Assessment (BIA)** is crucial for understanding the potential ways a business can be impacted. It helps contextualise what "impact" means for an organisation. Key categories of impact often include:

- **Safety**: Direct harm to humans (e.g., physical injury, mental health).
- **Financial**: Direct and indirect monetary losses (e.g., capital expenditure, recovery costs, regulatory fines, legal action, customer/staff attrition).
- **Reputational**: Damage to the organisation's public image and trustworthiness.
- **Regulatory**: Penalties or sanctions due to non-compliance with laws and regulations.

A service-oriented approach is often used in BIAs, viewing systems through the lens of the business services they provide (e.g., customer information portal, HR system, luggage screening).

Two critical concepts for specifying resilience requirements and understanding business impact are:

- **Recovery Time Objective (RTO)**: The maximum tolerable duration of time in which a service can be unavailable following a disruption. A higher business impact typically leads to stricter RTO requirements.
- **Recovery Point Objective (RPO)**: The maximum tolerable amount of data loss, measured as a period of time from the last good backup to the disruption event. This indicates how much data the business can afford to lose.

Understanding the interconnectedness of business services and their RTOs/RPOs is vital, as a disruption in one service can impact others.

##### Likelihood Determination

The likelihood of a compromise is often estimated qualitatively, based on the effectiveness of controls. Information gathering is key, drawing from:

- **Industry intelligence**: Vertical industry groups (e.g., ISACs), technology service providers, and national agencies (e.g., CISA).
- **Standards and frameworks**: Documents like PCI-DSS, ISO/IEC 27002 provide best practices and common controls that can be reverse-engineered to understand target risk scenarios.
- **Company internal information**: Insights from CIOs, COOs, architects, compliance functions, enterprise risk management frameworks, risk registers, post-incident reports, and board papers.

Controls can be categorised in various ways, including by their theme (people, physical, technology, organisational), type (prevent, detect, correct), cybersecurity concept (identify, protect, detect, respond, recover), or security domain (defence, resilience).

**Defence in depth** is a fundamental principle, involving a layered approach to controls to reduce the likelihood of compromise:

- **External Interfaces and Endpoints**: Controls on internet-accessible attack surfaces (e.g., firewalls, strong authentication, patching, endpoint protection). Without this, compromise is almost certain.
- **Trust Boundaries**: Internal network segmentation (e.g., VLANs, internal firewalls) to limit lateral movement within systems.
- **End-to-End Controls**: Such as end-to-end encryption, further reducing likelihood even if initial layers are breached.

**Attack surface analysis** is critical to understanding where controls are needed. Factors include the size, distribution, and volume of components. It's important to remember that controls themselves can also be part of the attack surface, potentially having flaws or vulnerabilities that attackers could exploit.

Creating a robust **controls environment** involves implementing specific measures to reduce likelihood and impact, such as Multi-Factor Authentication (MFA), security awareness training, spam filtering, encryption of credentials, firewalls to restrict lateral movement, regular patching, and behavioural analysis and monitoring against known good states. Controls should be assessed for both their design suitability and operational effectiveness.

---

#### Risk Treatment and Lifecycle

Once risks are assessed, decisions must be made on how to treat them. Common **risk treatment options** include:

- **Mitigate**: Implement controls to reduce likelihood or impact.
- **Transfer**: Shift risk to a third party (e.g., insurance, managed service provider).
- **Accept**: Acknowledge the risk and proceed without further treatment, typically when the risk is within the organisation's appetite.
- **Avoid**: Change plans or operations to eliminate the risk entirely (e.g., not migrating a system).

**Inherent risk** is the risk prior to applying specific risk treatments, often including controls that are inherently part of the environment or provided by third parties (e.g., cloud service providers). **Residual risk** is the risk that remains after controls have been implemented and operated.

Risk assessments are an ongoing process throughout a business lifecycle. In early stages (discovery, design), top-down assessments focus on overall business impact. As solutions are built and deployed, bottom-up assessments focus on technology stack and control effectiveness, ultimately combining to determine residual risk during operational readiness reviews and ongoing business as usual.

Continuous monitoring, proactive patching, ongoing employee training, and regular audits are essential for maintaining an effective risk management posture.

---

#### Considerations for Confidence and Maturity

Several human factors and organisational dynamics can influence risk assessments, such as overconfidence (Dunning-Kruger effect), deference to senior opinions, or confirmation bias.

Increasing confidence in risk assessments involves:

- **Transparency**: Being clear about the level of confidence in an assessment and addressing unknown areas.
- **Repeatability**: Following a consistent method to ensure similar outcomes from different professionals.
- **Continuous Improvement**: Formalising feedback loops to track and enhance risk management maturity over time.
- **Industry Collaboration**: Leveraging external knowledge to understand "unknown knowns" (risks known to the wider industry but not internally).

A key principle is that as knowledge improves, subsequent risk assessments might appear to show risk "getting worse" not because the situation is deteriorating, but because the organisation is getting better at identifying and understanding its risks.