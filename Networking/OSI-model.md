# OSI model


**The OSI Model (Open Systems Interconnection)** The **OSI model** is a **conceptual framework** that standardises how computer systems communicate over a network. It is a **theoretical seven-layer model** primarily used for teaching and deepening understanding of network communication.

We'll follow the journey of data as it leaves a computer (encapsulation) and how it's processed when it arrives at its destination (de-encapsulation).

---

### Layer 7: Application Layer

- **Role:** This is the layer that interacts directly with user applications. It's what you, as the user, directly "see" and use. It provides network services to applications.
- **Responsibilities:** Identifying communication partners, determining resource availability, and synchronising communication. It's responsible for the overall availability of network resources for applications.
- **PDU (Protocol Data Unit):** Often referred to simply as **Data** or **Application Data**.
- **How data moves:** Your application (like a web browser, email client, or file transfer program) generates the raw information you want to send. This data is then passed down to the Presentation Layer (Layer 6).
- **Examples:** HTTP (for web Browse), FTP (for file transfer), SMTP (for sending email), DNS (for translating domain names to IP addresses).

---

### Layer 6: Presentation Layer

- **Role:** This layer is the "translator" or "formatter." It ensures that data is presented in a format that the receiving application can understand.
- **Responsibilities:**
    - **Data formatting and translation:** Converting data between different formats.
    - **Data encryption/decryption:** Ensuring secure communication.
    - **Data compression/decompression:** Reducing the amount of data to be transmitted.
- **PDU:** Still considered **Data** or **Application Data**, but now formatted or translated.
- **How data moves:** The Application Layer's data is formatted and potentially compressed or encrypted here. This "prepared" data is then passed down to the Session Layer (Layer 5).
- **Examples:** JPEG, GIF, MPEG (for image/video formats), SSL/TLS (for encryption).

---

### Layer 5: Session Layer

- **Role:** This layer establishes, manages, and terminates communication sessions between applications. Think of it as opening, managing, and closing a specific conversation.
- **Responsibilities:**
    - **Session establishment/teardown:** Setting up and ending communication dialogues.
    - **Synchronisation and checkpointing:** Allowing for recovery from partial failures by inserting checkpoints into the data stream. If a connection fails, the session can resume from the last checkpoint instead of starting over.
    - **Dialog control:** Determining whether communication is half-duplex (one-way at a time) or full-duplex (two-way simultaneously).
- **PDU:** Still **Data** or **Application Data**, but now part of an active session.
- **How data moves:** The Presentation Layer's data becomes part of a managed session. This session-managed data then moves down to the Transport Layer (Layer 4).
- **Examples:** Online games establish sessions for voice chat, applications like Zoom establish and manage sessions between participants.

---

### Layer 4: Transport Layer

- **Role:** Ensures reliable or fast data transfer between systems by managing end-to-end communication.
- **Responsibilities:**
    - **Segmentation/Reassembly:** Breaking down large chunks of data from the upper layers into smaller, manageable pieces (segments) for transmission, and reassembling them at the destination.
    - **Error Detection and Correction (for TCP):** Detecting lost or corrupted segments and requesting retransmission.
    - **Flow Control:** Managing the transmission rate to prevent a fast sender from overwhelming a slow receiver.
    - **Port Addressing:** Uses **port numbers** to identify specific applications or services on a host (e.g., web server on port 80, email on port 25).
- **PDU:**
    - **Segment** (for TCP - Transmission Control Protocol): Connection-oriented, reliable, ordered delivery.
    - **Datagram** (for UDP - User Datagram Protocol): Connectionless, faster, less reliable.
- **How data moves:**
    - **Encapsulation (Sending Down):** The Transport Layer takes the data from the Session Layer, adds a **Layer 4 Header** (containing port numbers, sequence numbers, etc.), creating a **Segment** (if using TCP) or a **Datagram** (if using UDP). This Segment/Datagram then becomes the payload for the Network Layer.
    - **De-encapsulation (Receiving Up):** When a Layer 3 Packet arrives, the Transport Layer removes its Layer 4 Header, checks for errors/orders (for TCP), and passes the reassembled data up to the Session Layer.
- **Examples:** TCP, UDP.

---

### Layer 3: Network Layer

