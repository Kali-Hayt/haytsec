## Module 12 – VLANs (Virtual Local Area Networks)

### 🧱 What is a VLAN?
- Logical separation of networks **inside the same physical switch**.
- Devices in the same VLAN = same broadcast domain.
- Devices in different VLANs = different broadcast domains (need a router or Layer 3 switch to talk).

### 🔑 Why Use VLANs?
- **Segmentation**: Improve security and reduce unnecessary traffic.
- **Performance**: Limit broadcast storms.
- **Organization**: Group users/devices by function (e.g., Sales VLAN 10, HR VLAN 20).

### 🌈 VLAN IDs
- Range: **1–4094** (802.1Q standard).
- Common practice:
  - VLAN 1 → default (avoid using for production).
  - 1002–1005 → reserved for legacy.
- Use descriptive naming (e.g., "Finance_VLAN10").

### 📦 VLAN Tagging
- Standard: **IEEE 802.1Q** inserts a 4-byte VLAN tag into Ethernet frame.
- **Access port**: Belongs to ONE VLAN, sends/receives **untagged** frames.
- **Trunk port**: Carries traffic for multiple VLANs, sends/receives **tagged** frames.

### 🔌 Port Types
- **Access port** → connects to end devices (PCs, printers).
- **Trunk port** → connects switches, or switch ↔ router (Router-on-a-Stick).

### 🌐 Inter-VLAN Communication
- Switches alone can’t route between VLANs.
- Requires:
  - Router with subinterfaces (**Router-on-a-Stick**).
  - Layer 3 switch with routing enabled.

### ⚠ Exam-Trap Notes
- VLANs **break** a broadcast domain, but not a collision domain.
- VLAN misconfig (wrong tag/native VLAN mismatch) = **VLAN hopping** attack risk.
- Native VLAN (usually VLAN 1) → untagged traffic on a trunk. Best practice: change it from default.

---

## Exam Checklist
✅ VLAN = broadcast domain separation.  
✅ Access port = 1 VLAN, Trunk = many VLANs.  
✅ 802.1Q tagging for VLAN IDs.  
✅ Inter-VLAN traffic needs Layer 3 routing.  
✅ Native VLAN should be changed for security.

