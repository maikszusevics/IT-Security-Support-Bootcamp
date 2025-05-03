# Software

This document outlines key software concepts relevant to IT support, system administration, and cybersecurity roles.

## Application Types

- **Desktop Applications**: Installed and run on a user's computer.
- **Web Applications**: Accessed via browsers using HTML, CSS, JavaScript.
- **Databases**: Structured systems for storing and querying data.
- **APIs**: Interfaces enabling communication between software components.

## Programming and Markup Languages

- **Object-Oriented Programming (OOP)** is widely used in modern software development. Languages like Python, Java, and C# support OOP principles such as encapsulation, and inheritance.
- **Markup Languages** like HTML and XML are designed to be human-readable and use simple syntax involving tags.

### Website Development – House Analogy

- **HTML** – The foundation of the house (structure).
- **CSS** – The interior design (styling, appearance).
- **JavaScript** – The moving parts (interactivity like doors and windows).
  
**Client-side**: HTML, CSS, JavaScript  
**Server-side**: PHP, Node.js, etc.

## Data Traffic & Data Sources

### Common Forms of Data Traffic

- Video/Audio streaming
- API calls
- HTTP/HTTPS web traffic
- File transfers (e.g., FTP)
- DNS resolution requests
- General network protocol traffic

### Data Sources

Applications often interact with multiple data sources, including:
- Databases
- Web services
- External APIs

These sources may contain **sensitive data**, requiring protection through encryption and secure transmission.

## Data Security – The Three States of Data

| State        | Description                                                  | Protection Method         |
|--------------|--------------------------------------------------------------|---------------------------|
| **At Rest**  | Stored data on disk                                          | BitLocker, full-disk encryption |
| **In Transit** | Data being transferred between systems                      | VPN, TLS/SSL              |
| **In Process** | Data being actively used in memory or CPU                   | TPM (Trusted Platform Module) |

**TPM** stores encryption keys securely and creates a trusted execution environment.


## Windows Deployment Services (WDS)

- WDS automates OS installations across a network.
- Useful for provisioning both physical and virtual machines.
- Ideal for deploying standardized system images across organizations.


## APIs (Application Programming Interfaces)

APIs enable seamless communication and functionality integration between software components.

### Types of APIs

- **Web APIs** – Use web protocols (HTTP/S) for communication.
- **Library APIs** – Provide a set of callable functions with documentation, can operate in offline environments.
- **Operating System APIs** – Allow applications to interface with the OS.
- **Hardware APIs** – Provide access to physical components and peripherals.

### API Analogy – Restaurant

| Component        | Analogy                                      |
|------------------|----------------------------------------------|
| Application      | Customer ordering a meal                     |
| OS API           | Waitstaff taking the order                   |
| Driver           | Chef preparing the meal                      |
| Hardware API     | Kitchen equipment (stove, pans, etc.)        |
| Final Experience | Customer enjoying the dish                   |

