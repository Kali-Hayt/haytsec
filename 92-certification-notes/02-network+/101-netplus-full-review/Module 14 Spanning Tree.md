## Module 14 – Spanning Tree Protocol (STP)

### 🧱 Purpose
- Prevents **Layer 2 loops** in switched networks.
- Loops can cause:
  - **Broadcast storms** (endless looping of broadcast frames).
  - **Multiple frame copies** (MAC table instability).
- STP **blocks** redundant paths until needed.

---

## How It Works

1. **Election of Root Bridge**:
   - Switches exchange **Bridge Protocol Data Units (BPDUs)**.
   - Switch with **lowest bridge ID** (priority + MAC) becomes **Root Bridge**.

2. **Path Selection**:
   - STP calculates the **shortest path** to Root Bridge based on path cost.
   - Path cost depends on link speed (faster = lower cost).

3. **Port Roles**:
   - **Root Port (RP)** – Best path toward the Root Bridge.
   - **Designated Port (DP)** – Best port on a segment to forward traffic.
   - **Blocked Port** – Redundant path put in standby to avoid loops.

4. **Port States**:
   - **Blocking** – Listens for BPDUs, no data forwarding.
   - **Listening** – Preparing to forward, no data yet.
   - **Learning** – Builds MAC table, still no forwarding.
   - **Forwarding** – Passes traffic normally.
   - **Disabled** – Admin down.

---

## STP Flavors
- **STP (802.1D)** – Original, ~50 sec convergence.
- **RSTP (802.1w)** – Rapid STP, ~6 sec convergence.
- **MSTP (802.1s)** – Multiple spanning tree instances for multiple VLANs.

---

## Key Numbers (Exam Tips)
- **Bridge Priority** default = 32768.
- Lower priority wins Root Bridge election.
- Path costs (common):
  - 10 Mbps = 100
  - 100 Mbps = 19
  - 1 Gbps = 4
  - 10 Gbps = 2

---

## Why It Matters
- Without STP, redundant links cause **broadcast storms** → network meltdown.
- With STP, you can have redundancy without loops.
- If a link fails, STP unblocks a backup path.

---

## Exam Checklist
✅ STP prevents Layer 2 loops using BPDUs.  
✅ Root Bridge = lowest priority + MAC.  
✅ Ports: Root, Designated, Blocked.  
✅ States: Blocking → Listening → Learning → Forwarding.  
✅ RSTP = faster convergence.  
✅ MSTP = VLAN-aware multiple instances.  
