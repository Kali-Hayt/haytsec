## Module 9 – NAT (Network Address Translation)

## 🧱 Purpose of NAT
- Translates **private IPs** (inside your network) ↔ **public IPs** (used on the internet).
- Solves **IPv4 exhaustion** by allowing many internal devices to share one public address.
- Adds a layer of **privacy** — outside hosts only see the public IP, not internal private IPs.
- Separates **internal** addressing from **external** addressing for both **security** and **conservation**.
- Works at the **Network Layer** (Layer 3).

---

## Types of NAT

### 1. Static NAT
- **One-to-one** mapping between a private and public IP.
- Mapping does not change.
- **Use case:** Hosting a server that must always be reachable at the same public IP.

### 2. Dynamic NAT
- Uses a **pool** of public IPs.
- A private IP is temporarily mapped to an available public IP from the pool.
- Mapping changes over time.
- **Use case:** Organizations with multiple public IPs and many users.

### 3. PAT (Port Address Translation) – NAT Overload
- **Many-to-one** mapping using **unique source ports** to distinguish sessions.
- Most common in **home routers**.
- **Use case:** Multiple devices share one public IP by tagging each connection with a port number.
- **How it works:**
  - Router rewrites **source port numbers** for each outgoing request.
  - Maintains a **NAT table** mapping (Public IP + Port) → (Private IP + Port).
  - When a reply comes back, the router checks this table and sends the response to the correct internal host.
- **Analogy:** Public IP = street address; Port number = apartment number. Same building, different apartments.

---

## NAT Key Terms
- **Inside Local** – Private IP address assigned to a device inside the network.
- **Inside Global** – Public IP address that represents an internal device to the outside world.
- **Outside Local** – IP address of an external host as seen from inside the network (may differ if that host is behind its own NAT).
- **Outside Global** – Actual, routable IP address of the external host on the internet.

---

## Exam Pointers
- NAT breaks **end-to-end connectivity** — can cause issues for VoIP, gaming, and IPsec unless **NAT traversal** is configured.
- **PAT** is used by almost all home networks.
- **IPv6** removes the need for NAT because of its massive address space.

---

## NAT in Action – Public IP from ISP

- **Your private IP** (e.g., `192.168.0.100`) is **not routable** on the internet.
- Your ISP assigns your router a **public IP** (e.g., `155.93.89.163`).
- NAT rewrites your **source IP** in outgoing requests from private → public.
- When the web server replies, NAT translates the **destination IP** from public → private and forwards it back to the correct internal device.

### Example (Dynamic NAT or Static NAT)
- **You → www.comptia.org** (`104.18.35.29`)
  - Outgoing HTTP request:  
    - D.IP: `104.18.35.29`  
    - S.IP: `155.93.89.163` (public, from your ISP)  
- **DBT → www.thisiswhyimbroke.com** (`104.26.6.171`)
  - Outgoing HTTP request:  
    - D.IP: `104.26.6.171`  
    - S.IP: `212.77.4.170` (public, from their ISP)  

### Example (PAT)
- **Computer A (192.168.0.100)** → www.comptia.org (`104.18.35.29`)  
  - D.Port: 443 (HTTPS)  
  - S.Port: 555 (unique per session)  
- **Computer B (192.168.0.101)** → www.notflix.com (`199.60.103.31`)  
  - D.Port: 443 (HTTPS)  
  - S.Port: 556 (unique per session)  
- Both go out as Public IP `155.93.89.163`, but ports **555** and **556** keep sessions separate.

---


### Key Points
- **Public IP** = assigned by ISP; visible on the internet.
- **Private IP** = used internally; NAT handles the translation.
- NAT keeps track of each session so replies go to the correct internal host.
---

