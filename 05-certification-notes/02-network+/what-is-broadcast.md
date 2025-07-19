## 📡 Broadcasts Happen Inside Subnets

### 🧱 What Is a Broadcast?

A **broadcast** is a Layer 2 frame sent to all devices in a subnet using the destination MAC address:

```
FF:FF:FF:FF:FF:FF
```

- Used by protocols like **ARP** and **DHCP Discover**
- The message is received by **every device** in the same **broadcast domain**

---

### 🔁 Broadcast Domain = Subnet

A **broadcast domain** is defined by the **subnet** and **VLAN configuration**.

- Devices in the **same subnet** can send and receive each other's **broadcasts**
- Devices in **different subnets** do **not** receive each other's broadcasts
- **Routers do NOT forward broadcasts** — they drop them by default

> ✅ **Broadcasts stay inside the subnet.**

---

### 🏢 Apartment Building Analogy

Imagine a **large apartment building** wired by an ISP.

Each component of the network has a real-world equivalent:

| **Network Concept** | **Real-Life Equivalent**           | **Explanation**                                      |
|---------------------|------------------------------------|------------------------------------------------------|
| ISP Router          | Basement Router                    | Provides internet access to the building             |
| Switch              | Floor Switch or Apartment Panel    | Connects multiple devices inside the same space      |
| Subnet              | Each Apartment                     | Defines who can talk directly inside one unit        |
| Broadcast Domain    | Each Apartment’s Internal Network  | Local communication (like yelling in your apartment) |
| Router              | Doorway to the Internet            | Sends mail/packages (IP packets) to the outside world|

> 🧠 **Broadcasts = shouting inside your apartment**  
> **Routing = using the door to communicate outside**

---

### 📦 Example: ARP Broadcast

In subnet `192.168.1.0/24`:

- PC1 (192.168.1.10) wants to find Printer (192.168.1.50)
- It sends:  
  **“Who has 192.168.1.50? Tell 192.168.1.10”**
- The switch **floods** this frame to all ports in the VLAN
- Only the correct device responds

---

### 🧱 Subnet = Broadcast Bubble

| Traffic Type | Scope                   | Notes                       |
|--------------|--------------------------|-----------------------------|
| Broadcast    | Inside same subnet       | Switch floods to all        |
| Multicast    | Optional, controlled     | Needs IGMP + config         |
| Unicast      | Routed if necessary      | Sent to a single MAC/IP     |

---

### 🧠 Key Facts

- Routers = **broadcast boundaries**
- VLANs = **broadcast domain splitters**
- Subnet = **broadcast zone**
- Broadcasts never reach the **internet**

> 🧱 Broadcast is local. Routing is global.
