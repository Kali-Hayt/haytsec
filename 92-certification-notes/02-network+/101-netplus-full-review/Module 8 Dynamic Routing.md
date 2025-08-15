## Module 8 – Dynamic Routing

### 🧱 Routing Types
- **Static Routing** – Manually configured paths.
- **Dynamic Routing** – Routers share routes automatically using protocols.

---

## Autonomous System (AS)
- **Definition:** A routed network under the control of a single organization.
- **Example:** An ISP’s network, a large company’s internal network.
- **Numbering:** Each AS has a unique **ASN** (Autonomous System Number).

---

## Dynamic Routing Protocol Categories

### 1. **Interior Gateway Protocols (IGPs)**
- **Use:** Inside an AS.
- **Types:**
  - **Distance Vector** – Chooses routes based on hop count (shortest path by number of routers).
    - Example: **RIP** (max 15 hops).
    - “Tell your neighbor what you know.”
  - **Link State** – Chooses best route based on cost (often bandwidth).
    - Example: **OSPF**.
    - “Tell everyone about your direct connections.”

---

### 2. **Exterior Gateway Protocols (EGPs)**
- **Use:** Between different ASes.
- **Example:** **BGP** (Border Gateway Protocol).
  - Not heavily tested on Network+.
  - Think of it as the “global postal system”:
    - Europe → USA = figure out **which ISP** to send to.
    - Inside USA = that ISP figures out which **state** and **city** to deliver to.
  - Decides best path across the internet backbone.

---

## Quick Comparisons

| Type           | Scope         | Metric      | Example | Notes |
|----------------|--------------|-------------|---------|-------|
| Distance Vector| Inside AS     | Hop count   | RIP     | Simple, less efficient |
| Link State     | Inside AS     | Cost/bandwidth | OSPF | Scales well, faster convergence |
| Exterior (BGP) | Between ASes  | Path attributes | BGP  | Internet routing, ISPs |

---

## Administrative Distance (AD) Defaults
- **Connected** – AD **0** (always preferred)
- **Static** – AD **1**
- **EIGRP (internal)** – AD **90**
- **OSPF** – AD **110**
- **RIP** – AD **120**
- **BGP (external)** – AD **20**
- **BGP (internal)** – AD **200**

**Rule:** Lower AD wins if two routes to the same destination exist, regardless of metric.

---

💡 **Memory Hook:**  
- *Interior = In-house* (RIP, OSPF).  
- *Exterior = Between houses* (BGP).  
- **Distance Vector:** Count stops (hops).  
- **Link State:** Judge road quality (bandwidth).  
- **AD:** “Zero is king, one is next — higher is less trusted.”
---
## Interior Routing Protocols – Quick Map

### 1. Distance Vector
- **Measures:** Distance in **hops** (number of routers to destination).
- **Examples:**  
  - **RIP** – Routing Information Protocol (max 15 hops).  
  - **IGRP** – Interior Gateway Routing Protocol (Cisco proprietary, obsolete).
- **Pros:** Simple, low CPU.  
- **Cons:** Slow convergence, loop risk.

---

### 2. Link State
- **Measures:** **Cost** (usually based on bandwidth/speed).  
- **Examples:**  
  - **OSPF** – Open Shortest Path First (industry standard).  
  - **IS-IS** – Intermediate System to Intermediate System (mostly used by ISPs).
- **Pros:** Fast convergence, scales well.  
- **Cons:** More CPU/memory use.

---

### 3. Hybrid
- **Mix** of Distance Vector & Link State features.  
- **Example:** **EIGRP** – Enhanced Interior Gateway Routing Protocol.
  - Uses composite metric (bandwidth, delay, reliability, load).
  - Cisco proprietary (now partially open).

---

💡 **Memory Hook:**  
- **Hops = DV** (RIP, IGRP)  
- **Speed/Cost = LS** (OSPF, IS-IS)  
- **Both = Hybrid** (EIGRP)
---
## RIP – Routing Information Protocol (Distance Vector)

### Algorithm
- **Based on:** Bellman–Ford Algorithm
- **Purpose:** Find the shortest path to each network by counting **hops**.
- **Hop Limit:** Max 15 hops (16 = unreachable).
- Distance Vector Based

---

### Versions

#### **RIP v1**
- **Classful** – Does **not** send subnet mask info in updates.
  - Means it **cannot** support VLSM (Variable Length Subnet Masking) or CIDR.
  - Assumes default masks based on class (A, B, C).
- **Updates:** Sent via **broadcast** (255.255.255.255) every 30 seconds.
- **Downside:** Wastes bandwidth (all devices see it, even if not needed).

---

#### **RIP v2**
- **Classless** – Includes subnet mask info.
  - Supports VLSM and CIDR.
  - Works with more complex, modern networks.
- **Updates:** Sent via **multicast** to **224.0.0.9** (only RIP routers listen).
- **Still** a Distance Vector protocol (hop count metric).

---

#### **RIPng** (Next Generation)
- **Purpose:** RIP for **IPv6**.
- Uses multicast **FF02::9** for updates.
- Still limited to 15 hops.
- Supports IPv6’s addressing and features.

