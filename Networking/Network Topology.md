# Network Topologies

**Network topology** refers to the _logical structure_ or layout of how devices (nodes) are interconnected in a network.

> Note: A network’s **logical topology** (how data flows) may differ from its **physical topology** (how cables and devices are physically arranged).

Understanding topologies is essential for designing networks that meet requirements for performance, scalability, fault tolerance, and cost.

## Common Network Topologies

Several topologies are used in modern and legacy networks. Each has its own advantages and trade-offs:

### 1. Star Topology

A **Star topology** is one of the most widely used configurations in both home and enterprise networks.

- All devices (nodes) are connected to a **central device**, typically a **switch** or **hub**.
- The central device manages network traffic and communication between endpoints.

#### Advantages

- **Centralized Management**: The central switch simplifies monitoring, troubleshooting, and configuration.
- **Fault Isolation**: If a single node or its connection fails, the rest of the network remains operational.
- **Scalability**: Easy to add or remove devices without disrupting the network.

#### Disadvantages

- **Single Point of Failure**: If the central switch or hub fails, the entire network becomes inoperable.
- **Hardware Dependency**: The network's performance and capacity are limited by the central device’s capabilities.


### 2. Mesh Topology

A **Mesh topology** involves every device being connected directly to every other device.

- Commonly used in **mission-critical systems** where **redundancy** and **high availability** are essential.
- Can be **fully meshed** (every node connected to every other) or **partially meshed** (only some nodes have multiple connections).

#### Advantages

- **Fault Tolerance**: If one link or device fails, alternative paths are available for data to travel.
- **High Availability**: Ideal for environments requiring uninterrupted connectivity, such as data centers or backbone networks.

#### Disadvantages

- **High Cost**: Requires a large number of cables and network interfaces.
- **Complex Setup and Maintenance**: Configuration and troubleshooting can be difficult in large implementations.


## Other Topologies (Brief Overview)

> These are less commonly used today but are still important for understanding legacy systems and specific use cases.

### 3. Bus Topology

- All devices share a single communication line (backbone).
- Simple and inexpensive, but difficult to troubleshoot and scale.
- A fault in the main cable can bring down the entire network.

### 4. Ring Topology

- Devices are connected in a circular loop, each device linked to two others.
- Data travels in one direction or bidirectionally (dual-ring).
- Failure in one node can disrupt the entire network unless fault tolerance is built in.

## Summary Comparison

| Topology | Fault Tolerance | Cost     | Scalability  | Common Usage               |
| -------- | --------------- | -------- | ------------ | -------------------------- |
| Star     | Medium          | Moderate | High         | Offices, homes             |
| Mesh     | High            | High     | Low-Moderate | Data centers, military     |
| Bus      | Low             | Low      | Low          | Legacy LANs                |
| Ring     | Low-Medium      | Moderate | Moderate     | Legacy token-ring networks |

