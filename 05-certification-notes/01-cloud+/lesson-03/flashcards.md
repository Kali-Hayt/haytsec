### 🃏 Flashcard 1

**Q:**  
Hank is a security engineer for his publicly traded company. For secure logins, he requires users to log in with something they have and something they know.  
**What type of authentication is this?**

**A:**  
**Multifactor**

**🧠 Explanation:**  
Multifactor authentication (MFA) strengthens security by requiring users to provide two or more verification factors. In this case:

- "Something they know" = password or PIN
    
- "Something they have" = a token, smartcard, or mobile app
    

By combining different categories of factors, MFA significantly reduces the risk of unauthorized access—even if one factor (like a password) is compromised.

---
### 🃏 Flashcard 2

**Q:**  
What is the process called when a user enters their username and password to access a cloud-based server?

**A:**  
**Authentication**

**🧠 Explanation:**  
Authentication is the process of verifying a user's identity—basically answering the question: **"Are you who you say you are?"**  
When a user enters a username and password, the system compares those credentials to stored values. If they match, access is granted (assuming proper authorization follows).

This is the **first line of defense** in any security model and typically falls under **“something you know”** in authentication factor categories.

---
### 🃏 Flashcard 3

**Q:**  
Mike works for a medical records company in the United States that is planning on migrating customer records to a public cloud to accommodate growth. You have been brought on to the migration team as a Cloud+ certified consultant. What governmental requirement must Mike ensure the cloud provider meets before considering them as a potential solution?

**A:**  
**HIPAA**

**🧠 Explanation:**  
**HIPAA** stands for the **Health Insurance Portability and Accountability Act**. It sets the standard for protecting sensitive **patient health information (PHI)** in the United States.

When dealing with **electronic health records**, cloud providers **must be HIPAA-compliant**. That means they need to:

- Encrypt patient data (in transit and at rest)
    
- Restrict access using RBAC and auditing
    
- Sign **Business Associate Agreements (BAAs)** with the healthcare provider
    
- Maintain proper breach notification protocols
    

⚠️ **If a cloud provider isn’t HIPAA-compliant, it’s a legal and financial risk** for any healthcare organization to use them.

---
### 🃏 Flashcard 4

**Q:**  
What corporate process document outlines a firm’s responsibility in safely deploying a fleet of database servers to the public cloud?

**A:**  
**Security policy**

**🧠 Explanation:**  
A **security policy** is an official corporate document that defines how an organization protects its IT infrastructure, including cloud-based assets.

When deploying **database servers to the cloud**, the security policy covers:

- **Access control rules** (who can access what)
    
- **Encryption requirements** for data at rest and in transit
    
- **Logging and monitoring** expectations
    
- **Backup strategies** and **incident response**
    
- **Compliance mandates** (e.g., PCI DSS, GDPR)
    

💼 Think of it as the **blueprint** for security—**without it, teams may overlook critical safeguards**.

---
### 🃏 Flashcard 5

**Q:**  
You are performing a security audit on a newly launched e-commerce site hosted on a private cloud. You are investigating the Internet-facing Windows servers and notice that many user accounts are configured to the operations staff. What would you need to do to the unused accounts to harden the servers?

**A:**  
**Disable the accounts**

**🧠 Explanation:**  
Unused accounts are **low-hanging fruit** for attackers. If a forgotten or inactive account still exists—and especially if it has elevated privileges—it can be exploited to gain unauthorized access.

🔒 **Disabling** these accounts is a foundational **hardening** step. It ensures that only currently authorized users can interact with the system.

- This is part of **least privilege** and **account lifecycle management**.
    
- You can audit periodically to detect stale accounts.
    
- In Windows, you can disable accounts via **Active Directory** or **Local Users and Groups**.
    

💡 **Best practice:** Disable first, delete later after verification. This allows temporary reactivation if needed without security gaps.

---
### 🃏 Flashcard 6

**Q:**  
Terri is auditing the middle-tier Linux servers on her private cloud deployment and notices many services that should not be running. As a security consultant, what actions would you recommend she take?

**A:**  
**Disable the services**

**🧠 Explanation:**  
Every running service is a potential **entry point** for attackers. If it's not needed, it's a **liability**.

This falls under the security principle of **minimizing the attack surface**. Services that are unused should be disabled or uninstalled to:

- Prevent exploitation of vulnerable software
    
- Reduce system resource usage
    
- Simplify patching and auditing
    

🔧 **On Linux**, use tools like `systemctl`, `chkconfig`, or `service` to view and manage active services.

💡 **Example:** If a server doesn’t need FTP or Telnet, those should be shut down immediately—both are notorious for poor security.

🔐 Bottom line: If it doesn’t serve the system’s mission, **cut it loose**.

---
### 🃏 Flashcard 7

