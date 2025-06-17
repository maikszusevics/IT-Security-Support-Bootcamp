# Protocol Data Unit

## What is a PDU?

A **Protocol Data Unit (PDU)** is a term used in networking to refer to a single unit of data that is **transmitted between networked systems**. Each layer of the **OSI (Open Systems Interconnection)** model has its own specific type of PDU, which represents how data is handled and encapsulated at that layer.

> A PDU is just a fancy term for "a chunk of data" at a specific stage of network communication.

---

## PDUs by OSI Layer

Each layer of the OSI model has a corresponding PDU:

|OSI Layer|PDU Name|Example Protocols|Description|
|---|---|---|---|
|Layer 7: Application|Data|HTTP, FTP, SMTP|Human-facing data, like a web page or an email.|
|Layer 6: Presentation|Data|TLS, SSL, JPEG|Data format translation, encryption, compression.|
|Layer 5: Session|Data|NetBIOS, RPC|Manages sessions/connections.|
|Layer 4: Transport|Segment (TCP) / Datagram (UDP)|TCP, UDP|Ensures reliable or unreliable data transfer.|
|Layer 3: Network|Packet|IP, ICMP|Provides logical addressing and routing.|
|Layer 2: Data Link|Frame|Ethernet, PPP|Physical addressing (MAC), error detection.|
|Layer 1: Physical|Bits|Electrical/RF Signals|Transmits raw binary data over the medium.|

---

## Summary of Common PDU Types

### 1. **Bits (Physical Layer)**

- Pure binary (1s and 0s) sent over cables or wireless signals.
- Literally just voltages (5V/0V), light pulses, or radio waves.

### 2. **Frames (Data Link Layer)**

- Contains MAC addresses and error-checking info (FCS).
- Example: An Ethernet frame with source and destination MACs.

### 3. **Packets (Network Layer)**

- Contains IP addresses.
- Handles logical routing through a network.
- Example: An IPv4 packet with source/destination IPs and a TTL.

### 4. **Segments / Datagrams (Transport Layer)**

- **TCP Segment**: Contains sequence numbers, ACKs, ports, etc.
- **UDP Datagram**: Simpler, faster, no guarantee of delivery.

### 5. **Data (Upper Layers)**

- What you interact with as a user, your actual file, message, or stream.

---

## Encapsulation: Wrapping Data in Layers

PDUs are like nesting dolls:  
Each layer **encapsulates** the data from the layer above it.

For example:

- Application data → Encapsulated in a TCP segment → Put inside an IP packet → Wrapped in an Ethernet frame → Sent as bits over the wire.

This wrapping is **essential for delivering data correctly** through complex networks.

---

## De-encapsulation: Unwrapping on Arrival

At the receiving end, each layer **unpacks** the data:

1. Physical layer receives bits
2. Data Link layer reconstructs frames
3. Network layer identifies IP routing
4. Transport layer manages delivery and error checking
5. Application layer hands it off to the user

---

## Why PDUs Matter

- **Troubleshooting**: Understanding PDUs helps pinpoint where data fails (e.g. "Packet not reaching destination? Check Layer 3.").
- **Security**: Inspecting PDUs is core to packet sniffing, firewall rules, and intrusion detection.
- **Efficiency**: Optimising communication involves knowing the overhead introduced by each layer.
- For networking roles, being comfortable **visualizing PDUs and OSI layers** is a must. Every time a packet goes wrong, it's usually a PDU issue at one layer or another.

---

## Bonus: Real-World Tools that Work with PDUs

|Tool|Layer Focus|What it Does|
|---|---|---|
|Wireshark|L2–L7|Packet capture and analysis|
|Ping|L3|Tests IP connectivity via ICMP packets|
|Traceroute|L3|Shows route of packets via TTL|
|Netstat|L4|Displays active TCP/UDP sessions|
|Tcpdump|L2–L4|CLI packet sniffer|
