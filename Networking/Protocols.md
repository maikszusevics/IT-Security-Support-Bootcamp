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
  5. **Port 67**

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
5. Uses **port 52**


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


## NTP (Network Time Protocol)

- Synchronizes system clocks over networks.
- Uses **UDP port 123**.

## SSH (Secure Shell)

- Secure command-line access to remote systems.
- **TCP port 22**.

## SMTP (Simple Mail Transfer Protocol)

- Sends email from client to server or server to server.
- **TCP port 25**, or **587** for secure submission.

## IMAP4 (Internet Message Access Protocol v4)

- Retrieves email from server while leaving a copy there.
- **TCP port 143** (plaintext), **993** (secure/SSL).

## POP3 (Post Office Protocol v3)

- Downloads email and typically deletes it from the server.
- **TCP port 110**, **995** for POP3S (SSL).

## LDAP (Lightweight Directory Access Protocol)

- Directory access for authentication and directory services.
- **TCP port 389** (LDAP), **636** (LDAPS - secure).

## RDP (Remote Desktop Protocol)

- Remote access to Windows desktops.
- **TCP port 3389**.

## OSPF (Open Shortest Path First)

- Interior routing protocol used within an Autonomous System.
- **IP protocol number 89** (not a TCP/UDP port).

## RIPv2 (Routing Information Protocol v2)

- Distance-vector routing protocol.
- **UDP port 520**.

## EIGRP (Enhanced Interior Gateway Routing Protocol)

- Cisco proprietary routing protocol.
- Uses **IP protocol number 88**.

## Protocol Overview Table

|Protocol|Port(s)|Purpose / Function|TCP/IP Layer|
|---|---|---|---|
|IP|N/A|Addressing and routing|Internet|
|DHCP|UDP 67/68|Dynamic IP assignment|Application|
|DNS|TCP/UDP 53|Domain name to IP resolution|Application|
|ARP|N/A|Resolves IP to MAC (LAN)|Network Access (Link)|
|TCP|N/A|Reliable, ordered data transmission|Transport|
|UDP|N/A|Fast, unreliable data transmission|Transport|
|HTTP|TCP 80|Web communication (insecure)|Application|
|HTTPS|TCP 443|Encrypted web communication|Application|
|FTP|TCP 20/21|File transfer between systems|Application|
|ICMP|N/A|Network diagnostics and error reporting|Internet|
|NTP|UDP 123|Time synchronization|Application|
|SSH|TCP 22|Secure remote access|Application|
|SMTP|TCP 25/587|Sending email|Application|
|IMAP4|TCP 143/993|Email retrieval (leave on server)|Application|
|POP3|TCP 110/995|Email retrieval (download & delete)|Application|
|LDAP|TCP 389/636|Directory services and authentication|Application|
|RDP|TCP 3389|Remote desktop access|Application|
|OSPF|IP Protocol 89|Dynamic routing (intra-domain)|Internet|
|RIPv2|UDP 520|Basic dynamic routing|Application|
|EIGRP|IP Protocol 88|Cisco routing protocol|Internet|