---

💡 **Memory Hooks**
- **RIP = "Rest In Peace"** → old, slow, and dying out.
- **V1 = Very old, Classful, Broadcast.**
- **V2 = Very improved, Classless, Multicast.**
- **ng = Next Generation, IPv6.**
---
## OSPF – Open Shortest Path First (Link State)

### Algorithm
- **Based on:** Edsger Dijkstra’s **Shortest Path First** algorithm.
- **Goal:** Find the *fastest* route, not just the fewest hops.
- **Metric:** **Cost** (based on bandwidth — faster links = lower cost).

---

### Update Method
- **Uses multicast** (not broadcast) to reduce unnecessary traffic.
- **Addresses:**
  - `224.0.0.5` – All OSPF routers
  - `224.0.0.6` – All OSPF *designated routers* (DR) and backup DRs
- **Update behavior:** Sends **link-state advertisements (LSAs)** when network changes, not constant full table dumps.

---

### Versions
- **V1** – Deprecated, not supported.
- **V2** – For IPv4 networks.
- **V3** – For IPv6 networks.
  - Still uses the same SPF algorithm.
  - Runs separately for IPv6 addressing.

---

💡 **Memory Hooks**
- **“O” in OSPF = Open standard** → works across vendors (not proprietary).
- **Multicast instead of broadcast** = less noisy than RIP v1.
- **Shortest Path First** = quality of road (bandwidth), not just number of stops.
---
## OSPF – Cost & Communication

### Cost Calculation
- **Formula:**  
  `Link Cost = Reference Bandwidth ÷ Interface Bandwidth`
- **Reference Bandwidth**: Default is often 100 Mbps (can be changed by admin).
- **Interface Bandwidth**: Speed of the specific link (10 Mbps, 1 Gbps, etc.).
- **Rule:** Higher speed → lower cost.
- **Cumulative:** If a path has multiple links, add all their costs to get the total route cost.

---

### Link State Advertisements (LSAs)
- **Purpose:** Share network topology information between OSPF routers.
- **Functions:**
  - **Discover neighbors** (find other OSPF routers)
  - **Exchange route information**
  - **Monitor neighbors and link status** (detect link failures quickly)
- **Efficiency:** Only send changes, not the whole table every time (unlike RIP).

---

### OSPF Areas
- **Definition:** Logical groupings of routers to reduce complexity.
- **Benefit:**  
  - Simplifies administration.
  - Keeps routing tables smaller.
  - Limits LSA flooding to within an area.
- **Backbone Area:** Area 0 – all other areas connect here.

---

💡 **Memory Hooks:**
- **Cost = Road quality** → faster link = cheaper cost.
- **LSAs** = "gossip" about the network map, but only when something changes.
- **Areas** = "districts" in a city → reduces noise and keeps things organized.
---
## OSPF – Multi-Area Implementation

### What is an Area?
- Logical grouping of OSPF routers.
- **Inside an area** – Every router has a full map of all networks/routes in that area.
- **Purpose:** Reduce LSA flooding, keep routing tables smaller, simplify admin.

---

### Area 0 – The Backbone
- **Always** the central area in OSPF.
- All other areas **must connect directly to Area 0**.
- No direct connections between non-backbone areas (e.g., Area 1 ↔ Area 2 is not allowed without going through Area 0).
- Often acts as a **transit area** in large networks.

---

### Area Border Routers (ABRs)
- Connect **Area 0** to another area.
- Maintain **separate link-state databases** for each area they connect to.
- Can summarize routes from one area before advertising them into another (reduces table size).

---

### Key Rules
1. **Area 0** is the hub; others are spokes.
2. **ABRs** are the gateways between backbone and non-backbone areas.
3. Multi-area design improves scalability and performance in large OSPF deployments.

---

💡 **Memory Hooks**
- **Area 0 = "The Airport Hub"** – All flights (areas) connect through it.
- **ABR = Customs Officer** – Controls what routes enter/leave an area.
- If an area can’t reach Area 0 → routing breaks.
---
## EIGRP – Enhanced Interior Gateway Routing Protocol (Hybrid)

### Background
- **Formerly Cisco proprietary** (now partially open standard).
- Limited support in other vendors’ gear.

---

### Features
- **Supports Classless networks** – works with subnetted networks (CIDR/VLSM).
- **Type:** “Advanced Distance Vector” (Hybrid).
  - Combines distance vector simplicity with some link-state features.
  - **Metric factors:** Bandwidth + Delay (+ Reliability + Load if configured).
- **Hop Limit:** 255 hops (RIP was only 15).

---

### Update Method
- **After convergence:** Only sends **incremental updates** when a change occurs.
- Reduces bandwidth use compared to periodic full-table updates.
- **Multicast address:** `224.0.0.10`

---

### Multiple Instances
- Routers can run multiple **EIGRP Autonomous Systems** at the same time.
  - Each EIGRP AS maintains its own topology table.

---

💡 **Memory Hooks**
- Think: “EIGRP = RIP on steroids.”
- Hybrid → Hop count + Link quality in decision-making.
- Multicast address ends in `.10` (like “ten times better than RIP”).
