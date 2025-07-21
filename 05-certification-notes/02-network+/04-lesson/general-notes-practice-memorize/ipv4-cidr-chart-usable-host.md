#tags: #networking #subnetting #ipv4 #cidr #cheatsheet #certs #networkplus

## 🧮 IPv4 CIDR Chart + Usable Hosts

| CIDR | Subnet Mask         | Usable Hosts | Total IPs | Notes                            |
|------|----------------------|---------------|-----------|----------------------------------|
| /8   | 255.0.0.0            | 16,777,214    | 16,777,216 | Class A range                    |
| /16  | 255.255.0.0          | 65,534        | 65,536     | Class B range                    |
| /24  | 255.255.255.0        | 254           | 256        | Class C range, common in LANs   |
| /25  | 255.255.255.128      | 126           | 128        | Half of a /24                   |
| /26  | 255.255.255.192      | 62            | 64         | Quarter of a /24                |
| /27  | 255.255.255.224      | 30            | 32         | Used for small subnets          |
| /28  | 255.255.255.240      | 14            | 16         | Common in lab/testing nets      |
| /29  | 255.255.255.248      | 6             | 8          | Point-to-point WAN links        |
| /30  | 255.255.255.252      | 2             | 4          | Router-to-router links          |
| /32  | 255.255.255.255      | 0             | 1          | Host route (single device)      |

### 🧠 Formula Reminder:
Usable Hosts = 2^(32 - CIDR) - 2  
(*Subtract 2 for Network and Broadcast addresses*)

---

## ✅ Example Breakdown: 192.168.10.0/26

- **Subnet Mask**: 255.255.255.192  
- **Total IPs**: 64  
- **Usable Hosts**: 62  
- **Network Address**: 192.168.10.0  
- **First Usable IP**: 192.168.10.1  
- **Last Usable IP**: 192.168.10.62  
- **Broadcast Address**: 192.168.10.63

---

## 🔁 Use Cases
- **/24** — Most common subnet for local networks (254 hosts)
- **/30** — WAN links, only 2 usable IPs (router to router)
- **/32** — Used in routing tables, ACLs (represents one host)
---

# 🧠 Subnetting Made Simple (IPv4 + CIDR)

---

## 🔢 IPv4 = 32 Bits

- An IP address like `192.168.1.1` = 4 numbers (called octets)
- Each octet = 8 bits → total = 32 bits
- Example in binary:  
  `11000000.10101000.00000001.00000001` = 192.168.1.1

---

## 🎯 What is CIDR?

**CIDR** = "Classless Inter-Domain Routing"

- It's written like: `/24`, `/25`, `/26`, etc.
- It means: "How many bits are for the **network**"

Example:  
- `/24` = first 24 bits are network  
- The rest (32 - 24 = 8 bits) are for **host IPs**

---

## 🧱 Binary Bit Weights (per octet)

Helps turn bits into numbers:

128 64 32 16 8 4 2 1

So:

- `11111111` = 255  
- `11000000` = 128 + 64 = 192  
- `11111100` = 252  

---

## 🧠 CIDR to Subnet Mask / Hosts / Block Size

| CIDR | Subnet Mask         | Hosts Usable | Block Size |
|------|----------------------|---------------|-------------|
| /8   | 255.0.0.0            | ~16 million   | Very large  |
| /16  | 255.255.0.0          | 65,534        | 65,536      |
| /24  | 255.255.255.0        | 254           | 256         |
| /25  | 255.255.255.128      | 126           | 128         |
| /26  | 255.255.255.192      | 62            | 64          |
| /27  | 255.255.255.224      | 30            | 32          |
| /28  | 255.255.255.240      | 14            | 16          |
| /29  | 255.255.255.248      | 6             | 8           |
| /30  | 255.255.255.252      | 2             | 4           |

✏️ **Formula:**  
Block Size = `256 - last octet in subnet mask`

---

## 📦 Subnet Ranges and Network Boundaries

Example: **/26** (Block size = 64)

- 0–63
- 64–127
- 128–191
- 192–255

> ✅ If two IPs fall in **different blocks**, they’re in **different subnets**.

Even if devices are in the same building, if they're in different subnet blocks, they **can’t talk without a router**.

---

## 🔍 Example: /26

Given IP: `10.15.20.200/26`

- Subnet Mask: `255.255.255.192`
- Block Size: `64`
- IP falls in: `192 – 255` block
- Network Address: `10.15.20.192`
- Broadcast Address: `10.15.20.255`
- Usable Range: `10.15.20.193 – 10.15.20.254`
- Usable Hosts: `62`

---

## 🔓 CIDR → Binary Mask Breakdown

Each IP = 32 bits.  
CIDR = how many `1`s from the left.  
The rest are `0`s.

### Examples:

- **/24** = 255.255.255.0  
  `11111111.11111111.11111111.00000000`

- **/26** = 255.255.255.192  
  `11111111.11111111.11111111.11000000`

- **/30** = 255.255.255.252  
  `11111111.11111111.11111111.11111100`

---

## 🧠 Rules to Remember

- Same subnet mask + same block = ✅ same network
- Different blocks (even on same floor) = ❌ different network
- Need a router to talk between subnets

---

## 🧪 Practice Tips

✍️ Write this until it's burned in:

128 64 32 16 8 4 2 1

Then try converting:

- `11111111.11111111.11111111.11000000` → What is CIDR?
- `/27` → What is subnet mask? Block size? Hosts?
- Given `192.168.10.122/26` → What’s the network? Usable range?

---

#️⃣ Tags  
#networking #subnetting #ipv4 #CIDR #binary #networkplus #haytsec #certs #labs

