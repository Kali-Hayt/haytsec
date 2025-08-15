## Module 21 – IPv6

### 🧱 Why IPv6?
- IPv4 (32-bit) = ~4.3 billion addresses → exhausted.
- IPv6 (128-bit) = 340 undecillion addresses.
- Built for **end-to-end connectivity** without NAT.
- Integrated **security** with IPsec support.

---

## IPv6 Address Format
- **128 bits** written as **8 groups** of 4 hex digits.
- Example: `2001:0db8:0000:0000:0000:ff00:0042:8329`.

### Compression Rules
1. Remove leading zeros in each block:  
   `2001:db8:0:0:0:ff00:42:8329`
2. Replace **one** sequence of consecutive `:0:` blocks with `::`  
   `2001:db8::ff00:42:8329`

---

## IPv6 Address Types
- **Unicast** – One-to-one.
  - **Global Unicast**: Public, routable (`2000::/3`).
  - **Link-Local**: Auto-assigned for local link (`fe80::/10`), always present.
  - **Unique Local**: Private network space (`fc00::/7`).
- **Multicast** – One-to-many (`ff00::/8`).
- **Anycast** – Same address on multiple devices; routes to nearest.

---

## No Broadcast in IPv6
- Replaced with **multicast** and **anycast**.
- Reduces unnecessary traffic.

---

## IPv6 Key Protocols
- **NDP (Neighbor Discovery Protocol)**:  
  - Finds other nodes, learns addresses, and maintains reachability.
  - Uses ICMPv6 messages like *Neighbor Solicitation* and *Neighbor Advertisement*.
- **SLAAC (Stateless Address Autoconfiguration)**:  
  - Devices self-configure IPv6 addresses from router advertisements (no DHCPv6 needed).
- **DHCPv6**: Optional for managed IPv6 address assignment.

---

## IPv6 vs IPv4 – Exam Pointers
- No NAT in IPv6 — every device can have a unique global IP.
- IPv6 headers are simpler (fixed length).
- Link-Local addresses are **mandatory** and start with `fe80::/10`.
- IPv6 uses **ICMPv6** for neighbor discovery and error messages.
- **Dual Stack** = Running IPv4 & IPv6 simultaneously.
- **Tunneling** = Encapsulating IPv6 in IPv4 for compatibility.

---

## Common Exam Traps
✅ `::1` = Loopback (IPv6 version of 127.0.0.1).  
✅ `::` = Unspecified address (like 0.0.0.0).  
✅ One `::` allowed in compression — can’t use twice.  
✅ Link-Local only works in local segment — needs interface ID (`%eth0`).  
