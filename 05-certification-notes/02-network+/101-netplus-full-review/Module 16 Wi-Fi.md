## Module 16 – Wi-Fi Basics

### 🧱 Purpose
- Wireless networking using **IEEE 802.11** standards.
- Operates at **Layer 1 (Physical)** & **Layer 2 (Data Link)**.

---

## Wi-Fi Standards

| Standard | Freq (GHz) | Max Speed* | Max Range | Notes |
|----------|------------|------------|-----------|-------|
| 802.11a  | 5          | 54 Mbps    | ~35 m     | Early 5 GHz standard, less interference. |
| 802.11b  | 2.4        | 11 Mbps    | ~100 m    | Long range, slow, crowded band. |
| 802.11g  | 2.4        | 54 Mbps    | ~100 m    | Backwards-compatible with b. |
| 802.11n  | 2.4/5      | 600 Mbps   | ~70 m     | MIMO introduced. |
| 802.11ac | 5          | 6.9 Gbps   | ~35 m     | Multi-user MIMO (MU-MIMO). |
| 802.11ax | 2.4/5/6    | 9.6 Gbps   | Varies    | Wi-Fi 6, OFDMA, better dense-area performance. |

\*Max speeds are theoretical.

---

## Wi-Fi Frequencies
- **2.4 GHz**:
  - Longer range, better wall penetration.
  - More interference (Bluetooth, microwaves).
  - Channels 1, 6, 11 are non-overlapping in US.
- **5 GHz**:
  - Shorter range, less interference.
  - More non-overlapping channels.
- **6 GHz**:
  - New in Wi-Fi 6E, high throughput, shorter range.

---

## Security Modes
- **Open** – No authentication; avoid in secure networks.
- **WEP** – Outdated, easily cracked.
- **WPA** – TKIP encryption, weak today.
- **WPA2** – AES encryption, still common.
- **WPA3** – Latest, improved key exchange & encryption.

---

## Key Concepts
- **SSID** – Network name broadcast by AP.
- **BSSID** – AP’s MAC address.
- **Basic Service Set (BSS)** – One AP + its clients.
- **Extended Service Set (ESS)** – Multiple APs with same SSID.
- **Roaming** – Moving between APs within same ESS.
- **Ad-hoc** – Devices connect directly, no AP.
- **Infrastructure** – Uses AP to connect devices.

---

## Antenna Types
- **Omnidirectional** – 360° coverage (common in APs).
- **Directional** – Focused beam for long distance (Yagi, parabolic).
- **MIMO / MU-MIMO** – Multiple antennas for parallel data streams.

---

## Exam Pointers
✅ 802.11 = Wi-Fi standard family.  
✅ Channels 1, 6, 11 are non-overlapping in 2.4 GHz (US).  
✅ WPA3 = most secure; WEP = obsolete.  
✅ MIMO = Multiple Input, Multiple Output (parallel streams).  
✅ Frequencies affect range & interference.  
