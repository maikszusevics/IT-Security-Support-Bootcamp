# OSI model

The **OSI (Open Systems Interconnection)** model is a conceptual framework that standardizes how computer systems communicate over a network. Think of it as a **7-layer cake**, where each layer has a specific responsibility in the communication process.

## Layer 1 – Physical

- **Role**: Transmits raw binary data (1s and 0s) over a physical medium.
- **What it includes**: Hardware like cables, switches, connectors, and radio signals.
- **Examples**: Ethernet cables, fiber optics, Wi-Fi signals.

## Layer 2 – Data Link

- **Role**: Packages raw bits into frames and manages direct node-to-node communication.
- **Responsibilities**:
  - Basic error detection and correction
  - MAC (Media Access Control) addressing
- **Examples**: Ethernet, MAC addresses, switches.

## Layer 3 – Network

- **Role**: Handles logical addressing and routing across different networks.
- **Responsibilities**:
  - Determines best path for data
  - Delivers packets across multiple networks
- **Examples**: IP addresses, routers, Internet Protocol (IP).

## Layer 4 – Transport

- **Role**: Ensures reliable or fast data transfer between systems.
- **Responsibilities**:
  - Segmentation and reassembly
  - Error detection and correction
  - Flow control
- **Examples**: TCP, UDP, port numbers.

## Layer 5 – Session

- **Role**: Establishes, manages, and ends communication sessions between applications.
- **Responsibilities**:
  - Session establishment and teardown
  - Synchronization
- **Examples**: NetBIOS, RPC (Remote Procedure Call).

## Layer 6 – Presentation

- **Role**: Translates data formats between the application and network.
- **Responsibilities**:
  - Encryption and decryption
  - Data compression
  - Format translation
- **Examples**: JPEG, GIF, MPEG, SSL/TLS.

## Layer 7 – Application

- **Role**: Interfaces directly with user-facing applications that need network access.
- **Responsibilities**:
  - Provides services like email, file transfer, web browsing
  - Ensures proper resource availability
- **Examples**: HTTP, FTP, SMTP, DNS.



## Summary Table

| Layer | Name         | Description                                  | Examples                          |
|-------|--------------|----------------------------------------------|-----------------------------------|
| 7     | Application   | End-user services and network apps           | HTTP, FTP, DNS                    |
| 6     | Presentation  | Format translation, encryption, compression | SSL/TLS, JPEG, MPEG               |
| 5     | Session       | Manages sessions between applications        | NetBIOS, RPC                      |
| 4     | Transport     | Reliable data transfer between hosts         | TCP, UDP, ports                   |
| 3     | Network       | Routing and logical addressing               | IP, routers                       |
| 2     | Data Link     | Local addressing and error detection         | MAC, Ethernet                     |
| 1     | Physical      | Hardware transmission of raw bits           | Cables, radio signals, NICs       |
