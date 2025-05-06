# Data Traffic & Data Sources

## Common Types of Data Traffic

- **Streaming** – Continuous transmission of audio/video.
- **API Calls** – Requests between systems for data or functionality.
- **Web Traffic** – HTTP/HTTPS data sent between browsers and servers.
- **File Transfers** – E.g., FTP, SMB, or cloud syncing tools.
- **DNS Queries** – Resolving domain names to IP addresses.
- **Protocol Traffic** – Packets from networking protocols (e.g., ARP, ICMP, DHCP).

## Data Sources

Applications interact with various data sources, such as:

- **Databases** (e.g., SQL, NoSQL)
- **Web Services** (RESTful or SOAP)
- **External APIs** (e.g., weather, maps, financial data)

> These often involve **sensitive data** and must be protected using encryption, authentication, and secure transmission protocols.

## Data Security – The Three States of Data

Data exists in one of three states. Each requires specific protection strategies:

|**State**|**Description**|**Protection Methods**|
|---|---|---|
|**At Rest**|Stored data (e.g., on disk or backup)|Full-disk encryption (BitLocker, LUKS)|
|**In Transit**|Moving across a network|TLS/SSL, VPNs, HTTPS|
|**In Process**|Actively used in RAM or CPU|Hardware-based protection (e.g., TPM)|

- **TPM (Trusted Platform Module)** – Hardware chip that stores cryptographic keys securely and ensures integrity of boot processes and memory use.