# Packet Tracer Activity: Simple Network Build and Configuration

## Objective
Document progress in building a simple network and verifying end device connectivity using Packet Tracer.

## Part 1: Build a Simple Network

### Step 1: Devices Added
- PC added to workspace (Path: `End Devices > PC`)
![](Images/pc0.png)
- Laptop added to workspace (Path: `End Devices > Laptop`)
![](Images/laptop0.png)
- Cable Modem added to workspace (Path: `Network Devices > WAN Emulation > Cable Modem`)
![](Images/modem0.png)

### Step 2: Device Names Renamed
| Device      | New Display Name |
| ----------- | ---------------- |
| PC          | MaiksPC          |
| Laptop      | MaiksLaptop      |
| Cable Modem | LocalModem       |
- Select device -> Config -> Rename
![](Images/config.png)
![](Images/name0.png)
### Step 3: Physical Cabling
- PC connected to Wireless Router  
  - Cable Type: Copper Straight-Through  
  - PC Port: `FastEthernet0`  
  - Router Port: `Ethernet 1`

- Wireless Router connected to Cable Modem  
  - Cable Type: Copper Straight-Through  
  - Router Port: `Internet`  
  - Modem Port: `Port 1`

- Cable Modem connected to Internet Cloud  
  - Cable Type: Coaxial  
  - Modem Port: `Port 0`  
  - Cloud Port: `Coaxial 7`

![](Images/wired.png)

## Part 2: Configure End Devices and Verify Connectivity

### Step 1: PC Configuration
- DHCP enabled
![](Images/dhcp.png)
	 - Used PC desktop and Command Prompt to verify IP address received via `ipconfig -all`
	 ![](Images/cmd.png)
	 ![](Images/ipconfig.png)
- Pinged `cisco.srv`
	- Used command `ping cisco.srv`
		![](Images/ping.png)


---

### Step 2: Laptop Configuration

#### Hardware Setup
- Powered off Laptop
- ![](Images/pwr.png)
- Removed Ethernet Module
	![](Images/pwroff.png)
- Installed Wireless WPC300N Module
	![](Images/wpc.png)
- Powered on Laptop
	![](Images/pwron.png) 

#### Wireless Setup
-  Connected to `HomeNetwork` via PC Wireless
	![](Images/wirless.png)
	![](Images/hmnetwork.png)
-  DHCP enabled and IP Address received
	![](Images/lapdh.png)
	![](Images/lapip.png)
- Verified connectivity using web browser (`cisco.srv`)
	![](Images/web.png)

![](Images/final.png)

---

## Reflection and Notes
- What worked well?
	- Swapping out laptop components and using the wireless card worked flawlessly.
	- I did get a better understanding of how home networks are connected to ISP networks. I'm now able to add an explanation of modems into my network architecture folder.
- What issues did you encounter?
	- I was confused by the UI at first and used the incorrect cable types. This caused ping to fail and I had to come back another day to understand what happened.
- What would you do differently next time?
	- Take more care when reading the activity overview.


## IP Addressing Table

| Device | IPv4 Address | Subnet Mask   | Default Gateway |
| ------ | ------------ | ------------- | --------------- |
| PC     | 192.168.0.2  | 255.255.255.0 | 192.168.0.1     |
| Laptop | 192.168.0.3  | 255.255.255.0 | 192.168.0.1     |
