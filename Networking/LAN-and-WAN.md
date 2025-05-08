# Understanding LAN and WAN Networks

## LAN (Local Area Network)

A **Local Area Network (LAN)** connects computers and devices within a **limited geographic area**, typically:

- **Coverage**: A home, office, building, or campus
- **Speed**: Generally high-speed (100 Mbps to 10+ Gbps)
- **Ownership**: Usually owned, controlled, and maintained by a single organisation

### Common LAN Technologies

- **Ethernet** (wired connections using Cat5e, Cat6, or higher)
- **WiFi** (wireless connections using IEEE 802.11 standards)
- **Switches** and **routers** for local traffic routing and management

### Common LAN Applications

- File and printer sharing
- Internal email and messaging systems
- Shared software or applications
- Access to local databases
- Network-attached storage (NAS)

## WAN (Wide Area Network)

A **Wide Area Network (WAN)** connects multiple LANs over **large geographic areas**, enabling long-distance communication between sites.

- **Coverage**: Spans cities, regions, countries, or globally
- **Speed**: Typically slower than LANs due to longer transmission distances and higher complexity
- **Ownership**: Often relies on **third-party carriers or ISPs** for leased infrastructure

### Common WAN Technologies

- **Leased lines** (e.g., T1/E1, fiber circuits)
	- A **leased line** is a **dedicated, always-on connection** between two points, typically provided by a telecom company. It offers **guaranteed bandwidth, low latency, and symmetrical speeds**, making it ideal for business-critical applications like site-to-site data transfer, VoIP, or video conferencing. It's not shared with other customers, which improves reliability and performance, but it's very **expensive**. It is like a private road between your office and a datacenter, no traffic, always available.
- **MPLS** (Multiprotocol Label Switching)
	- **MPLS** is a **high-performance routing technique** used in WANs to **prioritise and route data efficiently**. It works by attaching **labels** to packets, allowing routers to **forward data based on labels instead of IP addresses**, which speeds up routing and improves reliability. It supports **QoS (Quality of Service)** for critical applications and can carry multiple protocols (IP, Ethernet, etc.), making it a scalable and secure option for connecting multiple business sites. It is like a VIP express lane for your data that changes dynamically in real-time based on current network conditions and traffic load, using labels instead of IP addresses so that much less computation is needed at each "hop".
- **VPN** (Virtual Private Network) over public or private networks
- **SD-WAN** (Software-Defined Wide Area Network)

### Common WAN Applications

- Branch office interconnectivity
- Secure remote access for employees
- Connections to cloud platforms and datacenters
- Internet access for distributed sites
- Global enterprise communications

## Key Differences Between LAN and WAN

|**Aspect**|**LAN (Local Area Network)**|**WAN (Wide Area Network)**|
|---|---|---|
|**Coverage**|Limited area (home, building, campus)|Broad area (cities, countries, global)|
|**Speed**|High (low latency, high throughput)|Slower (higher latency due to distance and routing)|
|**Cost**|Lower implementation and maintenance cost|Higher cost, often involves leased services|
|**Security**|Easier to secure and monitor internally|Requires robust security policies and encryption|
|**Bandwidth**|Typically higher bandwidth and throughput|Bandwidth may be limited by ISP or provider plans|


## Implementation Considerations

When planning network infrastructure, consider:

- **Geographic scope**: Are you connecting a single site or multiple remote locations?
- **Bandwidth needs**: What level of performance do your applications and users require?
- **Security**: Will data traverse public networks (e.g., Internet)? Consider VPNs or encryption.
- **Cost**: Factor in equipment, cabling, licensing, and third-party service fees.
- **Scalability**: Plan for future growth in users, devices, and data volume.

Most modern organisations use a **hybrid network architecture**, where multiple LANs are connected using WAN technologies to form a unified enterprise network. This allows for secure, scalable, and efficient communication across distributed environments.