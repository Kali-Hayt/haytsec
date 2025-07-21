## 🔍 Hack The Box - Common Ports & Protocols Table

| Port(s)    | Protocol/Service | TCP/UDP | Purpose / Usage                            | HTB Notes & Tools Used                          |
|------------|------------------|---------|---------------------------------------------|--------------------------------------------------|
| 21         | FTP              | TCP     | File transfers                              | `ftp`, `hydra`, check for anonymous login        |
| 22         | SSH              | TCP     | Secure shell access                         | `ssh`, `hydra`, key reuse/bruteforce             |
| 23         | Telnet           | TCP     | Remote shell (plaintext)                    | `telnet`, outdated, creds sniffing               |
| 25         | SMTP             | TCP     | Mail transfer                               | `smtp-user-enum`, relay attacks                  |
| 53         | DNS              | TCP/UDP | Domain resolution, zone transfer            | `dig`, `dnsenum`, `dnsrecon`                     |
| 67/68      | DHCP             | UDP     | Dynamic IP assignment                       | Rarely exploited directly                        |
| 69         | TFTP             | UDP     | Simple file transfers                       | No auth, file leaks                              |
| 80         | HTTP             | TCP     | Web servers                                 | `ffuf`, `gobuster`, LFI/XSS/Uploads              |
| 88         | Kerberos         | TCP/UDP | Windows authentication                      | AS-REP roast, `impacket`, `GetUserSPNs.py`       |
| 110        | POP3             | TCP     | Email (client receive)                      | Weak passwords, `hydra`                          |
| 111        | RPCbind          | TCP/UDP | Remote Procedure Call                       | `rpcinfo`, NFS detection                         |
| 135        | MS RPC/DCOM      | TCP     | Windows services                            | Interface to DCOM, used in exploits              |
| 139        | NetBIOS-SSN      | TCP     | Legacy SMB                                  | Often paired with 445, `enum4linux`              |
| 143        | IMAP             | TCP     | Email retrieval                             | Brute via `hydra`                                |
| 161/162    | SNMP             | UDP     | Network device info                         | `snmpwalk`, public strings leak data             |
| 389        | LDAP             | TCP/UDP | Directory services                          | `ldapsearch`, null bind, creds, AD enum          |
| 443        | HTTPS            | TCP     | Secure web                                  | Burp Suite, `nikto`, cert abuse                  |
| 445        | SMB              | TCP     | Windows file sharing                        | `smbclient`, `enum4linux-ng`, EternalBlue        |
| 464        | Kerberos (kpasswd)| TCP/UDP| Password changes                            | Used with Kerberos auth                          |
| 512/513/514| rsh/rexec/rlogin | TCP     | Remote shell (Unix)                         | Weak or no auth, legacy services                 |
| 873        | rsync            | TCP     | File sync (Unix)                            | Leaks files, `rsync` client                      |
| 902/903/912| VMware Services  | TCP     | Remote mgmt                                 | Target for ESXi and VM-based boxes               |
| 993/995    | IMAPS/POP3S      | TCP     | Secure email                                | Less common, may still leak creds                |
| 1080       | SOCKS Proxy      | TCP     | Tunneling                                   | Could be misused to proxy traffic                |
| 1433       | MS SQL Server    | TCP     | Database                                    | `sqsh`, weak auth, `mssqlclient.py`              |
| 1521       | Oracle DB        | TCP     | Oracle Database                             | Rare, usually in enterprise setups               |
| 2049       | NFS              | TCP/UDP | Network file sharing                        | `showmount`, mountable shares                    |
| 3306       | MySQL            | TCP     | Database                                    | Weak creds, SQLi                                 |
| 3389       | RDP              | TCP     | Windows desktop remote                      | `xfreerdp`, BlueKeep, creds brute                |
| 3690       | SVN              | TCP     | Source control                              | `svn info`, might leak code                      |
| 4444       | Metasploit       | TCP     | Default reverse shell port                  | `msfconsole` reverse shell listener              |
| 5000       | Flask Web Apps   | TCP     | Dev/test web servers                        | Often Python backends, LFI, RCE                  |
| 5432       | PostgreSQL       | TCP     | Database                                    | `psql`, `hydra`, data leak                       |
| 5900       | VNC              | TCP     | Remote GUI desktop                          | `vncviewer`, unprotected sessions                |
| 5985/5986  | WinRM            | TCP     | Remote Windows shell (PowerShell)           | `evil-winrm`, creds abuse                        |
| 6379       | Redis            | TCP     | Key-value store                             | Unauth access, RCE chains                        |
| 8000/8080/8443| HTTP Alt Ports| TCP     | Web apps                                    | Same tools as 80/443                             |
| 9200/9300  | Elasticsearch    | TCP     | Data indexing/search                        | `curl`, often unauth APIs                        |
| 27017      | MongoDB          | TCP     | NoSQL database                              | Unauth DB dump                                   |

---

## 🧱 Tips for HTB / CTF Enumeration

- `nmap -sC -sV -p- -oN allports.txt <IP>`  
- `rustscan -a <IP> --ulimit 5000 -- -sC -sV -oN rustscan.txt`  
- Always try common creds: `admin:admin`, `guest:guest`, etc.
- Bruteforce logins: `hydra`, `medusa`, `patator`
- Web fuzzing: `ffuf -u http://<IP>/FUZZ -w wordlist.txt`
- SMB: `enum4linux-ng`, `smbmap`, `crackmapexec`
- LDAP enum: `ldapsearch -x -h <IP> -b "dc=domain,dc=com"`

