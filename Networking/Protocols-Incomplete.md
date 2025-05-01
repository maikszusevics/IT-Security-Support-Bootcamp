# Protocols

Protocols are **sets of rules**. **Network protocols** are needed to ensure that data is sent, received, and understood properly.


## IP Addressing

- Every device on a network has an **IP address**.
- Two types:
  - **Dynamic IPs**: Temporarily assigned by a DHCP server.
	  - Used for most clients
  - **Static IPs**: Manually set and remain fixed.
	  - Used for shared devices (Printers, Servers, IoT devices)


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


## ARP

- Enables devices on the same local network to discover each other's MAC addresses.
	- Device A needs to communicate with Device B on the same network, it needs Device B's MAC address
	- Device A checks its ARP cache first to see if it already knows the MAC address
	- If not, Device A broadcasts an ARP request to the entire network saying "Who has IP address x.x.x.x?"
	- Device B, recognising its own IP address in the request, responds directly to Device A saying "That's my IP address! My MAC address is xx:xx:xx:xx:xx:xx"
	- Device A updates its ARP cache with this information and can now communicate directly with Device B
## TCP

## UDP

## HTTP/HTTPS

## FTP

## ICMP

