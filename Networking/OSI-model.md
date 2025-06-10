# OSI model

The **OSI (Open Systems Interconnection)** model is a **conceptual framework** that standardises how computer systems communicate over a network. It consists of **7 layers**, and each layer has a specific responsibility in the communication process.

Every layer is rule-based. At the physical layer the rules that tell us how to move data are Ethernet and wireless standards (802.3, 802.11). Protocols are rules which create standardised structures of data above the level of Ethernet standards.

## Layer 1 - Physical

- **Role**: Transmits raw binary data (1s and 0s) over a physical medium.
- **What it includes**: Hardware like cables, switches, connectors, and radio signals.
- **Examples**: Ethernet cables, fibre optics, WiFi signals.

## Layer 2 - Data Link

- **Role**: Packages raw bits into frames and manages direct node-to-node communication on the same Local Area Network (LAN).
- **Responsibilities**:
  - Basic error detection and correction
  - MAC (Media Access Control) addressing
- **Examples**: Ethernet, MAC addresses, switches.

#### Logical Link Control (LLC) Sublayer

The LLC sublayer serves as the connection point between the physical link and all higher layer protocols. It ensures that protocols like UP can function regardless of what type of physical tech is being used.

#### Media Access Control (MAC) Sublayer

MAC sublayer controls access to the physical medium, serving as a mediator if multiple devices are competing for the same link.
- CSMA/CD
	- Carrier Sense Multiple Access - Collision Detection. Used on Ethernet-based networks to detect collisions of data.
- CSMA/CA
	- Carrier Sense Multiple Access - Collision Avoidance. Used to prevent collisions of data over wireless connections.

**Ethernet Frames**

- An Ethernet Frame represents data when it is transferred around a LAN at the Data Link layer.
- Does not represent an entire email, document, video, etc. it is simply a portion of the data.
- Note at this layer the frame contains no IP address and consists solely of MAC addresses
- The protocol represents the application the data is for. For example: HTTP for a web browser. SMTP for an email client.
- The data size of an Ethernet frame will often vary, but the maximum permitted size per frame is 1518 Bytes.
- The FCS field contains a checksum value which is used by the receiving side to prove that the data is not corrupted and is collated in the correct order, the algorithm used is cyclic redundancy check

![](Images/eframe.png)


## Layer 3 - Network

- **Role**: Handles logical addressing and routing across different networks.
- **Responsibilities**:
  - Determines best path for data
  - Delivers packets across multiple networks
	  - an IP packet represents data when it is transferred at the Network Layer of the OSI Model.
	  - It takes the Ethernet Frame and adds logical addressing using IP so the data can be transported between networks.
- **Examples**: IP addresses, routers, Internet Protocol (IP).

## Layer 4 - Transport

- **Role**: Ensures reliable or fast data transfer between systems.
- **Responsibilities**:
  - Segmentation and reassembly
  - Error detection and correction
  - Flow control
- **Examples**: TCP (connection orientated **segments**), UDP (connectionless **datagrams**), port numbers.

## Layer 5 - Session

- **Role**: Establishes, manages, and ends communication sessions between applications via **source port** and **destination port**.
- **Responsibilities**:
  - Session establishment and teardown
  - Synchronisation
- **Examples**: NetBIOS, RPC (Remote Procedure Call).

## Layer 6 - Presentation

- **Role**: Translates data formats between the application and network.
- **Responsibilities**:
  - Encryption and decryption
  - Data compression
  - Format translation
- **Examples**: JPEG, GIF, MPEG, SSL/TLS.

## Layer 7 - Application

- **Role**: Interfaces directly with user-facing applications that need network access.
- **Responsibilities**:
  - Provides services like email, file transfer, web browsing
  - Ensures proper resource availability
- **Examples**: HTTP, FTP, SMTP, DNS.

### Intersection of OSI and TCP/IP

The OSI and TCP/IP models both explain network communication, but differ in structure and application. OSI is a **conceptual/theoretical** seven-layer model used for teaching and deepening understanding, while TCP/IP is a **practical** four-layer model that actually runs the internet. TCP/IP simplifies OSI by condensing its seven layers into four: Application (combining OSI's top three layers), Transport, Internet (equivalent to OSI's Network layer), and Network Interface (combining OSI's bottom two layers). OSI provides detailed theoretical understanding, while TCP/IP is more relevant for real-world network implementation and troubleshooting.

## Encapsulation

- The actual data that needs to be transmitted (For example a message from a messaging app) is a sequence of 1s and 0s. 
- During transmission, the message is attached to other sequences of 1s and 0s.
	- These sequences are **standardised structures** that allow the transmission to be interpreted at each step along its journey.
		- The specific structures attached define which layer of the TCP/IP model the data is currently passing through.
	- When the data reaches a boundary between layers, a new set of standardised structures is **added onto** the existing ones.
		- This **layering process** is called **encapsulation** and it ensures the data can be unpacked (**decapsulated**) and understood correctly, step by step, at the destination.

These **standardised structures of 1s and 0s** are called **headers** (if they come before the data), or **footers/trailers** (if they come after). Headers are always present, footers are protocol-specific and used when verification or end-of-transmission markers are required.

The **layering/adding** of headers/footers is called **encapsulation**. 

During each layer, the **encapsulated** data is called the **payload**. 

At the top layer (Application layer), the **payload** is the actual data you're sending, like the message in a text, or contents of a webpage, or the data in a file transfer.

During each **encapsulation**, the entire transmission including all headers/footers of previous layers becomes the new **payload**.


## Summary Table

| Layer | Name         | Description                                 | Examples                    |
| ----- | ------------ | ------------------------------------------- | --------------------------- |
| 7     | Application  | End-user services and network apps          | HTTP, FTP, DNS              |
| 6     | Presentation | Format translation, encryption, compression | SSL/TLS, JPEG, MPEG         |
| 5     | Session      | Manages sessions between applications       | NetBIOS, RPC                |
| 4     | Transport    | Reliable data transfer between hosts        | TCP, UDP, ports             |
| 3     | Network      | Routing and logical addressing              | IP, routers                 |
| 2     | Data Link    | Local addressing and error detection        | MAC, Ethernet               |
| 1     | Physical     | Hardware transmission of raw bits           | Cables, radio signals, NICs |


