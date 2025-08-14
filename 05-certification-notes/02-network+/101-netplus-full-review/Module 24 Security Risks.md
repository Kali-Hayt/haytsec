## Module 24 – Security Risks

### 🧱 Why Security Risks Matter
- Networks are constant targets for **data theft, disruption, and unauthorized access**.
- Threats can come from **outside** (hackers, malware) or **inside** (disgruntled employees, accidental misuse).
- Mitigation = combination of **technical controls**, **policies**, and **user awareness**.

---

## Common Network Threats

### 1. **DoS / DDoS** (Denial of Service / Distributed DoS)
- Overwhelm a target with traffic until it’s unusable.
- **DDoS** uses many compromised systems (botnet).
- **Mitigation:** Traffic filtering, rate limiting, DDoS protection services.

### 2. **Man-in-the-Middle (MITM)**
- Attacker intercepts and alters communications between two parties.
- **Mitigation:** Encryption (TLS/SSL, VPN), certificate validation.

### 3. **Spoofing**
- Pretending to be another device or user.
  - **IP spoofing** – fake source IP.
  - **MAC spoofing** – fake MAC address.
- **Mitigation:** DHCP snooping, dynamic ARP inspection, port security.

### 4. **Phishing / Spear Phishing**
- Deceptive emails or messages to steal credentials/data.
- **Mitigation:** User training, spam filters, multi-factor authentication.

### 5. **Malware & Ransomware**
- Malicious software to damage, steal, or lock data.
- **Mitigation:** Antivirus, patching, least privilege access.

### 6. **Eavesdropping / Packet Sniffing**
- Capturing unencrypted network traffic.
- **Mitigation:** Encryption (WPA3, TLS, VPN).

### 7. **Privilege Escalation**
- Gaining higher permissions than intended.
- **Mitigation:** Strong access controls, patching, monitoring.

---

## Physical Security Risks
- **Unauthorized entry** into server rooms.
- **Cable tapping**.
- **Equipment theft**.
- **Mitigation:** Locks, CCTV, badge access, secured cable routes.

---

## Configuration & Policy Risks
- **Default passwords** left unchanged.
- **Poorly configured firewalls or ACLs**.
- **Lack of patching**.
- **Mitigation:** Hardening procedures, regular audits, change control.

---

## Insider Threats
- **Accidental:** User clicks phishing link.
- **Malicious:** Employee steals data.
- **Mitigation:** Monitoring, access controls, user education.

---

## Defense in Depth
- Multiple security layers: **Physical → Network → Host → Application → Data**.
- Redundancy ensures one failure doesn’t expose everything.

---

## Exam Pointers
✅ DDoS = many systems attacking at once.  
✅ MITM = intercepted communications.  
✅ Spoofing = impersonating a trusted system.  
✅ Defense in Depth = multiple overlapping protections.  
✅ User training is as important as technical controls.
