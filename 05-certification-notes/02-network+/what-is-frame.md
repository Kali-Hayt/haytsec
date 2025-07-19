## 🧱 What Is a Frame?

A **frame** is the data unit used at **Layer 2 (Data Link Layer)** of the OSI model.

> ✅ **Frame = Layer 2 = Switches + MAC Addresses**

Frames are how devices on the same local network (like Ethernet or Wi-Fi) communicate using **MAC addresses**.

---

## 📦 OSI Model and Data Units

| OSI Layer | Data Unit | Example |
|-----------|------------|---------|
| 7 – Application | Data     | HTTP, DNS, etc. |
| 4 – Transport   | Segment  | TCP or UDP header + data |
| 3 – Network     | Packet   | IP header + payload |
| 2 – Data Link   | **Frame**| Ethernet frame |
| 1 – Physical    | Bits     | 1s and 0s on the wire |

---

## 🧠 What’s Inside a Frame?

An Ethernet frame contains:

- **Destination MAC address**
- **Source MAC address**
- **EtherType** (e.g. IPv4, ARP)
- **Payload** (usually an IP packet)
- **FCS** (Frame Check Sequence — error check)

---

## 🚦 Who Uses Frames?

- **Switches** use frames to **forward traffic based on MAC addresses**
- Switches **ignore IPs** and only look at the **Ethernet (Layer 2) header**
- Frames are only valid **within the local network segment**

> Switch sees a frame → reads the destination MAC → forwards/floods accordingly

---

## 🧁 Cupcake Analogy (Layer Cake)

Imagine sending a cupcake:

- **Segment** = Cupcake in a box with a label (TCP info)
- **Packet** = That box wrapped in shipping paper (IP info)
- **Frame** = Final wrapping + address sticker (MAC info)
- **Bits** = The electrical signals or Wi-Fi waves that carry it

---

## 🧠 Quick Summary: Frame vs Packet vs Segment

| Term     | OSI Layer | Used By     | Focus                   |
|----------|------------|-------------|--------------------------|
| Segment  | 4          | TCP/UDP     | Ports, reliability       |
| Packet   | 3          | Routers     | IP addresses, routing    |
| **Frame**| 2          | Switches    | MAC addresses, delivery  |
| Bits     | 1          | NICs, media | Physical transmission    |

> ✅ **Frame = Local delivery (MAC)**  
> ✅ **Packet = Routed delivery (IP)**  
> ✅ **Segment = Application-to-application flow (Ports)**

---

### 🔁 Final Note:

- Frames stay **within the same broadcast domain**
- When a frame leaves a subnet, the router **strips the frame** and builds a new one for the next hop

> 🧱 **"Frame" = Switch-level delivery vehicle for your IP packet**

