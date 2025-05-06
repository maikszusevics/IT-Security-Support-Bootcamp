# Network Architecture Components

### NIC (Network Interface Card)

A **Network Interface Card** (NIC) enables a computer to connect to a network.

- It lets your device send and receive data on a network, just as a mailbox lets you send and receive physical mail.
- Each NIC has a **MAC address**, like a **home address**, that uniquely identifies it.
- Can be wired (Ethernet) or wireless (Wi-Fi).
- Operates at **Layer 2** (Data Link) and sometimes **Layer 1** (Physical) of the OSI model.

### Router, Switch, and Gateway Roles

**Router**: Routes traffic between different networks.

 A **router** is like a **post office** that reads the addresses on outgoing packages and decides where to send them next.
 
- It connects different networks (e.g., your home network to the internet).
- Decides the **best route** for data packets.
- Assigns local IP addresses using **DHCP**, like handing out house numbers on a new street.
- Works at **Layer 3** (Network Layer).


**Switch**: Connects multiple devices within the same network.

- Uses MAC addresses to forward data only to the intended recipient, improving efficiency over hubs.
- Connects devices **within the same local network**.
- Operates at **Layer 2** (Data Link Layer).


**Default Gateway**: Usually a router, it routes traffic from the local network to external destinations. Front door of your house.

- The device that serves as the **exit point** from a local network to external networks.
- Devices send data to the default gateway when the destination IP is **outside** their subnet.
- Acts like the **front door** of a house—used to reach the outside world.


#### **Modem (Modulator-Demodulator)**

- Converts digital data from your device into analog signals that can be transmitted over traditional media (e.g., telephone lines, coaxial cable).
- Operates at **Layer 1** (Physical Layer).
- Acts as a bridge between your internal network and your **Internet Service Provider (ISP)**.
- Common types:
    - **DSL Modems** – Use telephone lines.
    - **Cable Modems** – Use coaxial cables.
    - **Fiber Modems** – Use optical fiber and may include media converters.
- In modern networks, modem functionality is often combined with the router in a **single device** (called a gateway or home hub).

### Additional Network Components

#### **Access Point (AP)**

- Extends a wired network by providing **wireless connectivity**.
- Usually connects to a router or switch.
- Operates at **Layer 2**, forwarding traffic between wireless clients and the rest of the LAN.

#### **Firewall**

- Can be hardware or software.
- Controls **inbound and outbound** traffic based on defined security rules.
- Often integrated into routers or gateways.
- May operate across **multiple OSI layers**, depending on implementation.

#### **Hub** (Legacy)

- Operates at **Layer 1** (Physical Layer).
- Broadcasts incoming traffic to all ports, regardless of destination.
- Largely replaced by switches due to performance and security limitations.