# Business Continuity

Business continuity is a vital component of an organisation's overall resilience, ensuring the ability to continue operations even during adverse circumstances. It is often invoked when an incident's duration exceeds acceptable timelines, aiming to keep the business operational. While incident response addresses immediate adverse events, and disaster recovery focuses on catastrophic events requiring relocation, business continuity plans bridge the gap by allowing sustained operations through significant disruptions.

## Business Continuity Management System (BCMS) Outcomes

A comprehensive Business Continuity Management System (BCMS) aims for several key outcomes, including:
*   Effective incident response planning, focusing on life safety, containment, documentation, and a swift return to normal operations.
*   Robust business continuity planning, driven by business impact analysis (BIA), identification of critical business functions (CBFs), establishing recovery time objectives (RTO), defining data recovery point objectives (RPO), and detailing requirements for system recovery.
*   Disaster recovery planning for catastrophic events that necessitate the relocation of IT and other services to an alternate location.

## BCMS Program Management

Business continuity is essentially a project management discipline, following a structured process:
1.  **Project Initiation:** Beginning the BC planning process.
2.  **Business Impact Analysis (BIA):** Analysing the potential impact of disruptions.
3.  **Strategy Selection:** Choosing appropriate recovery strategies based on BIA findings.
4.  **Plan Development:** Writing detailed plans for implementing recovery strategies.
5.  **Implementation and Testing:** Putting plans into practice and verifying their effectiveness through testing.
6.  **Communication and Training:** Rolling out plans and training staff on their roles.
7.  **Maintenance:** Regularly reviewing and updating plans based on tests, incidents, and changes.
8.  **Lessons Learned:** Continuously improving the plans based on experience.

## Business Impact Analysis (BIA)

The Business Impact Analysis (BIA) is arguably the most critical step in business continuity planning. It involves a thorough analysis of the potential impact of disruptions on the business over time. Unlike traditional risk management, which considers both impact and likelihood, BIA focuses solely on the impact over time.

The BIA determines several key elements:
*   **Critical Business Functions (CBFs):** Identifies the business processes that, if disrupted, would have the most significant impact on profitability, reputation, and operations. Some departments are more critical than others.
*   **Critical Supporting Processes (CSPs):** Defines the dependencies that CBFs have on other processes, as essential services cannot be recovered without their supporting processes.
*   **Resource Requirements:** Specifies the resources (people, data, facilities, equipment, supply chain) needed to restore systems and functions.
*   **Priorities for Recovery:** Establishes the order in which systems and processes should be recovered, based on their criticality and impact.

### Key Metrics from BIA

The BIA helps define critical recovery metrics:
*   **Maximum Tolerable Downtime (MTD):** Also known as the Maximum Tolerable Period of Disruption (MTPD) or Maximum Allowable Downtime (MAD), this is the maximum period an organisation can tolerate for a critical business process to be unavailable before business failure occurs (e.g., loss of customer confidence, financial collapse, regulatory non-compliance). The longer an outage, the greater the exponential damage to reputation and finance.
*   **Recovery Time Objective (RTO):** The target time by which a business process or system must be restored after a disruption to avoid exceeding the MTD. The RTO for a critical process must be significantly less than its MTD.
*   **Recovery Point Objective (RPO):** This metric measures the maximum amount of data (measured in time, e.g., an hour's worth of data) that can be lost from the time of an outage to the last viable data backup. It determines how old the data will be when systems are restored, directly influencing backup strategies.

### Resource and Cost Considerations

*   The BIA also determines the resources required to restore systems, including supporting processes and controls to prevent re-infection.
*   There's an inverse relationship between the cost of recovery and the duration of an outage: a minimal outage time typically incurs a very high recovery cost. The goal is to find a balance where the cost of recovery aligns with the tolerable impact.

### Setting Priorities

*   System recovery priorities are established based on the cost of recovery options and the impact on the business.
*   Recovery options must be feasible, acceptable to stakeholders (customers, owners, management), and suitable for the type of business.
*   These priorities can be contentious and require approval from senior executives.

## Data Preservation and Recovery

Data is an essential resource for IT system recovery. The RPO is a key driver for an organisation's backup strategy.

Strategies for data preservation and recovery include:
*   **Cloud Storage:** Storing data offsite for availability even if the primary location is compromised.
*   **Internal Hard Drives/Storage Area Networks (SANs):** Utilising internal or network-attached storage.
*   **Removable Storage Media:** Storing backups on media that can be securely transported offsite.
*   **Mirroring:** Duplicating data on two different systems, possibly geographically dispersed.
*   **Vaulting:** Regularly transferring data to an electronic or physical offsite vault (e.g., hourly or after a set number of transactions).
*   **Remote Journaling:** For databases, journal entries (records of changes) are written off to another location, allowing recovery up to the point of failure by applying journals to a full backup.

### System Resilience

Building resilient systems involves:
*   **Fault Tolerance:** Incorporating duplication and redundancy of equipment and networks so that a single failure does not disrupt operations.
*   **Clustering:** Grouping multiple servers to work together and share the load, ensuring minimal impact if one server fails.
*   **High Availability:** Designing systems to minimise downtime and ensure continuous operation.
*   **Failover:** The ability of a system to automatically switch to a standby system or component when the primary one fails.
*   **Quality of Service (QoS):** Ensuring adequate bandwidth, storage, and other resources to handle processing demands.

## Writing, Implementing, and Testing Plans

Business continuity plans are typically action-oriented, providing clear steps to follow during a crisis. For large organisations, there may be many specific plans tailored to different incident types.
*   **Worst-Case Scenario:** Plans should be written to address the most resource-intensive situations (worst-case scenarios), as this ensures that any lesser incident will also be covered.
*   **Team Assignments:** Clear roles, responsibilities, leaders, and deputies should be assigned to various teams, with cross-training encouraged.
*   **Communication:** Robust communication channels are essential for employees, management, regulatory agencies, customers (especially for privacy breaches), suppliers, and shareholders. Regular status reports are often managed from an Emergency Operations Centre (EOC).
*   **Restoration:** After an incident, critical business functions are prioritised for initial recovery. However, when restoring to "normal" operations, less critical functions are often restored first. This allows for testing of migration plans, networks, and systems before risking critical functions in a new environment.
*   **Testing:** Plans must be thoroughly and realistically tested to find deficiencies, train staff, develop skills, and ensure effectiveness. Testing should start small and gradually increase in complexity.
*   **Lessons Learned:** Every test and incident provides key learning points that must be documented and applied to improve preparation, plans, teams, tools, training, and overall awareness. This fosters a security-conscious culture where staff understand and contribute to security.