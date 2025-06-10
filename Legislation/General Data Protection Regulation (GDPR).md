# General Data Protection Regulation (GDPR)

The **General Data Protection Regulation (GDPR)** is a comprehensive data protection law enacted by the European Union, designed to give individuals more control over their personal data. It significantly updated and harmonised data privacy laws across Europe, setting a global benchmark for data protection.

#### Origins and Implementation

The GDPR is a **European Union regulation that governs the collection, processing, and storage of personal data**. It was developed in response to the rapid growth of digital data and the increasing complexity of data processing, aiming to strengthen and unify data protection for all individuals within the EU. The regulation came into effect on **25 May 2018**, replacing the older 1995 Data Protection Directive.

In the UK, the GDPR works in conjunction with the **Data Protection Act 2018 (DPA 2018)**. The DPA 2018 complements the GDPR by incorporating its provisions into UK law and making specific allowances for areas where the GDPR permits national variations, such as processing for law enforcement and intelligence services. This ensures that the robust protections of GDPR are fully integrated and enforceable within the UK legal framework.

#### What the Law States: Core Principles and Rights

GDPR fundamentally regulates the use of personal data and **mandates secure processing**. It covers not only digital data but also **paper filing systems** that contain personal information.

The core of GDPR is built around **seven key data protection principles** that organisations (data controllers and processors) must adhere to when handling personal data:

1. **Lawfulness, fairness, and transparency**: Personal data must be processed lawfully, fairly, and in a transparent manner in relation to the data subject.
2. **Purpose limitation**: Data must be collected for specified, explicit, and legitimate purposes and not further processed in a manner that is incompatible with those purposes.
3. **Data minimisation**: Personal data collected must be adequate, relevant, and limited to what is necessary in relation to the purposes for which they are processed.
4. **Accuracy**: Personal data must be accurate and, where necessary, kept up to date; every reasonable step must be taken to ensure that inaccurate data is erased or rectified without delay.
5. **Storage limitation**: Personal data must be kept in a form which permits identification of data subjects for no longer than is necessary for the purposes for which the personal data are processed.
6. **Integrity and confidentiality (security)**: Personal data must be processed in a manner that ensures appropriate security of the personal data, including protection against unauthorised or unlawful processing and against accidental loss, destruction, or damage, using appropriate technical or organisational measures.
7. **Accountability**: The data controller is responsible for, and must be able to demonstrate compliance with, the other principles.

Beyond these principles, GDPR grants individuals significantly **enhanced rights** over their personal data, including:

- The **right to be informed**: Individuals have the right to know how their data is being used.
- The **right of access** (known as a **Subject Access Request or SAR**): Individuals can request a copy of the personal data an organisation holds about them. Organisations typically have a **1 calendar month limit** to respond to such requests.
- The **right to rectification**: Individuals can request inaccurate data be corrected.
- The **right to erasure** (the "right to be forgotten"): Individuals can request their personal data be deleted under certain circumstances.
- The **right to restrict processing**: Individuals can request the processing of their data be limited.
- The **right to data portability**: Individuals can obtain and reuse their personal data for their own purposes across different services.
- The **right to object**: Individuals can object to the processing of their personal data in certain situations.
- Rights in relation to **automated decision-making and profiling**: Individuals have the right not to be subject to decisions based solely on automated processing, including profiling, which produces legal effects concerning them or similarly significantly affects them.

#### Offences and Enforcement

**Non-compliance** with GDPR can lead to severe consequences, including **legal penalties, reputation damage, or financial loss**. The regulation introduced a two-tiered fine structure, with penalties reaching up to **€20 million or 4% of an organisation's annual global turnover**, whichever is higher, for the most serious infringements.

Examples of offences and infringements include:

- Failure to adhere to data protection principles.
- Failure to implement appropriate technical and organisational security measures.
- Failure to notify data breaches to the supervisory authority and affected data subjects.
- Failure to respond to or facilitate individuals' rights (e.g., SARs).
- Unlawful processing of personal data.

In the UK, the **Information Commissioner's Office (ICO)** is the independent supervisory authority responsible for upholding information rights in the public interest and enforcing GDPR. The ICO has the power to investigate complaints, conduct audits, issue warnings, reprimands, orders, and impose fines.

#### Impact on Industry

GDPR has had a profound impact across all industries globally that process the personal data of EU citizens, necessitating significant shifts in data handling practices. It compels organisations to:

- **Implement Robust Data Security Measures**: Organisations must ensure **secure processing**, including the protection of **sensitive data** using **encryption, authentication, and secure transmission protocols**.
    - **Encryption** is crucial for data in all its states:
        - **At Rest**: Stored data (e.g., on disk or backup) must be encrypted using methods like **Full-disk encryption (BitLocker, LUKS)**.
        - **In Transit**: Data moving across a network should be protected by **TLS/SSL, VPNs, or HTTPS**. **VPNs** use **tunnels** and provide **encrypted communications**.
        - **In Process**: Actively used data in RAM or CPU requires **Hardware-based protection (e.g., TPM)**, which securely stores cryptographic keys and provides a protected environment for decryption.
    - Strong **Authentication** is paramount. **Multi-Factor Authentication (MFA)**, requiring two or more verification factors from different categories (something you know, something you have, something you are), is a key defence against credential-based attacks. Users should **never share authentication codes or approve MFA requests they didn't initiate**.
    - **Physical security** measures, such as **Access Control Vestibules (Mantrap)**, **Fencing**, **Bollards**, and **Video Surveillance** (CCTV), along with **locks** and **guards**, contribute to protecting physical data assets.
- **Enhance Transparency**: Businesses must clearly inform individuals about how their data is collected, used, and stored, often through comprehensive privacy notices.
- **Improve Accountability**: Organisations must be able to **demonstrate compliance** with the data protection principles. This involves maintaining detailed **audit trails**, **documentation**, user consent logs, and access records.
- **Adopt a Proactive Security Posture**: GDPR encourages a continuous approach to security, including **risk identification, assessment, and treatment**, along with **continuous monitoring** of security data across systems and networks. This aligns with broader cybersecurity best practices and frameworks such as NIST and ISO/IEC 27001/27002, which provide guidance for implementing Information Security Management Systems (ISMS).
- **Focus on Compliance and Governance**: Adherence to GDPR is a critical aspect of **GRC (Governance, Risk, and Compliance)**. Compliance ensures that the organisation adheres to relevant laws, regulations, standards, and internal policies. Non-compliance carries significant penalties, underscoring the importance of legal adherence.