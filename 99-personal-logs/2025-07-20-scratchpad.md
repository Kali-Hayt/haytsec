---
tags:
  - scratchpad
  - sprint
  - ipv6
  - networking
created: 2025-07-20
---
## ✍️ Raw Notes  
- IPv6 uses 128-bit addressing (vs. 32-bit in IPv4)  
- Address format: eight 16-bit hexadecimal blocks (e.g., `2001:0db8:85a3::8a2e:0370:7334`)  
- Abbreviation rules:  
  - Drop leading zeros: `0034` → `34`  
  - Collapse longest sequence of all-zeros to `::` (only once)  
- IPv6 address types:  
  - Unicast: single device  
  - Multicast: multiple devices (one-to-many)  
  - Anycast: sent to the *nearest* of multiple devices  
- No broadcast in IPv6 (🔍 replaced by multicast/anycast)

---

## 💡 Ideas  
- Make a one-page IPv6 cheatsheet for HaytSec vault  
- Script to validate/normalize IPv6 addresses (CLI or Python?)  

---
## 🔧 Experiments  
- Compare `ping6` vs `ping` output in lab environments (if supported)  
- Use `ip -6 addr` to explore structure of IPv6 addresses live  
- Use `ip -6 route` to see how IPv6 routes differ from IPv4  


---

## 🔗 References  
- HaytSec Vault path: `05-certification-notes/Network+/4-addressing/ipv6.md`

---

## 🧠 Thoughts / Journal  
- IPv6 feels cleaner and more logical than IPv4, once the syntax clicks  
- Not having broadcast is a mental shift — need to reframe old assumptions  
- Not hard — just unfamiliar. Repetition will fix that.  
- Made it through 4.3 to 5.2 today. Heavy material, but moved forward with intention.  
- Labs helped lock in concepts — especially routing tools and CLI interaction.  
- Tomorrow’s mission: push cleanly through 5.2 to 7.5. It’s all about note capture, moving forward, and staying focused.

