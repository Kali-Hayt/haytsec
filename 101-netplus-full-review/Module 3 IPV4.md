# IPv4 Master Note

## 🧱 IPv4 Overview
- IPv4 = Internet Protocol version 4
- Logical addressing for devices on a network
- Address size: **32 bits** (4 octets)
- Written as **dotted decimal notation** (e.g., 192.168.1.1)
- **Range per octet**: 0–255
- **Total possible IPv4 addresses**: 4,294,967,296
- Two parts:
  - **Network ID** – identifies the network
  - **Host ID** – identifies the device on that network
- Determined by **subnet mask** (e.g., 255.255.255.0)

---

## 📜 IPv4 Header Layout (with field meanings)

| Field          | Meaning |
|----------------|---------|
| **Version**    | IP version used (IPv4 = value 4) |
| **IHL** – Internet Header Length | Size of the IPv4 header in 32-bit words (tells where data starts) |
| **TOS** – Type of Service | Specifies packet priority & quality of service |
| **Total Length** | Entire packet size (header + data) in bytes |
| **Identification** | Unique ID to help reassemble fragmented packets |
| **Flags** | 3-bit field controlling fragmentation: Don't Fragment (DF), More Fragments (MF), or last fragment |
| **Fragment Offset** | Position of this fragment relative to the start of the original packet |
| **TTL** – Time To Live | Max number of hops before packet is discarded (prevents infinite loops) |
| **Protocol** | Identifies the next layer protocol (e.g., TCP=6, UDP=17, ICMP=1) |
| **Header Checksum** | Error-checking value for the header |
| **Source Address** | Sender’s IPv4 address |
| **Destination Address** | Receiver’s IPv4 address |
| **Options** | Additional header options (rarely used) |
| **Data** | Actual payload being delivered |

🧠 **Order to Remember**:
Version → IHL → TOS → Length → Identification → Flags → Offset → TTL → Protocol → Checksum → Source IP → Destination IP → Options → Data

---

## 🎯 IP Classes & Default Masks

| Class | First Octet Range | Default Subnet Mask | CIDR | Usage |
|-------|------------------|---------------------|------|-------|
| **A** | 1–126             | 255.0.0.0           | /8   | Large networks |
| **B** | 128–191           | 255.255.0.0         | /16  | Medium networks |
| **C** | 192–223           | 255.255.255.0       | /24  | Small networks |
| **D** | 224–239           | N/A (Multicast)     | N/A  | Multicast groups |
| **E** | 240–255           | Reserved            | N/A  | Experimental |

---

## 🏠 Private IPv4 Ranges

| Class | Private Range              | CIDR      | # of Addresses |
|-------|----------------------------|-----------|----------------|
| A     | 10.0.0.0 – 10.255.255.255   | 10.0.0.0/8| ~16.7 million  |
| B     | 172.16.0.0 – 172.31.255.255 | 172.16.0.0/12| ~1 million |
| C     | 192.168.0.0 – 192.168.255.255| 192.168.0.0/16| ~65k     |

---

## 📏 CIDR Cheat Sheet

| CIDR | Subnet Mask        | # of Hosts Usable |
|------|--------------------|-------------------|
| /8   | 255.0.0.0          | 16,777,214        |
| /16  | 255.255.0.0        | 65,534            |
| /24  | 255.255.255.0      | 254               |
| /25  | 255.255.255.128    | 126               |
| /26  | 255.255.255.192    | 62                |
| /27  | 255.255.255.224    | 30                |
| /28  | 255.255.255.240    | 14                |
| /29  | 255.255.255.248    | 6                 |
| /30  | 255.255.255.252    | 2                 |

---
## 🌐 Network vs Host Addresses

Each IPv4 subnet has **three key parts**:

- **Network Address**  
  - First IP in the subnet (all host bits = 0).  
  - Identifies the subnet itself.  
  - Not assigned to devices.

- **Host Addresses**  
  - Usable IPs for devices within the subnet.  
  - Range is **between** the network and broadcast addresses.

- **Broadcast Address**  
  - Last IP in the subnet (all host bits = 1).  
  - Sends data to **all hosts** in that network.

### Example: `192.168.1.0/24`
- **Network Address**: 192.168.1.0  
- **Usable Host Range**: 192.168.1.1 → 192.168.1.254  
- **Broadcast Address**: 192.168.1.255

💡 **Remember**: First address = network, last address = broadcast, everything in between = usable hosts.

---
## 🧠 Quick Reminders
- **First address** in a network = **Network ID**
- **Last address** in a network = **Broadcast**
- CIDR = Classless Inter-Domain Routing → lets you use custom subnet masks
- MAC address is different: hardware address at Data Link layer, 48 bits (hex)
- **Flags** = fragmentation control bits — decide whether a packet can be split and if more fragments follow.

---

## 🔍 Common Exam Tips
- 127.x.x.x = Loopback (localhost)
- 169.254.x.x = APIPA (Automatic Private IP Addressing – when DHCP fails)
- Public IP = routable on internet; Private IP = not routable without NAT
---
## 🌐 Private vs Public IP Addresses

### Private IP
- **Scope:** Internal networks only (LAN/WLAN).
- **Uniqueness:** Not unique globally; same ranges reused in many networks.
- **Internet Access:** Requires NAT to map private → public IP.
- **Examples:**  
  - `192.168.x.x` in home networks  
  - `10.x.x.x` or `172.16.x.x – 172.31.x.x` in corporate networks

### Public IP
- **Scope:** Globally unique, routable on the internet.
- **Assigned By:** ISPs, managed by IANA/RIRs.
- **Example:** Address websites see when you visit them.

💡 **Analogy:**  
Private IP = your apartment number.  
Public IP = the building’s street address.  
NAT = the receptionist who forwards mail.

---

## 🔄 How Private IP → Public Internet Works

1. **Device Gets Private IP**
   - Computer requests an IP via DHCP.
   - Router assigns a private address (e.g., 192.168.1.50).

2. **Router Has Public IP**
   - ISP assigns router a globally unique public IP (e.g., 73.44.55.102).

3. **NAT Translation**
   - Router rewrites outgoing packets’ source IP from private → public.
   - Tracks connections using ports in a NAT table.

4. **Internet Communication**
   - External servers see only the router’s public IP.
   - Replies return to router, which maps them back to the correct private IP.

---

## 🛠 Router's Key Jobs (IPv4 Context)

- **Routing:** Moves packets between networks (LAN ↔ Internet).
- **NAT:** Translates private IPs to public IP and vice versa.
- **DHCP Server:** Assigns private IPs inside LAN/WLAN.
- **Firewall:** Filters traffic based on rules.
---
