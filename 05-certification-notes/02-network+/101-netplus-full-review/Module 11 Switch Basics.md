## Module 11 – Switch Basics (Exam-Cram)

### 🧱 What a Switch Does
- Layer 2 device (Data Link Layer) in OSI model.
- Connects devices in the same LAN.
- Uses **MAC address table** (CAM table) to forward frames.
- Operates in **full-duplex** (both send/receive at the same time) or **half-duplex**.
- **No collisions** in full-duplex mode.

### 🛠 MAC Address Table
- Learns MAC addresses from incoming frames.
- Stores MAC ↔ port mapping.
- **Unknown MAC** → floods frame out all ports (except source port).
- Entries age out after inactivity.

### 🛡 Switch vs. Hub
- **Hub**: repeats everything to all ports (Layer 1, collision domain = all devices).
- **Switch**: sends frames only to intended port (Layer 2, collision domain = 1 per port).

### 📦 Collision & Broadcast Domains
- Each switch port = separate **collision domain**.
- Entire Layer 2 switch = **one broadcast domain** (unless VLANs are used).

### 🔌 Common Switch Types
- **Unmanaged** – plug-and-play, no config.
- **Managed** – VLANs, trunking, port security, monitoring.
- **PoE switches** – supply power to devices like VoIP phones, APs, cameras.

### 🚦 Forwarding Methods
- **Store-and-forward** – receives full frame, checks errors (CRC), then forwards.
- **Cut-through** – starts forwarding after reading destination MAC (faster, no error check).
- **Fragment-free** – waits for first 64 bytes (collision detection compromise).

### 🛡 Security Basics
- **Port security**: limit MACs per port, sticky MAC, shut down on violation.
- **Disable unused ports**: reduce attack surface.

### 🌐 VLANs (Teaser for later)
- Logical separation within same switch.
- Same VLAN = same broadcast domain.
- VLAN tagging via **802.1Q** on trunk ports.

---

## Exam Pointers
- Switch = Layer 2, MAC-based forwarding.
- Hubs are Layer 1, repeat everything.
- **Full-duplex** kills collisions, but **half-duplex** still has them (CSMA/CD).
- Broadcast domains are broken by **routers**, not switches (unless VLANs).
- **CAM table** = Content Addressable Memory table (MAC address table).
