# Wired and Wireless Networking

Computer networks can be classified into two broad categories based on the medium used for data transmission: **wired** and **wireless**. Each has its own standards, use cases, advantages, and trade-offs.

## Understanding IEEE Standards

The **Institute of Electrical and Electronics Engineers (IEEE)** is a professional organisation that develops and maintains international standards for a wide range of technologies, including networking.

In the context of networking, IEEE standards ensure **interoperability**, **consistency**, and **reliability** across devices and systems from different manufacturers.

### Common IEEE Networking Standards

| IEEE Standard | Description                         | Example Use Cases                       |
| ------------- | ----------------------------------- | --------------------------------------- |
| IEEE 802.3    | Defines **Ethernet** standards      | Wired LANs using RJ45 and CAT cables    |
| IEEE 802.11   | Defines **WiFi** wireless standards | Wireless LANs in homes and offices      |
| IEEE 802.1X   | Network access control and security | Enterprise authentication (e.g. RADIUS) |
| IEEE 802.15   | Wireless Personal Area Networks     | Bluetooth, Zigbee, IoT devices          |

These standards are critical for ensuring that networked systems can **communicate reliably** and **scale efficiently**, regardless of vendor or platform.

## Wired Networking

Wired networking relies on **physical cables** to transmit data between devices, ensuring stable, secure, and high-speed communication.

### Ethernet

- **Ethernet** is the most widely used LAN (Local Area Network) technology.
- Operates based on the **IEEE 802.3 standard**.
- Offers predictable and consistent speeds, low latency, and minimal interference.

#### Key Concepts

- **Twisted Pair Cabling**:
    
    - Most Ethernet networks use **Category (Cat) cables** such as **Cat5e, Cat6, Cat6a, Cat7**, and **Cat8**.
    - Each cable contains **four twisted pairs** (8 wires total).
    - Twisting reduces **Electromagnetic Interference (EMI)** and crosstalk between pairs.

- **RJ45 Connector**:
    
    - The standard connector used for Ethernet is **RJ45 (Registered Jack 45)**
    - RJ45 has **8 pins**, corresponding to the 8 wires inside the twisted pair cable.
    - Proper wiring order is required to follow standards like **TIA/EIA-568A or 568B**.

#### CAT Cable Types

| Category | Max Speed  | Max Distance  | Shielding        | Use Case                          |
| -------- | ---------- | ------------- | ---------------- | --------------------------------- |
| Cat5e    | 1 Gbps     | 100 meters    | Unshielded       | Standard office/home networking   |
| Cat6     | 1-10 Gbps  | 55-100 meters | Usually shielded | Higher-speed networks, PoE        |
| Cat6a    | 10 Gbps    | 100 meters    | Shielded         | Data centers, enterprise use      |
| Cat7     | 10 Gbps+   | 100 meters    | Fully shielded   | Industrial and specialized setups |
| Cat8     | 25-40 Gbps | ~30 meters    | Fully shielded   | High-performance server rooms     |

#### Fibre Optic Cabling

- Uses light signals through glass or plastic fibers.
- Offers **extremely high bandwidth** and **long-distance transmission** (kilometres without signal degradation).
- Immune to EMI, ideal for backbone infrastructure.
- More expensive and requires specialised connectors like **SC**, **LC**, or **ST**.

## Wireless Networking

Wireless technologies use **radio frequency (RF)** or **infrared (IR)** to transmit data over the air, eliminating the need for cables.

### WiFi (IEEE 802.11)

- The wireless equivalent of Ethernet for LANs.
- Operates under the **IEEE 802.11 family of standards**.
- Typically uses **2.4 GHz** and **5 GHz** frequency bands (with newer standards supporting **6 GHz**).

| Standard          | Frequency Band  | Max Speed (Theoretical) | Notes                      |
| ----------------- | --------------- | ----------------------- | -------------------------- |
| 802.11n           | 2.4 / 5 GHz     | ~600 Mbps               | Widely used, good coverage |
| 802.11ac          | 5 GHz           | ~1.3 Gbps               | Higher speed, less range   |
| 802.11ax (WiFi 6) | 2.4 / 5 / 6 GHz | ~9.6 Gbps               | Improved efficiency, OFDMA |

#### Advantages of WiFi

- No cables: ideal for mobile and flexible setups.
- Easy to scale and extend using access points (APs).
- Suitable for home, public, and enterprise environments.

#### Disadvantages

- Subject to **interference** from walls, devices, and other RF sources.
- **Lower security** compared to wired unless properly configured.
- Performance may degrade with many connected clients.

### Bluetooth

- Designed for **short-range** communication (typically 10m-100m).
- Operates in the **2.4 GHz** ISM band.
- Used for **personal area networks (PANs)**, such as    
    - Wireless headphones
    - Keyboards/mice
    - File sharing between mobile devices

#### Versions and Speeds

|Version|Max Speed|Range|Notes|
|---|---|---|---|
|4.0 (LE)|~1 Mbps|~50m|Low power for IoT and wearables|
|5.0|~2 Mbps|~100m|Improved range and speed|
|5.3|Varies|Up to 200m|Latest with better efficiency|

## Zigbee

Zigbee is a **low-power, low-data-rate wireless communication protocol** designed for **IoT and automation**. It is commonly used in **home automation systems**, **sensor networks**, and **industrial monitoring**.

- Based on the **IEEE 802.15.4 standard**
- Operates primarily on **2.4 GHz**, with regional sub-GHz variants
- Designed for **mesh networking**, allowing devices to relay signals and increase range and resilience
- Typical data rates are **20-250 kbps**

### Advantages of Zigbee

- **Ultra-low power consumption** - battery life can last for years
- Supports **thousands of nodes** in a single network
- Ideal for **low-bandwidth, infrequent communication** (e.g., turning on a light)
- **Self-healing mesh** - automatically reroutes around failed nodes

### Disadvantages of Zigbee

- **Very low data rates** - not suitable for video, audio, or real-time high-volume data
- **Shorter range per hop** (10-100m), though mesh can extend it
- **Limited compatibility** - requires Zigbee-capable hubs or bridges (e.g., Philips Hue, Home Assistant)

## Summary Comparison Table

| Feature                     | Ethernet (Wired)                     | WiFi (Wireless LAN)                 | Bluetooth (PAN)                  | Zigbee (IoT)                     |
| --------------------------- | ------------------------------------ | ----------------------------------- | -------------------------------- | -------------------------------- |
| Speed (Max)                 | Up to 40 Gbps (Cat8)                 | Up to 9.6 Gbps (WiFi 6)             | Up to 2 Mbps                     | Up to 250 kbps                   |
| Range                       | Up to 100m (Cat6), longer for fibre  | ~100m (WiFi 6), varies by obstacles | ~100m (Bluetooth 5.x)            | ~10-100m per hop                 |
| Power Consumption           | High (wired)                         | Medium                              | Low                              | Very Low                         |
| Latency                     | Very Low                             | Moderate                            | Moderate                         | Low                              |
| Network Type                | LAN                                  | WLAN                                | PAN                              | WPAN / Mesh                      |
| Scalability                 | Medium                               | High (with APs)                     | Low                              | Very High (thousands)            |
| Topology Support            | Star                                 | Star (via APs)                      | Point-to-point / star            | Mesh                             |
| Interference Susceptibility | Very Low                             | Medium                              | Medium                           | Low                              |
| Use Case Examples           | Office networks, servers, Gaming PCs | Homes, offices, public WiFi         | Wearables, headsets, peripherals | Smart homes, sensors, automation |
