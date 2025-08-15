## Module 20 – Application Services

### 🧱 Purpose
Covers common network application protocols, their ports, and their purposes.

---

## Common Protocols & Ports

| Protocol | Port | Transport | Purpose / Notes |
|----------|------|-----------|-----------------|
| **FTP**  | 21   | TCP       | File Transfer Protocol – unencrypted. |
| **SFTP** | 22   | TCP       | FTP over SSH – secure file transfer. |
| **TFTP** | 69   | UDP       | Trivial FTP – simple, no authentication. |
| **HTTP** | 80   | TCP       | Web traffic (insecure). |
| **HTTPS**| 443  | TCP       | Secure web traffic via TLS/SSL. |
| **SMTP** | 25   | TCP       | Send email (server-to-server). |
| **IMAP4**| 143  | TCP       | Retrieve & manage email (server folders). |
| **IMAPS**| 993  | TCP       | Secure IMAP. |
| **POP3** | 110  | TCP       | Retrieve email (downloads to client). |
| **POP3S**| 995  | TCP       | Secure POP3. |
| **Telnet**| 23  | TCP       | Remote terminal (insecure). |
| **SSH**  | 22   | TCP       | Secure remote terminal. |
| **DNS**  | 53   | UDP/TCP   | Name resolution (A, AAAA, MX, etc.). |
| **DHCP** | 67/68| UDP       | Automatic IP configuration. |
| **SNMP** | 161  | UDP       | Monitor/manage network devices. |
| **NTP**  | 123  | UDP       | Time synchronization. |
| **LDAP** | 389  | TCP/UDP   | Directory services. |
| **LDAPS**| 636  | TCP       | Secure LDAP. |
| **RDP**  | 3389 | TCP/UDP   | Remote desktop access. |

---

## Secure vs Insecure (Exam Hotspot)
- **Insecure**: Telnet, FTP, HTTP, TFTP, POP3, IMAP (unencrypted).
- **Secure**: SSH, SFTP, HTTPS, IMAPS, POP3S, LDAPS.

---

## Application Services in Action
- **Web browsing** – HTTP/HTTPS.
- **Email** – SMTP (send), POP3/IMAP (receive).
- **Remote access** – SSH or RDP.
- **File transfers** – FTP, SFTP, TFTP.
- **Device management** – SNMP.
- **Timekeeping** – NTP.
- **Directory access** – LDAP.

---

## Exam Pointers
✅ Know port numbers by heart — CompTIA loves “match the port to the service.”  
✅ Secure = encrypted (SSH, TLS/SSL).
