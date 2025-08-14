## Module 15 – Link Aggregation

### 🧱 Purpose
- Combine multiple physical links into **one logical link**.
- Increases **bandwidth** & **redundancy** between switches/servers.
- Seen as **one connection** by the devices.

---

## Benefits
- **More throughput** – Sum of all combined links.
- **Fault tolerance** – If one link fails, traffic continues on remaining links.
- **Load balancing** – Spreads traffic across all active links.
- **Simplified management** – One logical interface instead of many.

---

## How It Works
- Uses **Link Aggregation Control Protocol (LACP)** – IEEE 802.3ad.
- LACP negotiates which links join the aggregation group.
- Links must have:
  - Same speed.
  - Same duplex.
  - Connected between the same devices.

---

## Key Terms
- **Port Channel / EtherChannel** – Cisco term for aggregated link.
- **LAG (Link Aggregation Group)** – Industry term for the bundle of ports.
- **Static aggregation** – Configured manually, no LACP.
- **Dynamic aggregation** – Uses LACP to auto-detect and maintain group.

---

## Exam Pointers
✅ Protocol: LACP (IEEE 802.3ad).  
✅ Benefits: bandwidth + redundancy + load balancing.  
✅ Requirements: same speed/duplex, direct connection between devices.  
✅ Failure of one link doesn’t drop the whole connection.  

---

### 🛠 Example
- Two switches connected with 4 × 1 Gbps links.
- Without aggregation → only one link active (1 Gbps).
- With LACP → all 4 used together (4 Gbps total) + failover capability.
