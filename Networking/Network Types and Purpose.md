# Types of Networks and Their Purpose

Computer networks enable the interconnection of devices for the sharing of data, resources, and services. Broadly, network architectures can be categorized into two main types:

## Network Types

### Peer-to-Peer (P2P) Networks

- In a **Peer-to-Peer network**, two or more devices are directly connected to each other without a centralised server.
- Devices act both as clients and servers, sharing resources such as files or printers.
- P2P networks are typically easy to set up and cost-effective for small-scale use.
- **Modern usage** is limited; these networks are now largely considered legacy systems, having been replaced by more scalable **Client-Server** models in most environments.

### Client-Server Networks

- In a **Client-Server network**, all devices (clients) connect to a centralised server that manages resources and services.
- Clients request services, and the server responds with the necessary data or action.
- This model enables better control, centralised security, and scalability across larger or enterprise-level networks.


## Purpose of a Network

Networks exist to fulfil several critical functions in computing environments, including:

### 1. File and Data Sharing

- Enables the transfer of files and data between systems.
- User permissions and access controls (e.g., read, write, execute) can be applied to protect data.
- Common protocols: SMB (Windows), NFS (Unix/Linux), FTP, SFTP.

### 2. Resource Sharing

- Devices on a network can share both **physical** and **logical** resources:
    - **Hardware**: Printers, scanners, storage devices, internet connections.
    - **Services**: Application servers, cloud storage, network drives.
- Reduces redundancy and costs by avoiding duplication of expensive hardware.

### 3. Centralized Administration and Maintenance

- IT administrators can perform updates, install software, and monitor systems remotely.
- Ensures uniformity in:
    
    - Software versions
    - Security patches
    - Configuration settings
- Reduces downtime and increases operational efficiency through:
    
    - **Remote administration tools**
    - **Automated deployment**
    - **Backup solutions**
- **User role hierarchy** commonly includes:
    
    - **Guest** - Limited access
    - **Standard User** - General day-to-day access
    - **Administrator** - Full access and control
    - **Superuser (Linux)** - Root-level system access

### 4. Private Communications

- Internal communication systems rely on robust networking:
    - **Email servers** (e.g., Microsoft Exchange)
    - **VOIP (Voice Over IP)** - Internet-based calling (e.g., Zoom, Skype, Google Meet)
    - **Instant Messaging Platforms** - For collaboration (e.g., Microsoft Teams, Slack)
- Secure networks ensure that communications are private and encrypted when needed.

### 5. Data Integrity, Redundancy, and Security

- Networking enables **geo-replication** - storing copies of data in multiple locations.
- Protects against data loss from:
    - Hardware failure
    - Cyber threats
    - Natural disasters
- Enhances **data integrity**, **reliability**, and **disaster recovery planning**.
- Facilitates:
    - Regular automated backups
    - Centralised threat monitoring
    - Enforcement of security policies (e.g., firewall rules, access logs)

## Summary

|Feature|Peer-to-Peer|Client-Server|
|---|---|---|
|Scalability|Low|High|
|Cost|Low|Higher initial setup|
|Central Management|No|Yes|
|Performance|Varies|More consistent|
|Security|Decentralized|Centralized and enforceable|

A well-designed network enhances productivity, communication, and security, whether in a small home setup or a large enterprise environment.