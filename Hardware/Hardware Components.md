# Hardware Components


## Motherboard

**Chipset**  
The chipset is a set of integrated circuits that manage data flow between the CPU, RAM, storage, and peripherals. It determines which processors, memory types, and expansion cards are compatible with the motherboard and influences overall system capabilities.

**CMOS**  
Complementary Metal-Oxide-Semiconductor (CMOS) is a small amount of memory that stores basic system configuration, including date, time, and hardware settings. It's powered by a battery to retain information when the computer is powered off, allowing the system to remember its configuration between boots.

**PCIe**  
Peripheral Component Interconnect Express (PCIe) is a high-speed serial computer expansion bus standard that provides dedicated point-to-point connections between components. PCIe slots on motherboards allow for installation of graphics cards, sound cards, network adapters, and storage devices, with different generations (PCIe 3.0, 4.0, 5.0) offering increasing bandwidth.

**Northbridge**  
The Northbridge traditionally controlled high-speed components like the CPU, RAM, and PCIe lanes. In modern architectures, most Northbridge functions have been integrated into the CPU itself, but the concept represents the high-speed controller hub of the motherboard architecture.

**Southbridge**  
The Southbridge manages slower peripherals and I/O connections such as USB, SATA, audio, and network interfaces. It communicates with the CPU through the Northbridge (in older designs) or directly (in newer designs) and handles lower-bandwidth tasks.

**Input/Output**  
Motherboards provide various I/O ports for connecting peripherals, including USB, audio jacks, display outputs, network ports, and legacy connections. These interfaces are typically clustered in an I/O panel at the rear of the motherboard and may be supplemented by headers for front-panel connections.

**POST**  
Power-On Self-Test (POST) is a diagnostic testing sequence run by firmware when the computer is powered on. It checks critical hardware components like CPU, RAM, and storage devices before booting the operating system. If issues are detected, the system may display error codes or emit beep patterns to indicate the problem.

**BIOS/UEFI**  
Basic Input/Output System (BIOS) or Unified Extensible Firmware Interface (UEFI) is firmware stored in non-volatile memory that initializes hardware during boot and provides runtime services to the operating system. UEFI is the modern replacement for BIOS, offering a graphical interface, faster boot times, support for larger drives, and enhanced security features like Secure Boot.

## CPU 

**ALU**  
The Arithmetic Logic Unit performs mathematical operations (addition, subtraction) and logical operations (AND, OR, NOT). It's the computational workhorse of the CPU, executing calculations needed for program execution and data manipulation.

**CU**  
The Control Unit coordinates CPU operations by fetching instructions from memory, decoding them, and directing other components to execute them. It manages the timing and sequence of operations, ensuring instructions are processed correctly and in order.

**Registers**  
Registers are small, high-speed storage locations within the CPU that hold data being processed. They include general-purpose registers for calculations, special-purpose registers like the Program Counter (which tracks the next instruction), and status registers that maintain CPU state information.

**Instruction Set**  
The instruction set is the collection of commands a CPU can execute, defining its capabilities. Common architectures include x86, x86-64 (AMD64), and ARM. Each instruction performs operations like data movement, arithmetic, logic, or control flow, forming the CPU's "language."

**Frequency**  
CPU frequency (measured in GHz) represents the number of clock cycles per second. Higher frequencies generally mean faster processing, though modern performance also depends on architecture efficiency, core count, and cache size. Turbo boost technologies can temporarily increase frequency for demanding tasks.

**Cores**  
CPU cores are independent processing units within a single processor. Multi-core processors can execute multiple instructions simultaneously, improving performance for multi-threaded applications and multitasking. Modern CPUs typically have 4-16 cores in consumer products and more in server-grade processors.

**Threads/Hyperthreading**  
A thread is a sequence of instructions that can be managed independently by the CPU scheduler. Hyperthreading (Intel) or Simultaneous Multithreading (AMD) allows a single physical core to run two threads simultaneously by duplicating certain portions of the processor, improving efficiency when one thread is waiting for resources.

**Virtualisation**  
CPU virtualisation features enable efficient running of virtual machines by providing hardware support for isolating and managing multiple operating systems on one physical machine. Technologies like Intel VT-x and AMD-V reduce the overhead of virtualisation, allowing near-native performance for virtual machines.

**Cache**  
CPU cache is high-speed memory built into the processor to reduce data access times. It's organised in levels (L1, L2, L3) with L1 being smallest but fastest and L3 being larger but slightly slower. Cache stores frequently accessed instructions and data, significantly improving performance by reducing the need to access slower main memory.
## Memory

**Volatility**  
Memory volatility refers to whether storage retains data when power is removed. Volatile memory (like RAM) loses all stored information when powered off, while non-volatile memory (like SSDs or HDDs) preserves data without continuous power. This fundamental distinction determines how different memory types are used in computer systems.

