# Protocols

Protocols are **sets of rules**. **Network protocols** are needed to ensure that data is sent, received, and understood properly.
- Each protocol has a port number.

## IP Addressing

- Every device on a network has an **IP address**.
- Two types:
  - **Dynamic IPs**: Temporarily assigned by a DHCP server.
	  - Used for most clients
  - **Static IPs**: Manually set and remain fixed.
	  - Used for shared devices (Printers, Servers, IoT devices)
- IP traffic is packets.


## DHCP (Dynamic Host Configuration Protocol)

- Automates assignment and reassignment of IPs.
- Devices use DHCP to:
  1. **Discover** a DHCP server.
  2. **Receive** an IP address and lease.
  3. **Request** to use the address.
  4. **Get an Acknowledgement** confirming lease duration.

- Also used for:
  - Subnet mask
  - Default gateway
  - DNS server addresses


## DNS (Domain Name System)

- Retrieves IP addresses from domain names.
- Enables users to connect to websites by name instead of IP.

### DNS Steps:

1. Client checks local DNS cache.
2. If not found, sends request to DNS resolver.
3. Resolver contacts DNS servers.
4. IP address is returned to the client and cached.


## ARP (Address Resolution Protocol)

- Enables devices on the same local network to discover each other's MAC addresses.
	- Device A needs to communicate with Device B on the same network, it needs Device B's MAC address
	- Device A checks its ARP cache first to see if it already knows the MAC address
	- If not, Device A broadcasts an ARP request to the entire network saying "Who has IP address x.x.x.x?"
	- Device B, recognising its own IP address in the request, responds directly to Device A saying "That's my IP address! My MAC address is xx:xx:xx:xx:xx:xx"
	- Device A updates its ARP cache with this information and can now communicate directly with Device B


## TCP (Transmission Control Protocol)

- **Connection-oriented** protocol.
- Ensures **guaranteed delivery** of **segments**.
- Uses:
  - Packet sequencing
  - Acknowledgements (ACK)
  - Error checking and correction
- Examples:
  - Web browsing (HTTP/HTTPS)
  - Email (SMTP)
  - File transfer (FTP)


## UDP (User Datagram Protocol)

- **Connectionless** protocol, uses **datagrams**.
- **Faster**, but **no guarantee** of delivery, order, or error checking.
- Used for:
  - Live video/audio streaming
  - Online gaming
  - DNS queries


## HTTP / HTTPS (Hypertext Transfer Protocol / Secure)

- **HTTP**: Protocol for accessing web content.
- **HTTPS**: HTTP over SSL/TLS — adds **encryption** for secure communication.
- Operates over **TCP port 80 (HTTP)** and **443 (HTTPS)**.


## FTP (File Transfer Protocol)

- Used for transferring files between systems on a network.
- Operates over **TCP ports 20 and 21**.
- Requires authentication (username/password).
- Can be encrypted via FTPS (FTP Secure) or replaced by SFTP (SSH File Transfer Protocol).


## ICMP (Internet Control Message Protocol)

- Used for **diagnostic** and **error reporting**.
- Common use: **ping** command.
- Helps identify network connectivity issues:
  - Destination unreachable
  - Time exceeded
  - Echo request/reply (ping)

---

## Protocol Overview Table

| Protocol | Purpose / Function                             | TCP/IP Layer           |
|----------|------------------------------------------------|------------------------|
| IP       | Addressing and routing                         | Internet               |
| DHCP     | Dynamic IP assignment                          | Application            |
| DNS      | Domain name to IP resolution                   | Application            |
| ARP      | Resolves IP addresses to MAC addresses         | Network Access (Link)  |
| TCP      | Reliable, ordered data transmission            | Transport              |
| UDP      | Fast, unreliable data transmission             | Transport              |
| HTTP     | Web communication (insecure)                   | Application            |
| HTTPS    | Encrypted web communication                    | Application            |
| FTP      | File transfer between systems                  | Application            |
| ICMP     | Network diagnostics and error reporting        | Internet               |

