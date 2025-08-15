## Module 13 – VXLAN (Virtual Extensible LAN)

### 🧱 What is VXLAN?
- Network virtualization tech that **extends Layer 2 networks over Layer 3**.
- Encapsulates Ethernet frames inside **UDP** packets.
- Designed to overcome the 4,094 VLAN ID limit.

### 🔑 Why VXLAN?
- VLAN max IDs: 1–4094 → not enough for massive cloud/datacenter setups.
- VXLAN supports **16 million** network IDs (VNI: VXLAN Network Identifier).
- Works across Layer 3 boundaries → good for geographically separated networks.

### 📦 How VXLAN Works
1. **Encapsulation**:
   - Original Ethernet frame gets wrapped inside UDP, with VXLAN header.
   - Uses **VNI** (24-bit) instead of VLAN ID (12-bit).
2. **Transport**:
   - Moves across IP-based network (L3).
3. **Decapsulation**:
   - At destination, VXLAN header removed, Ethernet frame restored.

### 🔌 Key Components
- **VTEP** (VXLAN Tunnel Endpoint):
  - Device or switch interface that encapsulates/decapsulates VXLAN traffic.
  - Can be in software (hypervisors) or hardware (switches).
- **Underlay network**:
  - Physical L3 network that carries VXLAN traffic.
- **Overlay network**:
  - Virtual network created by VXLAN.

### 🌐 Benefits
- Scalability: Millions of segments.
- Flexibility: L2 adjacency over L3.
- VM Mobility: Keeps same IP/MAC when moving VMs across datacenters.
- Cloud-ready: Fits with SDN and multi-tenant setups.

### ⚠ Exam-Trap Notes
- VXLAN ≠ VLAN, but conceptually similar.
- VXLAN is **Layer 2 over Layer 3** tunneling using UDP port **4789**.
- Needs multicast or control plane (like EVPN) for MAC address learning.

---

## Exam Checklist
✅ VXLAN = scalable VLAN replacement.  
✅ Uses **VNI** (16 million IDs) instead of VLAN ID.  
✅ Encapsulates Ethernet in UDP (port 4789).  
✅ Needs VTEPs to function.  
✅ Runs over Layer 3, creates virtual Layer 2 networks.  
