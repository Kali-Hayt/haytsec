# Module 2 – TCP/IP Model

## TCP/IP Protocols by Layer (with Ports)

### Application Layer (OSI Layers 5–7)
- **Telnet** – *Telecommunication Network* – Remote text login (**insecure**) – **TCP 23**  
- **FTP** – *File Transfer Protocol* – File transfer – **TCP 20, TCP 21**  
- **TFTP** – *Trivial File Transfer Protocol* – Simple file transfer, no auth – **UDP 69**  
- **SNMP** – *Simple Network Management Protocol* – Monitor/manage devices – **UDP 161, UDP 162**  
- **POP3** – *Post Office Protocol v3* – Retrieve email – **TCP 110**  
- **HTTP** – *HyperText Transfer Protocol* – Web browsing – **TCP 80**  
- **HTTPS** – *HyperText Transfer Protocol Secure* – Encrypted web browsing (SSL/TLS) – **TCP 443**  
- **SMTP** – *Simple Mail Transfer Protocol* – Send email – **TCP 25, TCP 587**  
- **DNS** – *Domain Name System* – Resolve names to IP – **UDP 53, TCP 53**  
- **DHCP** – *Dynamic Host Configuration Protocol* – Assign IPs – **UDP 67, UDP 68**  
- **NTP** – *Network Time Protocol* – Clock sync – **UDP 123**

### Transport Layer (OSI Layer 4)
- **TCP** – *Transmission Control Protocol* – Reliable, connection-oriented  
- **UDP** – *User Datagram Protocol* – Fast, connectionless  

### Internet Layer (OSI Layer 3)
- **ICMP** – *Internet Control Message Protocol* – Diagnostics (e.g., ping)  
- **IGMP** – *Internet Group Management Protocol* – Multicast management  
- **ARP** – *Address Resolution Protocol* – IP-to-MAC mapping  
- **IPv4** – *Internet Protocol version 4* – 32-bit addressing  
- **IPv6** – *Internet Protocol version 6* – 128-bit addressing  

### Network Access Layer (OSI Layers 1–2)
- **Ethernet** – Wired LAN standard  
- **PPP** – *Point-to-Point Protocol* – Direct link  
- **PPPoE** – *Point-to-Point Protocol over Ethernet* – ISP connections  
- **FR** – *Frame Relay* – Older WAN  
- **MPLS** – *Multiprotocol Label Switching* – Label-based routing  
- **Wi-Fi** – Wireless LAN standard

---

## Transport Layer Details – TCP vs UDP

### TCP – Transmission Control Protocol
- **Connection-oriented** – Establishes stable connection before data transfer  
- **Sequence numbers** – Ensures correct order  
- **Acknowledgements (ACK)** – Confirms receipt  
- **Retransmissions** – Resend lost data  
- **Flow control** – Prevents overload  
- **Windowing** – Send multiple segments before requiring ACK  
- Example handshake: **SYN → SYN-ACK → ACK**  
- Reliable but slower

### UDP – User Datagram Protocol
- **Connection-less** – No session setup  
- **No sequence numbers** – Out-of-order possible  
- **No acknowledgements** – No confirmation of delivery  
- **No retransmissions** – Lost = gone  
- **No flow control** – Can overwhelm  
- **No windowing** – One at a time  
- Fast but unreliable

### Quick Analogy
- **TCP** – Certified mail 📦 — tracked, signed, in order  
- **UDP** – Shouting 📢 — fast, but no guarantee it’s heard
---
## TCP Three-Way Handshake

1. **SYN** – Client → Server: "Can we talk? Here’s my starting sequence number."  
2. **SYN-ACK** – Server → Client: "Yes, and here’s mine. I got your request."  
3. **ACK** – Client → Server: "Got it. Let’s start sending data."

✅ Connection established — ready for data transfer.  
🔍 Purpose: Synchronizes sequence numbers on both ends and confirms both sides are ready.

---
## TCP Acknowledgement, Transmission, and Flow Control

- **Acknowledgements (ACKs)** – Receiver confirms it got the data segment.  
- **Sequence Numbers** – Used to reassemble segments in correct order.  
- **Flow Control** – TCP adjusts how much data is sent before needing an ACK (prevents overwhelming the receiver).  
- **Window Size** – Amount of data (in bytes) that can be sent before waiting for an ACK.  
  - If network is busy → window size decreases.  
  - If network is clear → window size increases.  
## TCP Four-Way Handshake (Session Termination)

1. **FIN** – One side says, “I’m done sending data” (initiates close).  
2. **ACK** – Other side acknowledges the FIN.  
3. **FIN** – The other side now says, “I’m done too.”  
4. **ACK** – First side acknowledges.  

✅ Connection is now fully closed.  
🔍 Reason for four steps: Each direction of the TCP session is closed independently, ensuring all remaining data is sent and acknowledged.

---
## TCP vs UDP – When to Use

### TCP (Transmission Control Protocol)
- **Focus:** Reliability over speed  
- Connection-oriented – ensures delivery, order, and integrity.  
- Use when **all content must arrive intact** and timing is less important.  
- Example: **Email** – losing part of a message is unacceptable.

### UDP (User Datagram Protocol)
- **Focus:** Speed over reliability  
- Connection-less – sends without confirming receipt.  
- Use when **low latency is critical** and occasional data loss is acceptable.  
- Example: **VoIP (phone calls)** – a missing packet won’t ruin the conversation, but delays will.
- Common for **streaming media** (video/audio) because speed matters more than perfect accuracy.  
  - **Hybrid case:** Some applications may use TCP briefly (to establish connection, sync, or request missing key data) and then switch to UDP for speed.
---
