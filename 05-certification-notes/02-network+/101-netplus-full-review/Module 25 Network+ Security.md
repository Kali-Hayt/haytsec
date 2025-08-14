## Module 25 – Network+ Security

### 🧱 Goal
- Protect **confidentiality, integrity, and availability** (CIA triad) of network data.
- Use a mix of **technical controls**, **policies**, and **physical security**.

---

## Authentication, Authorization, Accounting (AAA)

- **Authentication** – Verify identity (passwords, biometrics, smart cards).
- **Authorization** – Decide what an authenticated user can do.
- **Accounting** – Track and log actions for auditing.

---

## Authentication Methods
- **Password-based** (least secure, if weak).
- **Multi-factor Authentication (MFA)**: Something you know, have, are.
- **Single Sign-On (SSO)**: One login for multiple systems.
- **Federation**: Trust between identity providers (e.g., SAML, OAuth).

---

## Access Control Models
- **MAC (Mandatory Access Control)** – Strict, rule-based; used in military/government.
- **DAC (Discretionary Access Control)** – Resource owner decides access.
- **RBAC (Role-Based Access Control)** – Access based on job role.

---

## Network Security Tools & Devices
- **Firewalls** – Filter traffic by rules (hardware or software).
- **IDS / IPS** – Detect (IDS) or block (IPS) suspicious traffic.
- **Proxy Servers** – Intermediary for web requests; hides internal IPs.
- **VPN Concentrators** – Manage secure remote connections.

---

## Secure Protocols
- **HTTPS** – Encrypted HTTP (TLS/SSL).
- **SSH** – Secure remote login.
- **SFTP / FTPS** – Secure file transfer.
- **SNMPv3** – Encrypted network management.
- **IPsec** – Encrypts network layer traffic (VPNs).
- **TLS** – Common encryption for many apps.

---

## Wireless Security
- **WPA3** – Strongest standard currently.
- **WPA2-Enterprise** – Uses 802.1X for authentication.
- **Disable WEP** – Weak and easily broken.
- **Disable open networks** unless isolated guest Wi-Fi.

---

## Hardening & Best Practices
- Change default passwords.
- Patch and update firmware.
- Disable unused ports/services.
- Implement VLAN segmentation.
- Enforce least privilege access.

---

## Physical Security
- Lock network closets.
- Badge-based access.
- CCTV monitoring.
- Protect cables from tampering.

---

## Logging & Monitoring
- **Syslog** – Standardized event logging.
- **SIEM** – Security Information and Event Management for correlation & alerts.
- Enable alerts for failed logins, config changes, intrusion attempts.

---

## Incident Response Basics
1. **Identify** – Spot the issue.
2. **Contain** – Limit the damage.
3. **Eradicate** – Remove the threat.
4. **Recover** – Restore operations.
5. **Lessons Learned** – Improve defenses.

---

## Exam Pointers
✅ AAA = Authentication, Authorization, Accounting.  
✅ RBAC = access based on job role.  
✅ WPA3 = current best for Wi-Fi security.  
✅ IDS detects, IPS blocks.  
✅ Use secure versions of protocols (SSH, HTTPS, SFTP, SNMPv3).
