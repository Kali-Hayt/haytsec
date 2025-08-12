**Application Layer (Layer 7)** – Not the physical apps you click on (like Outlook or Gmail). It’s the protocol layer where software services talk to the network.

**Email Protocols**  
- **SMTP** – Send email between servers (TCP 25) or from client securely (TCP 587)  
- **POP3** – Retrieve email (TCP 110)  (Postal Office Protocol Version 3)
- **IMAP** – Retrieve/manage email (TCP 143)  (Internet Message AccessProtocol)

**Network Management**  
- **SNMP** – Monitor/manage devices (UDP 161 for queries/commands, UDP 162 for traps)  

**Web Services**  
- **HTTP** – Web content (TCP 80)  
- **HTTPS** – Secure web content using SSL/TLS (TCP 443)  
  - **SSL (Secure Sockets Layer)** – Older encryption protocol, now replaced by TLS but still referenced by name.  
  - **TLS (Transport Layer Security)** – Modern encryption protocol that provides confidentiality, authentication, and integrity.


**File Transfer**  
- **FTP** – Transfer files (TCP 20, 21)  
- Variants: **SFTP**, **FTPS**, **FTPES**, **TFTP**  

**Remote Access**  
- **SSH** – Secure remote login (TCP 22)  (Secured Shell)
- **Telnet** – Insecure remote login (TCP 23)  

**Name Resolution**  
- **DNS** – Resolve domain ↔ IP (UDP 53 for queries, TCP 53 for zone transfers)  

**Time Sync**  
- **NTP** – Synchronize clocks (UDP 123) (Network Time Protocol)

---

**Presentation Layer (Layer 6)** – Formats data so both sender and receiver can process and display it as intended. Handles encryption, such as **TLS**.  
Example: A Windows server sends data to a Linux server in a format both can read, including fonts and data.

---

**Session Layer (Layer 5)** – Sets up, manages, and tears down sessions between systems. Keeps multiple simultaneous sessions isolated so they don’t interfere with each other.  

Types of communication:  
- **Client ↔ Client** – e.g., two users in a video call  
- **Client ↔ Server** – e.g., user browsing a website  
- **Server ↔ Server** – e.g., database server syncing with a backup server  

Example: Running two videos in separate browser tabs without them slowing each other down.  
Note: A little of the Presentation Layer’s encryption work can sometimes be handled here.

---

**Transport Layer (Layer 4)** – Prepares data for transmission over the network. Breaks large data into smaller segments (**segmentation**) and labels them with **sequence numbers** so the receiving endpoint can reassemble them in the correct order. Handles **error checking** to ensure data arrives intact.  

Example: Like eating a large meal in smaller bites instead of all at once, so it can be managed, checked, and reassembled properly.

---

**Network Layer (Layer 3)** – Handles logical addressing and determines if routing is needed. Selects the best path to the destination, which might be the fastest route (lower latency) or the shortest path (fewer hops).  

Example: Like traveling to a destination — you can choose the faster highway to arrive sooner or the shortest backroads to save distance. The Network Layer identifies the appropriate route to use.

Key protocols:  
- **IPv4 / IPv6** – Logical addressing systems.  
- **ICMP** – Internet Control Message Protocol, used for diagnostics (e.g., ping).

---

**Data Link Layer (Layer 2)** – Handles **physical addressing** (**MAC addresses**) to deliver data to the next directly connected device. Formats data into **frames**, which include the payload, source and destination MAC addresses, and error-checking information (CRC). Frames follow the standards of the network media (Ethernet, Wi-Fi, etc.).  

Addressing at this layer is **device-related**, meaning it identifies the exact hardware interface (NIC) on the local network segment.

Two sublayers:  
- **LLC (Logical Link Control)** – Manages communication between the network layer and the data link layer.  
- **MAC (Media Access Control)** – Uses MAC addresses to control how devices access the network media.

---

**Physical Layer (Layer 1)** – Converts between the binary bit stream and signals. The signals can be electrical, light, or radio waves (e.g., Bluetooth, satellite). This layer includes standards to ensure correct signal processing on both ends.  

The Data Link Layer receives the binary data from the Physical Layer to create frames with MAC addresses.

---
**Encapsulation** – The process of preparing data for delivery from point A to point B. Each OSI layer adds its own information (headers and sometimes trailers) to help it reach the destination.  

**Encapsulation – For Transmission**

When sending data, each OSI layer takes the information from the layer above (called **upper layer data**) and adds its own header. This process continues until the Physical Layer sends the bits/signals across the medium.

Step-by-step:  
- **Layer 7 – Application** → Data  
- **Layer 6 – Presentation** → Data (formatted)  
- **Layer 5 – Session** → Adds **session header** (who’s talking, where to send it within the session)  
- **Layer 4 – Transport** → Adds **transport header** (ports, sequencing, error checking) to **upper layer data**  
- **Layer 3 – Network** → Adds **network header** (source & destination IP addresses)  
- **Layer 2 – Data Link** → Adds **data link header & trailer** (source & destination MAC addresses, error check CRC)  
- **Layer 1 – Physical** → Converts frames to bits/signals for transmission

Key point: Each layer’s “finished package” becomes the **payload** for the next lower layer.
