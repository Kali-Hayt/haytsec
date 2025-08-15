### ❓ Flashcard 1

**Q:** Sid is a security engineer at a large public cloud company. He is implementing a new security service that tracks activity across the network and actively shuts down malicious activity. What security application is he implementing?  
**A:** Intrusion prevention system

---

### 🧠 Explanation:

An **Intrusion Prevention System (IPS)** goes beyond just detecting threats—it actively responds to them. It sits inline with network traffic, continuously monitoring for signs of malicious activity (like suspicious packets, known exploit patterns, or strange user behavior). When it spots something fishy, it can **block traffic, reset sessions, or quarantine systems in real time**.

Think of it like a bouncer at a club: not only watching the door but **kicking out troublemakers the moment they cause a scene**—without waiting for backup.

IPS is typically paired with IDS (Intrusion Detection System), which alerts you to threats but doesn't act on them.

---
### ❓ Flashcard 2

**Q:** BigCo has issued key fobs that have a small display that presents a numerical code that changes every two minutes. After you enter your username and password, you are then required to enter the currently displayed number. What type of authentication is this?  
**A:** Two-factor (or multifactor) authentication

---

### 🧠 Explanation:

This is classic **two-factor authentication (2FA)**. It requires:

1. **Something you know** — your username and password
    
2. **Something you have** — the key fob displaying a time-sensitive code
    

This second factor is often generated via a **time-based one-time password (TOTP)** algorithm. It's used to ensure the person logging in is in possession of a registered device (like the key fob).

It's called “multifactor” if more than two types are used (e.g., fingerprint too). But **2FA is the bare minimum these days for securing sensitive systems**—passwords alone just don’t cut it anymore.

---
### ❓ Flashcard 3

**Q:** Beth is asking you if there is a website that shows a high-level overview of her cloud deployment. What is this called?  
**A:** Dashboard

---

### 🧠 Explanation:

A **dashboard** is the main user interface provided by cloud service platforms like AWS, Azure, or GCP. Think of it like the **cockpit of a cloud deployment**—you get a centralized, visual summary of:

- Active resources (VMs, storage, networking)
    
- System health & alerts
    
- Billing and usage stats
    
- Security posture
    
- Monitoring logs and performance metrics
    

Dashboards are useful because they **condense complex environments into simple visuals**, often including charts, maps, and status indicators.

They are typically customizable so users can tailor them to show what’s most relevant to their operations.

---
### ❓ Flashcard 4

**Q:** Trevor is implementing a security application that operates in each web server that faces the Internet. He wants to track malicious attacks. What solution is he implementing?  
**A:** Host Intrusion Detection System (HIDS)

---

### 🧠 Explanation:

A **Host Intrusion Detection System (HIDS)** is software that runs on **individual machines** (like web servers) and monitors activity **locally**—unlike network-based solutions which inspect traffic between systems.

It detects signs of compromise by:

- Scanning system logs
    
- Monitoring file changes
    
- Watching running processes
    
- Analyzing resource usage patterns
    

This makes it ideal for **tracking attacks** like:

- Web defacements
    
- Unauthorized file modifications
    
- Privilege escalation attempts
    
- Malware dropped on a single host
    

Since Trevor wants visibility on attacks targeting _each server_, HIDS is the best fit—**focused, granular protection per endpoint**.

---
### ❓ Flashcard 5

**Q:** What is storage that does not survive a VM restart called?  
**A:** Ephemeral

---

### 🧠 Explanation:

**Ephemeral storage** is temporary and **tied to the lifecycle of the virtual machine (VM)**. Once the VM is **stopped, restarted, or terminated**, any data stored in ephemeral volumes is **immediately lost**.

You’ll typically see ephemeral storage used for:

- **Temporary cache space**
    
- **Scratch disk** for compute operations
    
- **Swap space** or buffer zones
    

This storage is **fast** but **not backed up**, so it’s best for workloads where **data loss is acceptable**.

🧨 Think of it like a whiteboard: great for scribbling quick ideas, but it’s wiped clean when the session ends.

💡 Pro Tip: For persistent data (like logs, databases, or saved files), always use **durable block or object storage**—not ephemeral.

---
### ❓ Flashcard 6

**Q:** What cloud service contains an ordered rule set that contains permit and deny statements and is used to protect cloud-based devices?  
**A:** Firewall

---

### 🧠 Explanation:

A **firewall** is a security system that monitors and controls incoming and outgoing network traffic based on **predetermined security rules**.

In the cloud, these rules are applied as:

- **Permit (Allow)** – Let traffic through
    
- **Deny (Block)** – Stop traffic dead in its tracks
    

These rules are **ordered**, which means the firewall reads from **top to bottom** and stops at the first match. Think of it like a bouncer with a guest list—they check names in order, and once they find a match, they stop looking.

Cloud firewalls operate in two ways:

1. **Network-based firewalls** – Protect subnets or entire virtual networks
    
2. **Host-based firewalls** – Installed directly on virtual machines to control access
    

💡 Modern firewalls also support **deep packet inspection**, **intrusion detection**, and **geofencing**.

📌 In AWS, these are called **Security Groups** or **Network ACLs**. In Azure, think **NSGs (Network Security Groups)**.

---
### ❓ Flashcard 7

**Q:** What is a software-controlled machine-to-machine interface called?  
**A:** Application Programming Interface (API)

---

### 🧠 Explanation:

An **API (Application Programming Interface)** is a set of instructions and protocols that allow software applications to **communicate with each other**. Think of it as a digital **middleman** that handles requests and responses between systems—like a waiter between a customer (your script) and a kitchen (the service).

In cloud environments, APIs are **how you control everything**:

- Spin up virtual machines
    
- Manage storage buckets
    
- Automate network rules
    
- Fetch logs, set permissions, update databases—you name it
    

APIs are key to **automation** and **integration**. They enable Infrastructure as Code (IaC), DevOps pipelines, and cloud security tooling.

🔧 APIs often use:

- **REST (Representational State Transfer)** – Lightweight, uses HTTP
    
- **SOAP (Simple Object Access Protocol)** – Heavier, XML-based, more secure/strict
    
- **RPC/gRPC** – Fast and efficient for internal system calls
    

📦 Example:

- AWS: `boto3` Python library hits AWS APIs
    
- Azure: Azure CLI wraps their REST API
    
- GCP: `gcloud` CLI uses APIs under the hood

---
### ❓ Flashcard 8

**Q:** Name the visual representation of your current cloud operations.  
**A:** Dashboard

---

### 🧠 Explanation:

A **dashboard** in cloud computing is like the cockpit of an airplane—it gives you real-time, visual insight into your cloud environment's status and performance.

It typically displays:

- **System health** (e.g., VM uptime, CPU/memory usage)
    
- **Network traffic** and latency metrics
    
- **Security alerts** or compliance statuses
    
- **Billing information**
    
- **Storage usage**
    
- **Service logs or events**
    

🧭 Dashboards are crucial for:

- **Monitoring performance**
    
- **Detecting anomalies early**
    
- **Maintaining SLAs**
    
- **Enabling proactive incident response**
    

🛠️ Tools that provide dashboards:

- **AWS CloudWatch**
    
- **Azure Monitor**
    
- **Google Cloud Console**
    
- **Grafana, Datadog, Splunk** (third-party)
    

Dashboards offer **at-a-glance control and insight**, and you can often **customize them** to display only the KPIs you care about.