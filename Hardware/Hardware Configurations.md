# Hardware and Hardware Configurations

Understanding the different types of computer systems, how, and ***why*** they are configured is foundational knowledge in IT support and infrastructure management. Hardware configurations can vary drastically depending on the system’s purpose.

## System Configurations

### **Desktop**

- **Fixed location**: Designed to stay in one place, typically on a desk.
- **Upgradeable**: Most important components (RAM, storage, GPU, CPU, PSU, etc.) can be replaced or upgraded. 
- **Performance-focused**: Offers more compute, better cooling, and expansion options when compared to more portable systems.
	- **Flexibility**: While it is true that performance is one of the main strengths of a desktop system, the variety of form factors available means that there are many different configurations to be made with desktops, and some may not be purely performance focused. 
		- For example: Mini-ITX is a form factor for PCs that is designed around compactness. Desktop builds using Mini-ITX form factor may be geared more towards space efficiency or aesthetics, and therefore sacrifice some of the superior cooling or performance that is associated with desktop systems.
- **Use cases**: Office workstations, gaming rigs, media creation/editing, software development, and general productivity.

### **Laptop**

- **Portable**: Combines essential hardware (screen, keyboard, battery) in a compact form.
- **Limited upgradeability**: Less and less over time. 
	- In the past laptops had socketed CPUs that could technically be swapped out for higher performance options (although this was rarely done due to power and heat considerations). But as laptops have gotten thinner, manufacturers have started integrating more and more components directly onto the motherboard via soldering, making them impossible to upgrade or replace. RAM upgrades is a more popular and accessible method of upgrading laptops, but even these components are now soldered onto many modern laptops.
		- The industry continues to move towards less user-serviceable components in laptops, although this varies significantly by manufacturer (i.e. Framework Laptops modular design)
- **Balanced**: Trades compute power for convenience and mobility.
- **Use cases**: Mobile work, students, business travel, light to moderate workloads.

### **Tablet**

- **Ultra-portable**: Thin, lightweight, and touchscreen-based.
- **Integrated OS**: Runs mobile operating systems (iPadOS, Android) or lightweight versions of desktop OS (e.g., Windows on ARM, Linux (JingOS, Ubuntu Touch)).
- **Limited multitasking and performance**: Suitable for simple tasks such as note-taking, web browsing, kiosk displays, or general entertainment.
- **Use cases**: Point-of-sale systems, education, media consumption, industrial fieldwork data entry.

### **Server**


- **Purpose-built**: Designed for continuous operation, redundancy, and high reliability.
- **Scalable**: Optimised for lots of RAM, storage, and multi-core or even dual CPU configurations.
- **Use cases**: Supports infrastructure such as websites, networks, databases, and user authentication systems.


## Common Server Roles

Each server role is specialised to handle a specific task or service within a network. A single physical or virtual server can host multiple roles, depending on its configuration and workload.

- **File & Print Server**
    - Provides centralised storage and access control for files.
    - Manages networked printer sharing and queueing.

- **DNS (Domain Name System) Server**
    - Resolves domain names (e.g., `example.com`) into IP addresses.
    - Essential for browsing the web and accessing network resources.

- **DHCP (Dynamic Host Configuration Protocol) Server**
    - Automatically assigns IP addresses to devices on a network.
    - Reduces manual configuration and ensures efficient IP address management.

- **Web Server**
    - Hosts websites, web apps, and APIs.
    - Common software: Apache, Nginx, IIS.

- **Email Server**
    - Manages sending, receiving, and storing emails.
    - Includes protocols such as SMTP (sending), IMAP, and POP3 (retrieving).

- **Virtualisation Host**
    - Runs multiple virtual machines (VMs) on a single physical server.
    - Software used includes Hyper-V, VMware ESXi, or KVM.
	    - VMs require:
		    - CPU cores
		    - RAM
		    - Storage
		    - NIC

- **Domain Controller / Active Directory (AD)**
    - Centralises authentication and access control in a Windows environment.
    - Manages user accounts, security policies, and group permissions.

- **Proxy Server**
    - Intercepts network traffic between clients and the internet.
    - Can be used to filter content, improve performance (caching), or enforce security.

- **Database Server**
    - Stores and manages structured data for applications or users.
    - Common systems: MySQL, PostgreSQL, Microsoft SQL Server, Oracle DB.