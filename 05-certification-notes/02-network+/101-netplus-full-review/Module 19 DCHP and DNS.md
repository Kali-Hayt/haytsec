## Module 19 – DHCP & DNS

### 🧱 DHCP (Dynamic Host Configuration Protocol)
- **Purpose:** Automatically assigns IP configuration to devices.
- Operates at **Application Layer** (Layer 7) but affects Layer 3 addressing.
- Saves time, avoids manual IP assignment errors.

---

### DHCP Process – **DORA**
1. **Discover** – Client broadcasts to find DHCP server.
2. **Offer** – Server sends an IP configuration offer.
3. **Request** – Client requests the offered address.
4. **Acknowledge** – Server confirms lease.

---

#### Key DHCP Terms
- **Lease** – Time an IP is assigned before renewal.
- **Scope** – Range of IPs a DHCP server can assign.
- **Reservation** – Specific IP always given to a specific MAC.
- **Exclusion** – IPs in scope that will never be assigned automatically.

---

#### DHCP Ports
- **UDP 67** – Server
- **UDP 68** – Client

---

#### Exam Tip
- If a client gets an address like `169.254.x.x`, it’s using **APIPA** (Automatic Private IP Addressing) → means DHCP failed.

---

## DNS (Domain Name System)
- **Purpose:** Translates domain names ↔ IP addresses.
- Works like the **phonebook** of the internet.
- Operates at **Application Layer**.

---

### DNS Record Types
- **A** – Hostname → IPv4 address.
- **AAAA** – Hostname → IPv6 address.
- **CNAME** – Alias to another name.
- **MX** – Mail exchange server.
- **PTR** – Reverse lookup (IP → name).
- **NS** – Nameserver for a domain.
- **TXT** – Text information (often for verification).

---

### DNS Process
1. User enters `www.example.com`.
2. Query goes to DNS resolver (often ISP or local cache).
3. Resolver contacts root → TLD → authoritative name server.
4. IP is returned and cached.

---

#### DNS Ports
- **UDP 53** – Standard queries.
- **TCP 53** – Zone transfers (server-to-server).

---

## Exam Pointers
✅ DHCP = DORA (Discover, Offer, Request, Acknowledge).  
✅ DHCP failure → APIPA (169.254.x.x).  
✅ DNS “A” = IPv4, “AAAA” = IPv6.  
✅ DNS & DHCP both at Application Layer, but serve different functions.  
✅ UDP 67/68 (DHCP), UDP/TCP 53 (DNS).  
