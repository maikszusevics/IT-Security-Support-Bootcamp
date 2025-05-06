# Operating Systems

The foundational software layer that facilitates communication between the hardware of the computer and the programs that run on it is called an operating system (OS). Allocating system resources, including the CPU, memory, storage, and input/output devices, is the responsibility of the operating system. Most modern OSes provide users with a coherent graphical user interface (GUI) to interact with the system.


## Types of Operating Systems

### Consumer Operating Systems

Accessibility is a priority in the design of these operating systems. They are designed to be user-friendly, compatible with a variety of hardware, and supportive of a large number of applications.

#### Windows

- The most widely used of all consumer OSes.
- Versions include Windows 10, Windows 11. (Windows 10 [support](https://github.com/maikszusevics/IT-Security-Support-Bootcamp/blob/main/Customer%20Support/Vendor%20Support.md) ends in October 14, 2025)
- Standard for general-purpose computing, productivity, and gaming.

#### macOS

- Developed by Apple for its Mac computers.
- Built on a [UNIX](###Kernel) foundation with an aesthetic-centric graphical user interface.
- Strong integration with Apple ecosystem.
- Known for design, security, and stability.

#### Linux (Desktop Distributions)

- Open-source and highly customisable.
- Popular distributions: Ubuntu, Fedora, Mint, Manjaro, Pop!OS, EndeavourOS
- Preferred by developers, system administrators, and privacy-conscious users.
- Offers CLI-only and GUI options.

---

### Server Operating Systems

Server OSes are optimised for high performance, reliability, and continuous operation. They are designed to manage network services, host applications, and ensure secure data handling.

#### Windows Server

- Includes features like Active Directory, IIS, and Group Policy.
	- Active Directory: A proprietary type of database developed by Microsoft for organisational IT management.  
	- Group Policy: A Windows Server tool designed to facilitate the creation and enforcing of settings and rules in the Active Directory.
	- Internet Information Services (IIS): Software designed to provide the website hosting capability to servers.  

- Ideal for organisational management.

#### Linux Server

- Includes features like LDAP, Apache/Nginx, and containerisation support.
    - LDAP (Lightweight Directory Access Protocol): A standardised protocol used as a foundation to create Linux based directories similar to Active Directory by Microsoft
    - Apache/Nginx: Open-source web server software that provides website hosting capabilities.
    - Containerisation: Native support for Docker, Kubernetes, and other container technologies for application deployment and secure isolation.

- Ideal for flexibility, customisation, and cost-effectiveness.

#### macOS Server

- Includes features like Open Directory, Profile Manager, and Xsan network file sharing.
    - Open Directory: Apple's equivalent to Active Directory.
    - Profile Manager: Apple's equivalent to Group Policy
    - Xsan: Network file system for sharing storage volumes across multiple Mac systems.

- Ideal for managing Apple-centric environments and creative workflows.

---

### Mobile Operating Systems

Mobile OSes are designed for portable devices. They are optimised for touchscreen interaction, power efficiency, and wireless connectivity.

#### Android

- Developed by Google; the most popular mobile OS worldwide.
- Open-source with heavy OEM customisation.
- Most popular mobile OS.

#### iOS

- Developed by Apple for iPhones and iPads.
- Known for performance, security, and particular user experience.
- Closed source ecosystem

#### Fuchsia (Google)

- An experimental OS built from scratch (not based on Linux).
- Uses Zircon kernel.
- Intended to unify various device platforms (IoT, Mobile) under one OS.

#### Windows Mobile (Discontinued)

- Microsoft’s attempt at a mobile OS, discontinued in favor of focusing on Android integration.

#### Symbian (Discontinued)

- Once widely used, especially on Nokia phones.
- Superseded by Android and iOS.

---

### Web-based / Cloud Operating Systems

These OSes run primarily through the cloud and are accessed via web browsers. They require minimal local resources and are maintained remotely.

#### Chrome OS (Google)

- Lightweight OS built around the Chrome browser.
- Used in Chromebooks, popular in education and enterprise.
- Pros: Fast, secure, long battery life, low hardware demands.
- Cons: Limited offline functionality, not suited for high-end applications or gaming.

#### Windows 365 (Microsoft)

- Cloud-based Windows desktop delivered over the internet.
- Hosted on Microsoft Azure.
- Pros: Scalable, secure, accessible from any device, integrates with Azure tools.
- Cons: Subscription-based, limited performance for intensive tasks.

#### webOS (LG)

- Originally created for smartphones, now used in smart TVs and IoT devices.
- HTML5-based, supports multitasking and web apps.
- Pros: Lightweight, intuitive interface, optimised for media.
- Cons: Limited app ecosystem, mainly LG-exclusive.

---

### IoT Operating Systems

IoT OSes are designed for embedded systems and devices with limited computing power. They often serve as programmable controllers over networks.

- Lightweight, real-time, and energy-efficient.
- Common examples: TinyOS, RIOT OS, and embedded versions of Linux.
- Act like programmable logic controllers (PLCs) with internet connectivity.
- Fuchsia is an operating system designed to be used in both mobile devices and IoT devices
---

## Key Components of an Operating System

### Kernel

The kernel is the foundational component of every operating system, serving as the core that controls all basic functions. It loads first during startup and is in memory throughout system operation.  
  
**Kernel Space vs. User Space:**  
  
- **Kernel Space**: A protected memory area where the kernel executes with privileged access to hardware and system resources. Code running here has unrestricted access to the CPU and memory.  
- **User Space**: Where regular applications run with limited privileges. Programs in user space must request kernel services through system calls when they need to access hardware or perform privileged operations.  
  
**Types:**  
  
- **Monolithic Kernels**: All services run in the kernel space, providing direct access to resources  
- **Microkernels**: Minimal functionality in the kernel space, with most services and applications in user space  
- **Hybrid Kernels**: Blend both approaches for balance between performance and security  
  
**Primary Functions:**  
  
- **Memory Management**: Controls memory allocation for system processes and applications  
- **Process Management**: Schedules and coordinates program execution  
- **Device Management**: Enables I/O with hardware through device drivers  
- **File System Operations**: Manages data storage and retrieval  
  
**Security Aspects:**  
  
- Kernel vulnerabilities are particularly serious as they can affect the entire system  
- Separation between kernel space and user space provides essential security boundaries  
- Kernel exploits often target breaking this separation to gain elevated privileges  
  
#### Notable Kernels  
  
- **Unix Kernel**: The original kernel that established the foundation for modern operating systems.  
  
- **Linux Kernel**: The most widely used open-source kernel, powers Linux distributions, Android devices, and many embedded systems.  
  
- **Windows NT Kernel**: Microsoft's proprietary hybrid kernel that powers all modern Windows operating systems.  
  
- **BSD Kernel**: A Unix-derived kernel that focuses on stability and security, used in FreeBSD, OpenBSD.  
  
- **XNU Kernel**: Apple's hybrid kernel that powers macOS, iOS, iPadOS, watchOS, and tvOS. Incorporates a significant portion of FreeBSD kernel environment.  
  
- **Zircon**: Google's microkernel that powers the Fuchsia operating system, designed with modern devices and security in mind.
### Drivers

Drivers are software that allows the OS to communicate with hardware peripherals (e.g., printers, keyboards, GPUs).

- Without drivers, hardware can't function correctly.
- Keeping drivers updated is essential for security and performance.

### Operating System Architecture

- **32-bit (x86[^1])**: Supports up to 4GB RAM; used in older hardware.
    
- **64-bit (x64)**: Supports large memory addressing; used in modern systems.
    
- RISC (ARM, RISC-V): Reduced instruction set computing (RISC) architecture, standard in mobile and embedded devices. Offers great power efficiency.
    
    - ARM has recently resurged in consumer computing, primarily due to Apple's M-series chips, which demonstrated that ARM-based processors can deliver exceptional performance in desktop and laptop environments while maintaining superior power efficiency compared to CISC (Complex Instruction Set Computer) alternatives.
        This success has influenced the market, with companies like Qualcomm developing competitive ARM chips for Windows devices (Snapdragon X Elite), and even Microsoft creating custom ARM processors. The recent industry shift represents a looming challenge to Intel and AMD's traditional traditional x86 dominance in personal computing.
        
[1]: When people contrast "x86" with "ARM" or "RISC-V" today, they're typically referring to the entire Intel/AMD architecture family (which is CISC-based) versus other RISC-based systems like ARM or RISC-V, regardless of whether they're specifically talking about 32-bit or 64-bit implementations.
---

## File and Folder Structures

### Windows

- Uses NTFS (new tech file system)
- Uses drive letters (e.g., C:, D:).
- Root directory usually C:.
- Common directories: Program Files, Users, Windows.

### Linux

- Uses
- Root directory is "/".
- Follows a hierarchical structure.
- Common directories: /bin, /etc, /home, /var, /usr.

---

## User Interfaces

### GUI (Graphical User Interface)

- Visual interface using windows, icons, menus, and pointers.
- Easier for most users.
- Examples: Windows Explorer, macOS Finder, GNOME.

### CLI (Command Line Interface)

- Text-based interface.
- Offers powerful control and scripting capabilities.
- Some OSes are CLI only
	- MS-DOS (Microsoft OS before windows)
	- Early Unix versions 
	- Minimal Linux distributions
		- Alpine Linux
		- Arch Linux (base install)
- Examples: Windows CMD, PowerShell, Linux Bash.

---

## Operating System Hardening

Hardening is the process of securing an OS against vulnerabilities.

- Regularly update and patch.
- Remove unnecessary services and software (bloatware).
- Implement firewalls and antivirus.
- Use encryption and strong authentication.
- Kernel hardening techniques 
	-  1. Address Space Layout Randomization (ASLR)
		- Randomly arranges memory addresses used by the system
		- Like rearranging furniture so an intruder can't find things in the dark
	- 2. Privilege Separation
		- Divides the kernel into parts with different permission levels
		- Similar to having separate keys for different rooms in a building
	- 3. Kernel Module Signing
		- Only allows trusted code to be loaded into the kernel
		- Like checking ID before allowing entry to a secure building
	- 4. Secure Boot
		- Verifies system integrity before starting up
		- Ensures the system hasn't been tampered with, like a tamper-evident seal
---


