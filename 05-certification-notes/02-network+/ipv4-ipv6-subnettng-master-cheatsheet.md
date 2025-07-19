```markdown
# 🧠 IPv4 + IPv6 Subnetting Master Cheatsheet

---

## 📦 1. IPv4 Address Structure
- IPv4 uses **32-bit addresses**, divided into **4 octets** (8 bits each)
- Written in **dotted decimal**: `192.168.1.1`
- Each octet ranges from **0–255**
- Binary example: `192.168.1.1` = `11000000.10101000.00000001.00000001`

---

## 🏛️ 2. IP Address Classes (Classful IPv4)
| Class | Starting Bits | Range              | Default Mask       | CIDR |
|-------|----------------|--------------------|--------------------|------|
| A     | 0xxxxxxx       | 1.0.0.0 – 126.255  | 255.0.0.0          | /8   |
| B     | 10xxxxxx       | 128.0.0.0 – 191.255| 255.255.0.0        | /16  |
| C     | 110xxxxx       | 192.0.0.0 – 223.255| 255.255.255.0      | /24  |

🧱 *Class D (Multicast) = 224–239 | Class E (Experimental) = 240–255*

---

## 📊 3. CIDR to Subnet Mask Table (IPv4)
| CIDR | Subnet Mask        | Block Size | Usable Hosts | Wildcard Mask     |
|------|---------------------|-------------|---------------|-------------------|
| /30  | 255.255.255.252     | 4           | 2             | 0.0.0.3           |
| /29  | 255.255.255.248     | 8           | 6             | 0.0.0.7           |
| /28  | 255.255.255.240     | 16          | 14            | 0.0.0.15          |
| /27  | 255.255.255.224     | 32          | 30            | 0.0.0.31          |
| /26  | 255.255.255.192     | 64          | 62            | 0.0.0.63          |
| /25  | 255.255.255.128     | 128         | 126           | 0.0.0.127         |
| /24  | 255.255.255.0       | 256         | 254           | 0.0.0.255         |

---

## 📐 4. IP Range Examples (for /27 to /30)
### Subnetting `192.168.1.0/27`
- **Subnet 1:**
  - Network: `192.168.1.0`
  - First Host: `192.168.1.1`
  - Last Host: `192.168.1.30`
  - Broadcast: `192.168.1.31`
- **Subnet 2:**
  - Network: `192.168.1.32`
  - Hosts: `.33 – .62`
  - Broadcast: `.63`

### Subnetting `192.168.1.64/28`
- Block size: 16
- Hosts: 14
- Range: `.65 – .78`, Broadcast = `.79`

---

## 🧮 5. Subnet Math (IPv4)
- **# Hosts = 2^(32 - CIDR) - 2** (subtract 2 for network + broadcast)
- **# Subnets = 2^borrowed bits**
- **Block Size = 256 - 4th Octet in Mask**
  - e.g. `255.255.255.224` → `256 - 224 = 32`

---

## 💡 6. Binary Quick Reference (IPv4)
- /24 = `11111111.11111111.11111111.00000000`
- /27 = `11111111.11111111.11111111.11100000`
- /30 = `11111111.11111111.11111111.11111100`

---

## 🔥 7. Cheat Code for Exam (IPv4)
- **/30 = point-to-point links (2 hosts)**
- **/28 = 14 hosts → small LANs**
- **/27 = 30 hosts → common subnet**
- **If unsure, guess /24 (default class C)**

---

## 📚 8. VLSM Tips
- Start with largest network first
- Break remaining space into smaller subnets
- Keep track of used blocks to avoid overlaps

---

## ✅ 9. What You NEED to Memorize (IPv4)
- /24 → 254 hosts
- /27 → 30 hosts
- /28 → 14 hosts
- /29 → 6 hosts
- /30 → 2 hosts

Use these CIDRs to size networks fast without math.

---

## 🌍 10. IPv6 Basics
- **IPv6 = 128 bits**, written in hexadecimal
- Format: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
- Can omit leading zeros & compress zero blocks
  - `2001:db8:85a3::8a2e:370:7334`

### Key Terms
- **Global Unicast:** Routable addresses (like public IPv4)
- **Link-Local:** `fe80::/10` for local communication
- **Multicast:** `ff00::/8`
- **Loopback:** `::1`

### Common Prefix Lengths
| Prefix | Usage                   | Addresses        |
|--------|--------------------------|------------------|
| /64    | Standard host subnet     | 2^64 addresses   |
| /48    | Site allocation          | 2^80 addresses   |
| /128   | Single host              | 1 address        |

### No Broadcast in IPv6
- Uses **multicast** instead
- Every interface **must** have a **link-local** address

---

*Stay subnet smart. Glance at this sheet often until your brain does it automatically.*
```