- **Role:** Responsible for **addressing** and **routing data across different networks**. It determines the best path for data to travel from the source to the final destination.
- **Responsibilities:**
    - **Logical Addressing (IP Addressing):** Uses **IP addresses** to uniquely identify devices across different networks.
    - **Routing:** Determining the optimal path for data packets to reach their destination, potentially across many different intermediate networks. This is where routers operate.
    - **Packet Fragmentation:** Breaking down large packets into smaller ones if a network link has a smaller maximum transmission unit (MTU).
- **PDU:** **Packet**.
- **How data moves:**
    - **Encapsulation (Sending Down):** The Network Layer takes the Segment/Datagram from the Transport Layer, adds a **Layer 3 Header** (containing source and destination IP addresses). This newly formed unit is called a **Packet**. This Packet then becomes the payload for the Data Link Layer.
    - **De-encapsulation (Receiving Up):** When a Layer 2 Frame arrives, the Network Layer removes its Layer 3 Header, checks the destination IP, and if it's for this device, passes the Segment/Datagram up to the Transport Layer. If it's for another network, it routes it accordingly.
- **Examples:** Internet Protocol (IP), routers.

---

### Layer 2: Data Link Layer

- **Role:** Provides **node-to-node data transfer** within the **same local network segment**. It takes packets from the Network Layer and frames them for transmission over the physical medium. It also handles basic error detection and physical addressing.
- **Responsibilities:**
    - **Framing:** Encapsulating Layer 3 Packets into **Frames** by adding a header and a trailer.
    - **Physical Addressing (MAC Addressing):** Uses **MAC addresses** (Media Access Control addresses) which are unique hardware addresses for devices on a local network segment.
    - **Error Detection:** Adds a **Frame Check Sequence (FCS)** in the trailer to detect errors in transmitted bits.
    - **MAC sublayer:** controls access to the physical medium, serving as a mediator if multiple devices are competing for the same link.
		- CSMA/CD
			- Carrier Sense Multiple Access - Collision Detection. Used on Ethernet-based networks to detect collisions of data.
		- CSMA/CA
			- Carrier Sense Multiple Access - Collision Avoidance. Used to prevent collisions of data over wireless connections.
    - **Logical Link Control (LLC Sublayer):** Provides a standardised interface to the Network Layer (Layer 3). Its primary job is to **identify _which_ Network Layer protocol** (like IP, IPv6, or ARP) is encapsulated in the frame, ensuring the receiving system knows exactly where to direct that data.
- **PDU:** **Frame**.
- **How data moves:**
    - **Encapsulation (Sending Down):** The Data Link Layer takes the Packet from the Network Layer, adds a **Layer 2 Header** (with source/destination MAC addresses) and a **Layer 2 Trailer** (with FCS). This completed unit is called a **Frame**. This Frame is then passed to the Physical Layer for conversion into raw bits.
    - **De-encapsulation (Receiving Up):** The Data Link Layer receives raw bits from the Physical Layer, reassembles them into a Frame, checks the MAC address and FCS. If valid and for this device, it removes the Layer 2 Header and Trailer, passing the Packet up to the Network Layer.

	- **Note:** When using WiFi 802.11, LLC headers are also added (sending down) or removed (receiving up). However when using modern 802.3 Ethernet, the network layer protocol is already included in the Ethernet II header information.
		- **Bonus note:** LLC headers are still explicitly expected on wired networks if they use older/legacy network protocols such as IEEE 802.2
- **Examples:** Ethernet, Wi-Fi (802.11), MAC addresses, network switches.

---

### Layer 1: Physical Layer

- **Role:** This is the most basic layer, responsible for the **physical transmission of raw binary data (1s and 0s)** over the network medium.
- **Responsibilities:**
    - Defining physical characteristics of the network (e.g., voltage levels, cable types, connectors, data rates, signalling methods).
    - Transmitting and receiving raw bit streams.
    - **Converting frames into electrical signals, light pulses, or radio waves** suitable for the specific medium.
- **PDU:** **Bits** (raw binary data).
- **How data moves:**
    - **Encapsulation (Sending Down):** The Physical Layer takes the Frame from the Data Link Layer and converts it into a stream of electrical signals, light pulses, or radio waves (bits) that can travel across the physical medium (e.g., an Ethernet cable, fiber optic cable, or Wi-Fi airwaves).
    - **De-encapsulation (Receiving Up):** The Physical Layer receives these raw signals from the medium, converts them back into bits, and passes them up to the Data Link Layer to be reassembled into a Frame.
- **Examples:** Ethernet cables, fibre optic cables, Wi-Fi radio waves, USB, network interface cards (NICs).

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


