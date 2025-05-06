# Software

## Application Types

Software applications can be categorised by platform and purpose:

### By Platform

- **Desktop Applications** – Installed directly on a user's computer (e.g., Microsoft Word, Photoshop).
- **Mobile Applications** – Designed for smartphones or tablets, typically installed via app stores (e.g., WhatsApp, Spotify).
- **Web Applications** – Accessed through a browser; rely on technologies like HTML, CSS, and JavaScript (e.g., Google Docs, Trello).

### By Function

- **Productivity Applications** – Tools that help users complete tasks (e.g., Microsoft Office, Notion).
- **Entertainment Applications** – Games, media players, and streaming platforms (e.g., Steam, Netflix).
- **Communication Applications** – Enable messaging and collaboration (e.g., Zoom, Slack).
- **Utility Applications** – Support system maintenance or performance (e.g., antivirus, file managers).

## Programming and Markup Languages

High level programming languages can be learned by humans because it is human readable.

Low level programming languages are made to be understood by machines. They are a step above binary.

Software written in high level programming languages needs to be translated for the processor to be able to ready it.

Compilers and Interpreters do the translation of high level programming languages into low level programming languages (in binary)

### Programming Concepts

- **Object-Oriented Programming (OOP)** – A programming paradigm based on objects that contain data and behavior. Key principles include:
    - **Encapsulation** – Bundling data with methods.
    - **Inheritance** – Deriving new classes from existing ones.
    - **Polymorphism** – Methods behaving differently based on context.
    - Languages: Python, Java, C#, C++.

- **Common Functions in Programming**
    - `if/else` – Conditional logic
    - `while` loop – Repeats code while a condition is true
    - `for` loop – Iterates over sequences
    - `do...while` loop – Runs at least once before checking the condition

### Markup Languages

- **HTML** – Structures content on the web.
- **XML** – Used for data storage and transport with strict formatting.
- **Markdown (MD)** – Lightweight syntax for formatting text.

### JavaScript

JavaScript is a **high-level scripting language** widely used in web development for:

- Real-time content manipulation
- Interactive user interfaces
- Communicating with APIs (e.g., via `fetch` or `XMLHttpRequest`)
- Server-side development (Node.js)
- Mobile and desktop app development via frameworks (React Native, Electron)

### PHP

A server-side scripting language used for building dynamic web applications.

- Commonly embedded in HTML.
- Powers platforms like WordPress and content management systems.

### Compiled vs Interpreted Languages

Compiled languages are converted directly into machine code.
- They tend to be faster and more efficient 
- More control over hardware aspects 
- C, C++, Erlang, Haskell, Rust, Go

Interpreted languages run through a program line by line.

- Interpreted languages were once significantly slower than compiled languages. Today the gap is much closer.
- Examples of common interpreted languages are PHP, Ruby, Python, and JavaScript


## Website Development – House Analogy

Think of a website like a house:

|Component|Purpose|Analogy|
|---|---|---|
|**HTML**|Structure|The house's framework and walls|
|**CSS**|Appearance|The interior/exterior design|
|**JavaScript**|Interactivity|The moving parts – doors, switches, etc.|

- **Client-side technologies**: HTML, CSS, JavaScript – run in the user's browser.
- **Server-side technologies**: PHP, Node.js, Python – run on a web server.


## Data Traffic & Data Sources

### Common Types of Data Traffic

- **Streaming** – Continuous transmission of audio/video.
- **API Calls** – Requests between systems for data or functionality.
- **Web Traffic** – HTTP/HTTPS data sent between browsers and servers.
- **File Transfers** – E.g., FTP, SMB, or cloud syncing tools.
- **DNS Queries** – Resolving domain names to IP addresses.
- **Protocol Traffic** – Packets from networking protocols (e.g., ARP, ICMP, DHCP).

### Data Sources

Applications interact with various data sources, such as:

- **Databases** (e.g., SQL, NoSQL)
- **Web Services** (RESTful or SOAP)
- **External APIs** (e.g., weather, maps, financial data)

> These often involve **sensitive data** and must be protected using encryption, authentication, and secure transmission protocols.

---

## Data Security – The Three States of Data

Data exists in one of three states. Each requires specific protection strategies:

|**State**|**Description**|**Protection Methods**|
|---|---|---|
|**At Rest**|Stored data (e.g., on disk or backup)|Full-disk encryption (BitLocker, LUKS)|
|**In Transit**|Moving across a network|TLS/SSL, VPNs, HTTPS|
|**In Process**|Actively used in RAM or CPU|Hardware-based protection (e.g., TPM)|

- **TPM (Trusted Platform Module)** – Hardware chip that stores cryptographic keys securely and ensures integrity of boot processes and memory use.

---

## Windows Deployment Services (WDS)

- **WDS** is a Microsoft service for deploying operating systems over a network.
- Used to **remotely install Windows images** onto multiple client machines.
- Reduces setup time and enforces consistency across:
    - Physical desktop        
    - Virtual machines
    - Enterprise labs

Use cases:

- Educational labs
- Enterprise IT onboarding
- Standardized device imaging



## APIs (Application Programming Interfaces)

APIs allow software components to **communicate, share data, and delegate functionality**.

### Common Types of APIs


- **Web APIs** - Use web protocols (HTTP/S) for communication.
- **Library APIs** – Provide a set of callable functions with documentation, can operate in offline environments. 
- **Operating System APIs** – Allow applications to interface with the OS. 
- **Hardware APIs** – Allow apps to interact with physical components (GPU, camera)

### API Analogy – The Restaurant Model

|**Component**|**Analogy**|
|---|---|
|Application|A customer ordering food|
|OS API|The waiter taking the order|
|Driver|The chef who understands the recipe|
|Hardware API|The kitchen tools used to prepare the meal|
|Response/Data|The dish served to the customer|
