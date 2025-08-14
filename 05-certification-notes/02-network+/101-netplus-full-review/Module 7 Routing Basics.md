## Module 7 – Routing Basics & Static Routing

### Inter-subnet Communications
- Routers facilitate traffic forwarding to the destination subnet.
- Route selection is based on:
  - Network address of the destination IP address.
  - Network address being present in the router’s routing table.

---

### Routing Table Information
- Different network vendor’s routing tables may vary in format and details.
- **3 Key things a router needs to know to select a route:**
  1. **Destination Network Address + Subnet Mask** – Defines where the packet should go.
  2. **Outbound Interface** – Which port/interface on the current router will send the packet.
  3. **Next Hop Address** – IP address of the next router in the path.
- Additional information in the table can explain *why* the router chose that route.

---

### Populating Routing Table Entries
1. **Directly Connected**
   - Router has an interface within that IP subnet.
   - Automatically added to the routing table.

2. **Static Routes**
   - Manually configured by an administrator.
   - Cost is not calculated (manual control).

3. **Dynamic Routes**
   - Learned via a dynamic routing protocol.
   - Costs are factored in.
   - **Cost** = a metric used to decide the best path.
     - **RIP (Routing Information Protocol):** Cost = hop count (fewer hops is better).
     - **OSPF (Open Shortest Path First):** Cost = based on link bandwidth (higher bandwidth = lower cost).
     - **EIGRP (Enhanced Interior Gateway Routing Protocol):** Cost = composite metric (bandwidth, delay, reliability, load).
   - **Rule:** Lower cost wins. If costs are equal, router may load balance between paths.
---
## System Administrative Distance (AD)

- **Definition**: AD is the value a router uses to decide which route source to trust when multiple routes lead to the same destination.
- **Purpose**: Helps the router choose the most reliable route.
- **Decision Point**:
  - **Configured manually** → Static routes (admin decides the path).
  - **Learned automatically** → Dynamic routes (routing protocol decides the path).
- **Rule**: Lower AD = more preferred.
- **Exam Tip**: Focus on the concept — AD compares route *sources*, not route *metrics*.

---
## How to Read Any Routing Table 🧱

Routers use routing tables to decide **where to send packets**.  
Different vendors display it differently, but the logic is the same.

---

### 1. Identify the Destination Network
- **Column names:** `Destination`, `Network`, `Prefix`, `Subnet`, or `Destination/Mask`
- Example:
  - `192.168.1.0/24` → All addresses from `.1` to `.254`
  - `/32` → A single host
- 🧠 *Rule:* Router picks the **longest prefix match** (most specific network) first.

---

### 2. Find the Prefix Length or Mask
- `/24` = 255.255.255.0 (smaller network, more specific)
- `/16` = 255.255.0.0 (larger network, less specific)
- Why important? **Longest prefix wins.**

---

### 3. Check the Protocol (How Route Was Learned)
- Common codes:
  - `C` = Connected (directly plugged into router)
  - `S` = Static (manually set)
  - `O` = OSPF (Open Shortest Path First)
  - `R` = RIP (Routing Information Protocol)
  - `D` = EIGRP (Enhanced Interior Gateway Routing Protocol)
  - `B` = BGP (Border Gateway Protocol)
- Vendor note: Juniper shows full names, Cisco uses short letters.

---

### 4. Look at Administrative Distance (AD) or Preference
- **AD = Trust Level** (lower is better)
- Typical Cisco defaults:
  - Connected = 0  
  - Static = 1  
  - EIGRP (internal) = 90  
  - OSPF = 110  
  - RIP = 120
- Juniper calls it **Preference**, Huawei calls it **Pre**.

---

### 5. Check the Metric or Cost
- Metric = How “expensive” the route is inside its protocol.
- Lower = better.
- Each protocol calculates cost differently:
  - OSPF → Link bandwidth
  - RIP → Hop count
  - EIGRP → Bandwidth + delay

---

### 6. Find the Next Hop
- The **IP address of the next router** in the path.
- Example: `via 192.168.3.2`
- If **Connected**, there’s no “via” — it’s already directly reachable.

---

### 7. Identify the Outbound Interface
- The router port that sends packets toward the next hop.
- Examples:
  - Cisco: `GigabitEthernet0/1`
  - Juniper: `ge-0/0/0`
  - Huawei: `Vlanif100`

---

## Reading Order in Real Life
When a packet arrives:
1. Match the **most specific network** in the table (longest prefix).
2. If tied, pick the **lowest AD/Preference**.
3. If still tied, pick the **lowest metric**.
4. Send packet **out the listed interface** toward the **next hop**.

---

## Example Mental Walkthrough

Packet to `172.16.2.1`:
1. Table has `/24`, `/16`, and `/8` matches → `/24` wins (most specific).
2. Check AD if multiple `/24` exist.
3. If AD ties, lowest metric wins.
4. Forward out `GigabitEthernet1/2` to `172.16.2.254`.
---
## Default Route

- Used **only** when packets to be forwarded do **not** match any specific entry in the IP routing table.
- In an IP routing table, the default route is `0.0.0.0/0` (IPv4) — meaning it matches all possible addresses.
- Acts as a **catch-all** route to forward packets when no better match exists.
- Can be set:
  - **Statically**: manually configured by the administrator.
  - **Dynamically**: learned through routing protocols (e.g., OSPF, BGP).
- Often points to an upstream router or ISP as the **gateway of last resort**.

📝 **Analogy**: Like a "miscellaneous" bin in a mailroom — if no address matches a known box, it goes here for forwarding.