**ROM**  
Read-Only Memory is non-volatile memory that stores permanent data, typically containing essential boot-up instructions like firmware. Unlike RAM, ROM content remains intact without power and traditionally couldn't be modified (though modern variants like EEPROM and flash memory allow for updates). ROM provides the critical initial instructions that start the computer before other systems load.

### RAM

**DDR Standard**  
Double Data Rate (DDR) standards define RAM performance characteristics, with each generation offering higher speeds and efficiency. Current standards range from DDR4 (common in most systems) to DDR5 (newer systems), with each providing increased bandwidth, lower voltage requirements, and higher maximum capacities compared to previous generations.

**RAM Channels**  
RAM channels are independent pathways between memory and the memory controller. Dual-channel, triple-channel, or quad-channel configurations multiply bandwidth by allowing simultaneous data transfers across multiple channels. To utilize multi-channel architecture, identical memory modules must be installed in matching slots, significantly improving memory throughput.

**ECC RAM**  
Error-Correcting Code memory includes additional data bits to detect and correct common memory errors. Unlike standard RAM, ECC can identify and fix single-bit errors on the fly, improving system stability and preventing data corruption. Primarily used in servers, workstations, and mission-critical systems where data integrity is essential.

## NIC

Network Interface Cards connect computers to networks by translating data between the computer and network infrastructure. Modern NICs support various speeds (1Gbps, 10Gbps, etc.), connection types (Ethernet, fiber), and advanced features like TCP offloading. Integrated NICs are built into most motherboards, while dedicated cards offer enhanced performance for specialised network-heavy use cases.

## GPU

Graphics Processing Units handle display rendering and increasingly, parallel computing tasks. Unlike CPUs, GPUs contain thousands of smaller cores optimized for simultaneous operations. They include dedicated video memory (VRAM), specialized rendering pipelines, and hardware acceleration for 3D graphics, video encoding/decoding, and compute workloads like AI and scientific simulations.

## Storage

### HDD

**PATA**  
Parallel Advanced Technology Attachment (formerly IDE) is an older interface standard for connecting storage devices. Using 40 or 80-pin ribbon cables, PATA transfers 16 bits simultaneously at speeds up to 133 MB/s. Though largely obsolete, PATA established fundamental concepts for storage interfaces and may still be found in legacy systems.

**SATA**  
Serial ATA replaced PATA with a more efficient serial connection using thinner cables and smaller connectors. SATA revisions increased speeds from 1.5 Gb/s (SATA I) to 6 Gb/s (SATA III), while adding features like hot-swapping and Native Command Queuing. SATA remains the standard connection for most HDDs, offering a balance of performance, compatibility, and cost-effectiveness.

### SSD

**SATA**  
SATA SSDs use the same interface as HDDs but deliver significantly better performance through flash memory. While limited by the SATA interface's 6 Gb/s theoretical maximum, these SSDs offer substantial improvements over HDDs in random access times and reliability. They represent an excellent upgrade path for existing systems without requiring motherboard changes.

**M.2**  
M.2 is a form factor specification for internally mounted expansion cards, commonly used for SSDs. These compact devices can utilize either SATA or NVMe protocols, with the latter offering substantially higher performance. M.2 slots support different "key" configurations and lengths (2242, 2280, etc.), with the numbers indicating dimensions in millimeters.

**PCIe**  
PCIe SSDs connect directly to the PCIe bus, bypassing traditional storage interfaces for dramatically improved performance. NVMe (Non-Volatile Memory Express) is the protocol designed specifically for these drives, reducing latency and overhead. PCIe 4.0 SSDs can achieve speeds over 7000 MB/s, making them ideal for data-intensive workloads like video editing and gaming.

## PSU

**Wattage**  
Power Supply Unit wattage indicates maximum power delivery capability, measured in watts. Proper wattage selection depends on system components, particularly CPU and GPU power requirements, with headroom for efficiency and future upgrades. Insufficient wattage can cause system instability, while excessive capacity may reduce efficiency at typical loads.

**Efficiency Standard**  
80 PLUS certification rates PSU efficiency at different load levels (20%, 50%, 100%). Tiers include Standard (80%), Bronze (85%), Silver (88%), Gold (90%), Platinum (92%), and Titanium (94% at 50% load). Higher efficiency reduces electricity consumption and heat generation, potentially lowering operating costs and improving system reliability despite higher initial purchase price.

**Modularity**  
Modularity refers to detachable power cables. Non-modular PSUs have fixed cables, semi-modular units allow some cables to be removed, and fully modular PSUs have completely detachable cables. Modular designs improve cable management, airflow, and aesthetics by eliminating unused cables, though they typically command a price premium over equivalent non-modular models.

## UPS

Uninterruptible Power Supplies provide emergency power when the main power fails, preventing data loss and hardware damage from sudden shutdowns. UPS systems include batteries that instantly take over during outages, giving time for proper system shutdown or bridging brief interruptions. Advanced models offer voltage regulation, surge protection, and management software that can automatically initiate safe shutdowns during extended outages.



