
# Understanding the TCP/IP Stack

## Overview of the TCP/IP Model

Fundamentally, **the TCP/IP model exists to describe and facilitate data moving between software, hardware, and networks**. It’s divided into four layers, each responsible for a specific part of the transmission process.

| Layer       | Description                                             | Example Protocols    |
| ----------- | ------------------------------------------------------- | -------------------- |
| Application | Provides networking capability to software applications | HTTP, DNS, FTP, SMTP |
| Transport   | Ensures data arrives correctly                          | TCP, UDP             |
| Internet    | Routes data across networks using IP addresses          | IP, ICMP             |
| Link        | Handles direct connections between physical devices     | Ethernet, Wi-Fi, ARP |

These layers work together to move data from one machine to another, whether that’s across a local network or the entire internet.

### TCP/IP Layers at the binary level

- The actual data that needs to be transmitted (For example a message from a messaging app) is a sequence of 1s and 0s. 
- During transmission, the message is attached to other sequences of 1s and 0s.
	- These sequences are **standardised structures** that allow the transmission to be interpreted at each step along its journey.
		- The specific structures attached define which layer of the TCP/IP model the data is currently passing through.
	- When the data reaches a boundary between layers, a new set of standardised structures is **added onto** the existing ones.
		- This **layering process** ensures the data can be unpacked and understood correctly, step by step, at the destination.

These **standardised structures of 1s and 0s** are called **headers** (if they come before the data), or **footers/trailers** (if they come after). Headers are always present, footers are protocol-specific and used when verification or end-of-transmission markers are required.

The **layering/adding** of headers/footers is called **encapsulation**. 

During each layer, the **encapsulated** data is called the **payload**. 

At the top layer (Application layer), the **payload** is the actual data you're sending, like the message in a text, or contents of a webpage, or the data in a file transfer.

During each **encapsulation**, the entire transmission including all headers/footers of previous layers becomes the new **payload**.



## TCP/IP Layer Summary

#### Application Layer
- User-facing
- Common protocols: HTTP, HTTPS, DNS, SMTP, FTP, SSH

#### Transport Layer
- Responsible for reliable (TCP) or fast (UDP) data delivery.
- Adds port information to identify services on each host.

#### Internet Layer
- IP (Internet Protocol) for addressing and routing.
- ICMP (used by `ping` and `traceroute`) supports troubleshooting and testing.

#### Link Layer
- Connects devices on the same network segment, uses Ethernet, Wi-Fi, or ARP for address resolution
- Uses MAC addresses to ensure specific device connections.



## Next Steps

Future additions:
- TCP handshakes and retransmission
- ARP and MAC address resolution
- NAT, subnetting, and fragmentation
- Examples of packet captures (Wireshark)
- Troubleshooting examples at each layer




