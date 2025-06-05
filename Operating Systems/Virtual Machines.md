# Virtual Machines

**Virtualisation** is a technology that allows multiple operating systems (OS) to run efficiently on a single physical machine. This is achieved by creating **virtual machines (VMs)**, which are software-based emulations of physical computers.

#### Understanding Virtualisation

A **virtual machine** is a software-defined computer system that shares the hardware resources of a single physical server, yet operates as an independent system. This capability allows for greater optimisation of hardware resources by enabling a single physical machine to host numerous isolated environments.

#### Hypervisors: The Foundation

At the core of virtualisation is the **hypervisor**, sometimes referred to as a **Virtual Machine Monitor (VMM)**. A hypervisor is a layer of software or firmware that creates and runs virtual machines. It manages the underlying physical hardware and allocates resources to each VM, ensuring they operate independently without interfering with each other.

Hypervisors are broadly categorised into two types:

- **Type 1 Hypervisors** (Bare-Metal): These run directly on the host hardware, without a host operating system. They are common in enterprise server environments for their performance and security. Examples include VMware ESXi and KVM.
- **Type 2 Hypervisors** (Hosted): These run as an application on a conventional operating system (e.g., Windows, macOS, or Linux). They are typically used for desktop virtualisation or testing environments. An example is VirtualBox.

Technologies like Intel VT-x and AMD-V provide **hardware support for CPU virtualisation**, which significantly reduces the overhead of running virtual machines, allowing them to achieve near-native performance.

#### Core Components of a Virtual Machine

To function, each virtual machine requires virtualised versions of key hardware components:

- **CPU Cores**: Virtual processors that enable the VM to execute instructions.
- **RAM (Memory)**: Allocated portion of the physical host's memory for the VM's operations.
- **Storage**: Virtual disks that can reside on the host's physical storage, appearing as local drives to the VM.
- **NIC (Network Interface Card)**: A virtual network adapter that allows the VM to connect to networks.

These virtual components are managed by the hypervisor, abstracting the underlying physical hardware from the virtual machine, which simplifies complexity and allows systems to be built in layers.

#### Containerisation: A More Focused Approach

While related to virtualisation in enabling isolated environments, **containerisation** offers a different approach, focusing on application deployment and secure isolation. Unlike VMs, which encapsulate an entire operating system, containers share the host OS kernel and virtualise the OS at a higher level.

- **Key Technologies**: Popular container technologies include Docker and Kubernetes.
- **Purpose**: They provide native support for deploying applications in isolated environments, ensuring consistency across different computing environments from development to production. This approach is ideal for flexibility, customisation, and cost-effectiveness, especially for server roles like web servers.

#### Benefits of Virtualisation

Virtual machines and virtualisation technologies offer several significant advantages in IT environments:

- **Resource Optimisation**: Multiple workloads can run on a single physical server, increasing hardware utilisation and reducing capital expenditure.
- **Flexibility and Scalability**: VMs can be easily provisioned, moved, and scaled up or down to meet changing demands.
- **Isolation and Security**: Each VM operates in its own isolated environment, preventing applications in one VM from affecting others on the same host.
- **Disaster Recovery**: Snapshots and easy replication of VMs simplify backup and recovery processes, enhancing disaster recovery planning.
- **Testing and Development**: VMs provide a safe, isolated environment for testing new software, configurations, or security patches without impacting production systems.