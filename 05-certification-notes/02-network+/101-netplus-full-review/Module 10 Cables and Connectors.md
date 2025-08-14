## 📜 Ethernet Naming Format (IEEE 802.3)

### Structure
`[x]BASE[y]`

- **BASE** → Baseband transmission (dedicated channel for data; not shared with TV or voice).
- **x** → Speed in **Mbps** (unless otherwise specified, e.g., 1000BASE = 1 Gbps).
- **y** → Media type (how the signal travels).

---

### 📦 Media Type (y)

#### Letters
- **T** → Twisted Pair (copper)
- **F** → Fiber optic
- Other letters → Special cases (e.g., SX, LX for fiber variants)

#### Numbers
- Show **max cable segment length** in **hundreds of meters** for coax.
- Example: `10BASE5` → Up to 500 meters (thick coax)

---

### 💡 Examples
- `10BASE-T` → 10 Mbps, baseband, twisted pair  
- `100BASE-FX` → 100 Mbps, baseband, fiber  
- `1000BASE-SX` → 1 Gbps, baseband, short-range fiber  
- `10BASE2` → 10 Mbps, baseband, 200 meters of thin coax  

---

### 🧠 Exam Tip
If you know:
1. **BASE** means baseband
2. The number in front is **speed**
3. The letter/number after tells **media & length**

…you can decode *any* Ethernet type you see.

---
## Twisted Pair

- Most common LAN cable in use today
- Commonly called **Ethernet Cable** or **LAN Cable**
- Cheap
- Good speed options
- Supports **Half-** and **Full-Duplex**
- Reasonable cable length:
  - **100 meters** (ideal)
  - Good practice to terminate before 100 meters
- Colour-coded pairs twisted together:
  - Nearly eliminates **crosstalk**
---
## Unshielded Twisted Pair (UTP)

- **8 wires**
  - 4 colour-coded pairs
- **Twisting different per pair**
- Nearly eliminates **crosstalk**
- Minimises **minor interference**
  - Common sources: office/residential electrical noise
- Well priced
- Easy to work with
---
## Shielded Twisted Pair (STP)

- Still **8 wires** in **4 colour-coded pairs**
- Includes **shielding**
  - Usually metallic foil
- Requires **shielded RJ-45 connector**
- Various kinds of shielding exist
- Drastically reduces (sometimes prevents) **external interference** in electrically noisy environments
  - Common in **industrial environments**
---

## Crossover Cable Basics

- **Purpose:** Connect two similar devices directly (PC↔PC, switch↔switch) without needing an intermediate device.
- **How it works:** Swaps the TX and RX pairs so each device’s "talk" line connects to the other’s "listen" line.

---

## T568A vs T568B Standards

- Both define the **color order** of the 8 wires in an Ethernet cable.
- Difference is mainly the **green** and **orange** pairs are swapped.
- **T568A**:
  1. White/Green  
  2. Green  
  3. White/Orange  
  4. Blue  
  5. White/Blue  
  6. Orange  
  7. White/Brown  
  8. Brown  
- **T568B**:
  1. White/Orange  
  2. Orange  
  3. White/Green  
  4. Blue  
  5. White/Blue  
  6. Green  
  7. White/Brown  
  8. Brown  

---

## Popularity:
- **North America:** T568B is most common.
- **Some other regions & government contracts:** T568A is preferred.
- **Crossover Cable:** One end wired as **T568A**, the other as **T568B**.

---

## Modern Note:
- Many newer Ethernet ports are **auto-MDI/MDIX**, meaning they detect and swap TX/RX automatically — so crossover cables aren’t always necessary anymore.
---
## Rollover Cable (Console Cable)

- **Purpose:** Connect a computer’s serial port (or USB-to-serial adapter) to a network device’s console port for configuration.
- **Main use case:** Talking to routers, switches, and other gear at a low level — before network settings even exist.
- **Special wiring:** Pin 1 on one end connects to pin 8 on the other, pin 2 → pin 7, pin 3 → pin 6, etc.
  - Literally a *rolled over* wiring — the wire order is reversed end-to-end.
- **Connector:** Often RJ-45 at both ends (with an adapter to DB-9 serial if needed).
- **Color:** Cisco traditionally used flat, light blue cables for rollover.
- **NOT** for Ethernet data — only for serial console communication.

---

## Mental picture:
Think of it like an **emergency phone line** between your PC and the device — no internet, no IP addresses, just direct "command line" access to tell the box what to do.

---
## 🧱 Fiber Optic Cable Layers

- **Core** – The glass (or sometimes plastic) center where the light actually travels.
- **Cladding** – Surrounds the core, made of a material with a lower refractive index to keep the light bouncing inside (total internal reflection).
- **Coating** – A protective plastic buffer right around the cladding to shield it from physical damage and moisture.
- **Strengthening Layer** – Often Kevlar® fibers, prevents the cable from stretching or breaking when pulled.
- **Outer Jacket** – The colored protective layer you see from the outside, gives the cable environmental resistance and helps identify type.

---
## Single Mode vs Multi Mode Fiber

### Single Mode Fiber
- ~8 to 10 micron core  
  - Smaller  
  - More and better cladding  
- **1310 / 1550 nm wavelength**  
  - LASER based emitter  
- More expensive  
- Suitable for long distances  
  - WANs  

### Multi Mode Fiber
- ~50 to 60 micron core  
  - Larger  
  - Less and inferior cladding  
- **850 / 1300 nm wavelength**  
  - Diode based emitter  
- Cheaper  
- Suitable for short distances  
  - LANs  
---