**Q:**  
Zander is a database administrator for your private cloud operations. He is planning on attending a user conference in Austin, Texas, but wants to be able to connect to the database from his hotel in case an emergency arises. As a security consultant, which security system would you set up for his VPN?

**A:**  
**IPsec**

**🧠 Explanation:**  
**IPsec (Internet Protocol Security)** is a secure network protocol suite used to encrypt and authenticate data at the **network layer**. It’s commonly used in **VPNs** to protect sensitive traffic over the internet.

For remote access to a **private cloud database**, IPsec offers:

- 🔐 **Strong encryption and integrity checks**
    
- 🌍 **Secure remote access across untrusted networks (like hotel Wi-Fi)**
    
- 🧱 Works well with firewalls and security policies
    

💡 **Use case analogy**: Think of IPsec as creating a **secure, invisible tunnel** from Zander’s laptop straight into your datacenter—with nobody peeking inside.

✅ Bonus: IPsec supports both **site-to-site** and **client-to-site** VPN configurations, which makes it flexible for mobile users like Zander.

---
### 🃏 Flashcard 8

**Q:**  
A private cloud deployment is worried about its first line of defense against attacks to its Internet-facing e-commerce web servers. Delbert is a security consultant. What solution should he implement?

**A:**  
**Firewall**

**🧠 Explanation:**  
A **firewall** is your **first line of defense**—a digital gatekeeper that controls incoming and outgoing traffic based on a set of rules.

- 🔥 It can block or allow traffic based on **IP address**, **port number**, **protocol**, or **application**.
    
- 🌐 For **Internet-facing web servers**, firewalls prevent unauthorized access attempts, port scans, and DDoS attacks.
    
- 🔒 They help enforce **network segmentation**—isolating sensitive systems from public access.
    

💡 **Think of a firewall like a nightclub bouncer**—it checks IDs, filters out the troublemakers, and only lets in authorized guests. In cloud architecture, it’s the barrier between the wild internet and your backend systems.

🧱 Bonus: Use both **network firewalls** and **host-based firewalls** for layered protection (defense-in-depth).

---
### 🃏 Flashcard 9

**Q:**  
Charles wants to offer his user base a selection of two-factor authentication solutions. What two options are there?

**A:**  
**Key fob and smartphone**

**🧠 Explanation:**  
This question tests your understanding of **multi-factor authentication (MFA)**—specifically **something you have**.

A **key fob** is a physical hardware token that generates one-time passcodes. A **smartphone** can do the same using apps like Google Authenticator or Duo Mobile.

Both of these count as **"something you have"**, which complements:

- **Something you know** (like a password)
    
- **Something you are** (like a fingerprint)
    

📱 + 🔐 = Stronger security!

💡 **Real-world example:** A user logs in with a password (knowledge) and then confirms a push notification on their phone (possession). If one method is compromised, the attacker still can’t get in.

---
### 🃏 Flashcard 10

**Q:**  
What web security technology is implemented with HTTPS?

**A:**  
**SSL/TLS**

**🧠 Explanation:**  
**HTTPS** stands for **HyperText Transfer Protocol Secure**, and it's made secure by **SSL (Secure Sockets Layer)** or more commonly now, **TLS (Transport Layer Security)**.

- **SSL** was the original protocol, but it's outdated and deprecated.
    
- **TLS** is the modern, secure replacement and is what browsers actually use today—TLS 1.2 and 1.3 are the current standards.
    

🔐 **What it does:**

- Encrypts data sent between your browser and a web server
    
- Prevents **eavesdropping**, **tampering**, and **man-in-the-middle attacks**
    
- Shows the 🔒 padlock in the browser bar (which users have learned to trust)
    

💡 **Fun fact:** Even though we say “SSL certificates,” they usually use **TLS** under the hood. The name just stuck.

---
### 🃏 Flashcard 11

**Q:**  
Porter is a cloud administrator who is configuring access for the storage administration team. He does not want to add rights for every user and is asking you if there is a more efficient way to administer rights for the storage group. What user administrative approach would you recommend he implement?

**A:**  
**Groups**

**🧠 Explanation:**  
Managing users individually is a nightmare as the team grows. Instead, you can assign permissions to **groups**, and then simply add or remove users from those groups.

✅ **Why this is smart:**

- Assign permissions **once** to the group (e.g., `StorageAdmins`)
    
- Any user added to that group **inherits those permissions**
    
- Saves **tons of time** and **reduces human error**
    

📌 **Example:**  
Porter creates a `StorageAdmins` group with the right access policies. Now when a new team member joins, he just drops them into the group. Done.

💡 Groups are a key feature in **RBAC (Role-Based Access Control)** and supported by IAM systems in AWS, Azure, GCP, and beyond.