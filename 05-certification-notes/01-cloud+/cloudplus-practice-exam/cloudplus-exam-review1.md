# QUESTION 1
**Question:** **Question:** A MySQL database operates on a multi-CPU instance that is nearing 100 percent utilization. However, the database can only run on a single server. What option is available to support the requirements of this database?

- ✅ A. Vertical scaling
- ❌ B. Cloud bursting
- ❌ C. Community cloud
- ❌ D. Horizontal scaling

### Why the others are wrong:
- - ❌ **B. Cloud bursting:** Refers to bursting into a public cloud during high load—usually for apps that can run in multiple locations. Not helpful when the database is confined to one server.
- - ❌ **C. Community cloud:** A deployment model shared by multiple organizations. Not relevant to solving compute/memory constraints.
- - ❌ **D. Horizontal scaling:** Means adding **more** servers, but the question states the DB can only run on a single server.
---
### 🧱 Notes: Vertical vs Horizontal Scaling
- **Vertical scaling (scale-up):** Increase resources (CPU, RAM, storage) *on the same server*.
- - ✅ Good for legacy systems or monolithic apps that can't run distributed.
- 🔍 Limitation: There's always a hardware max.
- **Horizontal scaling (scale-out):** Add *more servers* and distribute the load.
- - ✅ Good for stateless services, microservices, web apps.
- - ❌ Not possible when your DB can’t shard or replicate across nodes.
---
## ❓ What is MySQL?
**MySQL** is an open-source **relational database management system (RDBMS)**. It uses **SQL (Structured Query Language)** to store and retrieve data.
- 📦 Stores data in tables with rows and columns (like a spreadsheet with relationships).
- 🧱 Strong ACID compliance (Atomicity, Consistency, Isolation, Durability).
- 🔗 Common in LAMP stack: **Linux + Apache + MySQL + PHP/Python**.
- 🔧 Used for web apps, back-end systems, reporting dashboards, etc.
- ✅ It's good for structured data and supports transactions.
- ❌ Not ideal for massive unstructured data or distributed storage—that’s NoSQL territory (e.g., MongoDB, Cassandra).
---
### [Automation & Infrastructure as Code]
- ❓ **Guessed Question:**
Cloud providers and third-party automation systems can deploy and configure your resources from ______ that you can create or customize.
- - ✅ **Correct Answer:**
**B. Templates**
Templates are reusable infrastructure blueprints that define resources like VMs, networks, security groups, etc. Tools like AWS CloudFormation, Azure ARM, and Terraform use templates to automate deployments.
- 🧠 **My Understanding:**
Templates are like pre-written blueprints. Instead of clicking through setup screens for every server or service, you define everything once in a file (like JSON, YAML, or HCL) and let the automation system handle it.
- You can reuse or customize them.
- This supports **IaC (Infrastructure as Code)**.
- CloudFormation templates (AWS) or Terraform configs are great examples.
- Helps reduce human error and speeds up consistent deployments.
- 🔍 **Note:**
I guessed this answer, but it made sense because “template” sounds like something reusable or pre-built. Confirmed now.
### Why the others are wrong:
- - ❌ A. *Temtops* – Not a real term.
- - ❌ C. *Tabletops* – These are simulation exercises for testing incident response plans.
- - ❌ D. *Call trees* – Used in disaster response to define who notifies who during incidents. Not related to deployment automation.
---
### [Hypervisor Resource Monitoring]
- - ❌ **Missed Question:**
Capacity and utilization reporting often contains utilization info on which hypervisor objects? *(Select all that apply)*
- - ✅ **Correct Answers:**
- B. Network
- C. CPU
- - ❌ **Incorrect Selections:**
- A. RAM
- (Missed selecting: B. Network)
- 🧠 **My Understanding:**
Hypervisors report on **CPU** and **Network utilization** because those are key to managing performance across multiple VMs.
- **CPU**: Tracks how much processing power VMs are using.
- **Network**: Monitors bandwidth, packet flow, latency—important in shared virtual networks.
- ❌ RAM is **not typically tracked per se by the hypervisor** for utilization reporting—it’s more of a static allocation unless ballooning or swapping is enabled.
- ❌ OS version and Volume tier are **metadata**, not utilization metrics.
- 🔍 ### Why the others are wrong:
- - ❌ **A. RAM** – Memory is often allocated at VM startup, but hypervisors don’t always track real-time RAM utilization the same way they do CPU/network.
- - ❌ **D. OS version** – Doesn’t affect utilization; used more for compatibility or compliance.
- - ❌ **E. Volume tier** – Refers to storage class (standard, premium, etc.), not current usage or performance load.
- 🛠️ **Fix:**
When you see *utilization* or *performance reporting*, think: **dynamic, changing metrics**. That’s usually CPU, network, sometimes IOPS or disk usage—but not static labels or specs.
---
### [High Availability During Updates]
- - ❌ **Missed Question:**
A fleet of 20 load-balanced Internet-facing e-commerce web servers needs to be upgraded to remediate a critical bug. The company cannot afford to be offline during the update. Which method allows fixing the bug while staying online?
- - ✅ **Correct Answer:**
**B. Rolling updates**
- - ❌ **Your Answer:**
**A. Blue-green deployment**
- 🧠 **My Understanding:**
**Rolling updates** work by upgrading a subset of servers one at a time, while others keep running the older version. This avoids downtime since traffic keeps flowing to healthy servers.
- Example: 2 servers upgraded, 18 still serve users → slowly replace more.
- This is commonly used in Kubernetes or load-balanced web tiers.
- It’s great for patching critical bugs while maintaining service.
- ❌ Blue-green deployments **require two full environments** (blue = current, green = updated). You switch traffic to green *after* it’s fully tested. While also non-disruptive, it’s heavier, more resource-intensive, and **not** what the question was hinting at.
- 🔍 ### Why the others are wrong:
- - ❌ **C. QA** – Quality assurance testing is done before release, not for live updates.
- - ❌ **D. Backup target** – That’s for recovery, not online updates.
- 💡 **Key Concept:**
Use **rolling updates** for minimal-downtime fixes across *many* instances. Use **blue-green** when you want instant rollback or staging with full environment duplication.
---
### [Which of these can be used to collect performance metrics in cloud management systems?]
- ❌ **Your answer:** Elasticity
- ✅ **Correct answer:** Object
#### 🧱 Why “Object” is correct:
- In **cloud monitoring systems**, an **object** is a measurable unit—like:
- A VM instance
- A disk volume
- A CPU or network interface
- These objects **generate metrics** (CPU %, IOPS, memory usage, etc.)
- Cloud tools like **AWS CloudWatch** or **Azure Monitor** track performance by watching these **objects**.
#### - ❌ Why “Elasticity” is wrong:
- Elasticity is a **property** of the system.
- It refers to the system's **ability to scale resources** up or down in response to demand.
- It is not something that **produces metrics** on its own.
#### 🔍 Think of it like this:
- **Object = metric producer**
- **Elasticity = behavior enabled by automation/architecture**
This question is a trap if you’re thinking about cloud strategy vs. monitoring!
---
### [Object tracking metrics should be aligned with which cloud service provider requirements?]
- ✅ **Correct answer:** SLA
#### 🧱 Why this matters:
- An **SLA** (Service Level Agreement) is a formal commitment by a cloud provider to meet **specific performance and uptime targets**.
- To prove they're meeting that SLA, they use **metrics**—often tracked by object monitoring.
- Example metrics: latency, throughput, error rates, availability %
#### - ❌ Why the others are wrong:
- **RDP (Remote Desktop Protocol):** A protocol for remote access, not related to performance contracts.
- **SLW:** Not a recognized term in cloud agreements.
- **RBP:** Likely a distractor or fictional acronym.
#### 🧠 Tip:
Always tie your **monitoring goals** to the **SLA**—that’s how you prove compliance or catch violations.
---
### [Your cloud migration requirements are limited to application management only... What service model best meets the requirements?]
- ❌ **Your answer:** D. SaaS
- ✅ **Correct answer:** A. PaaS
#### 🧱 What's being tested:
- Understanding the **division of responsibility** in cloud service models:
- **IaaS**: You manage OS, middleware, and app.
- **PaaS**: You manage only the app.
- **SaaS**: You manage nothing. Provider does everything.
#### - ✅ Why A is correct:
- The question says:
> "You only need to manage the application. The provider handles OS and virtualization."
That’s **exactly what PaaS is**:
- Provider gives you the platform (OS + runtime + storage)
- You install and manage your application on top.
#### - ❌ Why D is wrong:
- **SaaS (Software as a Service)** means the cloud provider runs both the **platform** and the **application** (think Gmail, Salesforce, Dropbox).
- You don’t install your own app on a SaaS—you just use their app.
#### 🧠 Mnemonic:
IaaS = I do most
PaaS = I do app
SaaS = I do nada
---


# QUESTION 2
**Question:** **Your employer has developed a mission-critical application for the medical industry, and there can be no downtime during maintenance. You have designed a web architecture to take this into account and that allows you to have an exact copy of your production fleet that can be brought online to replace your existing deployment for patching and maintenance. What type of model did you implement?**

- ❌ A. Quality assurance
- ❌ B. Rolling updates
- ✅ C. Blue-green
- ❌ D. Backup target

### Why the others are wrong:
- - ❌ **A. Quality assurance**: QA is a testing phase, not a deployment model. It’s where you validate builds—not something that goes live for zero-downtime failover.
- - ❌ **B. Rolling updates**: This updates instances one by one, *not* a full copy you can instantly switch to. Useful, but not fast enough for critical apps.
- - ❌ **D. Backup target**: Backups are for recovery, not for immediate switch-over. They're not active environments.
---
## 💡 What is Blue-Green Deployment?
**Blue-green deployment** = two identical environments (blue and green):
- One is **live (blue)**.
- One is **standby (green)**.
- You do updates on green, test it, then **flip traffic over instantly**.
- No downtime, fast rollback possible.
Think of it like:
📦 “Blue” is your current warehouse
🆕 “Green” is your new warehouse, fully stocked and ready
🚛 You redirect deliveries to the green one at go-live—zero interruption
---
## 💉 Why it fits the *medical* scenario
> “There can be no downtime”
> “Exact copy of production fleet”
> “Brought online to replace”
This screams **mission-critical + zero-downtime + instant switchover**, which = - ✅ **Blue-Green**.
---
## 🧠 Your takeaway
If you ever see:
- **Zero downtime**
- **Switch between production clones**
- **Rollback-ready deployments**
👉 **Blue-Green is your go-to answer**.
---


# QUESTION 3
**Question:** **What type of storage can use buckets?**   ---  ## 🧱 Object Storage = Bucket-Based  - Buckets = containers to hold **objects** (files + metadata) - Common services: - AWS S3 - Azure Blob Storage - Google Cloud Storage  **Object storage is ideal for:** - Static web assets (HTML, CSS, JS) - Backups and logs - Media files (images, video) - Software repositories  Think of it like this:  📦 **Bucket** = a named container 🗂️ **Object** = a file (with metadata) dropped in the bucket 🔑 **Key** = the name/path to access it  You don’t mount it. You don’t partition it. You just **drop files into buckets over HTTP/S**.  ---  ## - ❌ Why the others are wrong  - - ❌ **Block**: Used by VMs. You format/mount volumes. No buckets. Think of a virtual SSD. - - ❌ **Data**: Not a real storage type. Too vague. - - ❌ **Disk**: Could be block storage or ephemeral, but still no buckets.  ---  ## 🔍 Common Confusion: "Object" Sounds Like a Metric  Absolutely fair. “Object” can mean a bunch of things: - In **metrics**: tracked elements (e.g., CPU, memory, etc.) - In **storage**: it means a file + metadata blob - In **OOP programming**: it means an instance of a class  So yeah—it’s one word, many worlds. Context matters.  ---  ## - ✅ Fast Memory Hook  > 🪣 **Buckets = Object Storage = S3** > 💾 **Volumes = Block Storage = EBS** > 📂 **Files = File Storage = NFS/SMB**  ---

- ✅ A. Object
- ❌ B. Block
- ❌ C. Data
- ❌ D. Disk



# QUESTION 4
**Question:** **_____ I/O is a measurable object whose metrics should be included in the baseline documentation.**   ---  ## - ✅ Correct Answer: D. Network  - "Network I/O" refers to **input/output operations over the network**—packets sent and received. - For **baseline documentation**, especially in high-speed, low-latency environments (like clustered apps or microservices), tracking **network I/O** helps you: - Set SLAs - Detect anomalies - Choose placement groups and high-throughput NICs  ---  ## Why the others are wrong:  - - ❌ **A. Memory**: Important, yes—but not I/O. It’s resource usage, not a throughput-based measurement. - - ❌ **B. CPU**: Also critical, but again, **not I/O**. This is measuring processing, not input/output operations. - - ❌ **C. Storage**: Storage I/O *is* a real thing (IOPS), but the question specifically targeted **Network I/O** as the fill-in.  ---  ## 🧱 Baseline Metrics You Should Always Track:  Even if the question laser-focused on network, in real ops you'd record all of these:  - **CPU usage** (avg, peak) - **Memory utilization** - **Disk IOPS / latency** - - ✅ **Network I/O (MBps, packet drops, etc.)** - App-specific metrics (queries per sec, req latency...)  ---  ## 🎯 Fast Takeaway  > If it has I/O in the name, it's measuring data *flow* — not just usage. > > **CPU = capacity** > **Memory = usage** > **I/O = flow rate**  ---

- ❌ A. Memory
- ❌ B. CPU
- ❌ C. Storage
- ✅ D. Network



# QUESTION 5
**Question:** **A policy change required migrating application VMs to synchronously replicated storage. One VM is located offshore. Users report that performance is slow. You check the resource usage and discover CPU utilization is at 70% and available memory is at 30%. What is the most likely cause?**   ---  ## - ✅ Correct Answer: C. The new configuration is adding latency  - **Synchronous replication** requires writes to be confirmed at **both** the primary and secondary site **before** they’re committed. - When one of those VMs is offshore—say across an ocean—you've got **geographic latency** added to every write. - That adds up fast in I/O-intensive apps.  ---  ## Why the others are wrong:  - - ❌ **A. Under allocated memory**: Nope—memory is at 30%, so there’s plenty left. - - ❌ **B. Not enough vCPU**: CPU is at 70%, not maxed out. Not the bottleneck. - - ❌ **D. App incompatibility**: The app is *running*, just slowly. That implies performance degradation, not outright incompatibility.  ---  ## 💡 Key Insight  Synchronous replication is great for **data consistency**, but it introduces **write latency**—especially over long distances. It’s not ideal when performance is priority #1.  If your architecture depends on speed (like for medical imaging or transactional systems), **asynchronous** or **local replicas** might be better.  ---  ## 🧠 Final Word  > “Latency is the silent killer of high availability.” > Even good CPU/memory won’t help if every I/O operation waits on a distant acknowledgment.  ---

- ❌ A. It is present under allocated memory on the VM.
- ❌ B. Not enough vCPU assigned.
- ✅ C. The new configuration is adding latency.
- ❌ D. The application is not compatible with new settings.



# QUESTION 6
**Question:** **You want to avoid issues leading to performance degradation. You are using Fibre Channel LANs. What can you do to restrict how initiators and targets can communicate with each other?**  Each correct answer represents a complete solution. Choose all that apply.   ---  ## - ✅ Correct Answers: B and D  ### 🟦 B. **Define zones** - **Zoning** is a SAN-specific method to control which **initiators (servers)** can see which **targets (storage)**. - Think of it like **SAN segmentation**—a privacy fence in the SAN world. - Prevents noisy neighbor problems and enhances performance.  ### 🟩 D. **Set up LUN masking** - This restricts which **Logical Unit Numbers** (storage volumes) a given initiator can access **after zoning is applied**. - Without LUN masking, initiators might see **all** LUNs even if they can’t use them, causing security and performance issues.  ---  ## - ❌ Why the others are wrong:  - **A. Break L2 with VLANs** - VLANs are good for Ethernet-based LAN segmentation, **but Fibre Channel** uses **zones**, not VLANs. - VLANs are Layer 2 network concepts—this is a **storage** layer question.  - **C. Define sources** - Not a meaningful SAN configuration term. You define **initiators and targets**, not "sources."  ---  ## 💡 Pro Tip  Fibre Channel SAN security and performance = 🧱 Zoning (who sees who) + 🧱 LUN masking (who sees what).  They go together like firewall rules + access control lists.  ---

- ❌ A. Break the L2 segment into multiple VLANs
- ✅ B. Define zones
- ❌ C. Define sources
- ✅ D. Set up LUN masking



# QUESTION 7
**Question:** **The DevOps team is requesting read/write access to a storage bucket in the public cloud that is located in a backup region. What kind of service are they requesting?**   ---  ## - ✅ Correct Answer: D. Authorization  When someone requests access to a **resource** (like a storage bucket), they are asking, "Am I allowed to do this?"  - 🔐 **Authorization (AuthZ)** = “Do I have permission to do this?” - 🔑 **Authentication (AuthN)** = “Am I who I say I am?”  In this case, access to read/write storage = **authorization** to perform actions after already being identified.  ---  ## - ❌ Why the others are wrong:  - **A. Federation** - 🔍 Federation allows identities from one domain (like Active Directory) to access resources in another domain. - This is identity sharing, not access control.  - **B. SSO (Single Sign-On)** - 🧱 SSO is about convenience—sign in once, access many services. - It handles **identity sessions**, not resource permissions.  - **C. Authentication** - - ❌ They’re not asking to **prove who they are** (AuthN), they already did that. - They now want **access rights** (AuthZ).  ---

- ❌ A. Federation
- ❌ B. SSO
- ❌ C. Authentication
- ✅ D. Authorization



# QUESTION 8
**Question:** **George is troubleshooting a SQL database in a public cloud using IaaS. Vendor found a bug and requests a rapid-deploy fix for a specific critical issue. What will George install?**  - - ❌ A. Patch - - ✅ B. Hotfix - - ❌ C. Rollback - - ❌ D. Version update  Why the others are wrong: - - ❌ Patch: More general, often scheduled, not emergency-specific. - - ❌ Rollback: Used to revert to a previous version—not to fix a new issue. - - ❌ Version update: Broad scope and not always immediate.  ---

- ✅ Hotfix = targeted fix for urgent problems.



# QUESTION 9
**Question:** **Your public cloud provider located a data center in an industrial park, no signage, with video surveillance, tall fences, and biometric controls. What type of security is this?**  - - ❌ A. Zone - - ✅ B. Infrastructure - - ❌ C. Data Center - - ❌ D. Location  Why the others are wrong: - - ❌ Zone: Refers to logical divisions in cloud (e.g., availability zones), not physical hardening. - - ❌ Data Center: Too broad, describes the place—not the *type* of security. - - ❌ Location: Just a general term, not a recognized security category.  ---

- ✅ Infrastructure = physical facility hardening (e.g., cameras, fencing, biometrics).



# QUESTION 10
**Question:** **Connie needs a scalable solution for seasonal computing spikes at an accounting firm. What public cloud services meet this need? (Choose all that apply)**   Why the others are wrong: - - ❌ B. Availability zones: These improve **fault tolerance**, not cost or scalability. - - ❌ C. Resource pooling: That's a **general cloud trait** behind the scenes—Connie needs **services**, not backend architecture.  - - ✅ A. On-demand lets you spin up resources only when needed. - - ✅ D. Pay-as-you-go aligns costs with usage—perfect for seasonal demand. - - ✅ E. Elasticity enables auto-scaling up/down as demand changes.  🔍 Bottom line: Connie needs *agility + cost control*. These 3 deliver both.  ---

- ✅ A. On-demand computing
- ❌ B. Availability zones
- ❌ C. Resource pooling
- ✅ D. Pay-as-you-go
- ✅ E. Elasticity
- ✅ Correct:



# QUESTION 11
**Question:** **License capacity can be measured in which of the following ways? (Choose all that apply)**   Why the others are wrong: - - ❌ E. Named vendors: Licensing is about *how many people/devices* are using the product—not who makes it.  ---  ## 💡 Licensing in Plain English  ### 🧱 What is licensing? Licensing = the **rules** that say who can use software, how much of it, and under what conditions.  Think of it like a movie ticket: - 🎟️ 1 ticket = 1 person (user license) - 🎟️ 1 ticket for unlimited people = site license - 🎟️ Tickets that expire = subscription licensing  ---  ## 🔢 Ways License Capacity Is Measured  - - ✅ **Usage metrics**: Based on **how much** you're using (CPU time, storage used, etc.). - - ✅ **Concurrent connections**: Limited to X number of users at the **same time**. - - ✅ **Total connections**: Could mean the **total number of endpoints** or unique systems connected. - - ✅ **Number of users**: Classic "per-seat" license model. 50 users = 50 licenses.  ---  ## 🧱 Licensing in Cloud vs Traditional  | Model                    | Example                              | Notes                            | |-------------------------|--------------------------------------|----------------------------------| | Per-user                | 1 license = 1 named user              | Microsoft 365, Adobe             | | Per-device              | 1 license per system                  | Common in labs, hospitals        | | Concurrent user         | Max X users at once                  | Good for shift-based work        | | Resource usage          | Pay for what you use (CPU, GB, etc.) | Cloud-native, flexible           | | Site-wide or enterprise | Unlimited within org                 | Expensive but simple             |  ---  ## 🛡️ In Practice (for Cloud+)  If you're managing licensing in the cloud: - Monitor usage to avoid **overages** or **non-compliance** - Choose models that **scale with the business** - Use cloud-native license tracking tools like AWS License Manager or Azure Cost Management  ---  ## 🧠 Bottom Line When they ask how license capacity is measured, they’re really ask  ---

- ✅ A. Usage metrics
- ✅ B. Concurrent connections
- ✅ C. Total connections
- ✅ D. Number of users
- ❌ E. Named vendors



# QUESTION 12
**Question:** **Which of the following RAID levels uses disk striping to spread contents of files in roughly even parts across two or more drives?**   Why the others are wrong: - - ❌ A. RAID 1 = **Mirroring**, not striping. Data is duplicated, not split. - - ❌ B. RAID 6 = Striping **with dual parity**, not just plain striping. - - ❌ C. RAID 5 = Striping **with single parity**. It uses parity blocks, not just raw striping.  ---  ## 🧱 RAID Quick Breakdown: Think Pizza Slices 🍕  | RAID | Core Function                  | Striping | Mirroring | Parity | Tolerance | Use Case                             | |------|-------------------------------|----------|-----------|--------|-----------|--------------------------------------| | 0    | Speed boost only              | - ✅ Yes   | - ❌ No     | - ❌ No  | - ❌ None    | Temp files, gaming, non-critical use | | 1    | Redundancy via copies         | - ❌ No    | - ✅ Yes    | - ❌ No  | - ✅ 1 drive | Simple backup, OS disks              | | 5    | Speed + single drive fail OK  | - ✅ Yes   | - ❌ No     | - ✅ Yes | - ✅ 1 drive | Web servers, file servers            | | 6    | Like RAID 5 but safer         | - ✅ Yes   | - ❌ No     | - ✅- ✅ Yes | - ✅ 2 drives| High-reliability apps                |  🧠 **Striping = speed**, **parity = safety**, **mirroring = backup**.  ---  ## 🧠 Bottom Line RAID 0 is the only one that uses **pure striping with no redundancy**. RAID 5/6 use striping **with parity** for fault tolerance.  ---  # QUESTION You have an update to fix a bug that was slowing down the system. What kind of update are you installing?  - - ❌ A. Rollback - - ✅ B. Patch - - ❌ C. Hotfix - - ❌ D. Version update  Why the others are wrong: - - ❌ **A. Rollback** – This reverts to a previous version, usually after a bad update. You're not undoing anything here, just fixing a bug. - - ❌ **C. Hotfix** – Hotfixes are fast, emergency fixes for **critical or security-breaking issues**, often deployed live with minimal testing. This bug sounds annoying, not catastrophic. - - ❌ **D. Version update** – That implies a major upgrade (v1.0 → v2.0), which usually adds new features, not just bug fixes.  🧱 **Patch** is the standard term for a small update meant to fix bugs, improve performance, or close minor security holes.  --- # QUESTION You are evaluating the physical layout of a large public cloud company. Your company’s operations require local data centers in Japan, Kuwait, Berlin, and Chicago to host low-latency web services for your customers. What cloud architecture should you implement?  - - ✅ A. Region - - ❌ B. Autoscaling - - ❌ C. Availability zone - - ❌ D. Pay-as-you-go  Why the others are wrong: - - ❌ **B. Autoscaling** – That controls how resources grow or shrink based on demand, not where your infrastructure is physically located. - - ❌ **C. Availability zone** – These are **within** a region, typically multiple per region, used for fault tolerance. They don’t refer to global location distribution. - - ❌ **D. Pay-as-you-go** – That’s a billing model, not architecture.  🧱 **Region** is the right call when you need geographic distribution. Each region is a physically isolated area, often with multiple AZs inside. You want **multiple regions** close to each customer base for **low latency**.  --- # QUESTION X In which access control model do administrators assign security classifications, or labels, to each user and each resource and only allow users to access a given resource if their labels are compatible?  - - ❌ A. RBAC - - ❌ B. MFA - - ✅ C. MAC - - ❌ D. DAC  Why the others are wrong: - - ❌ **RBAC** (Role-Based Access Control) is based on job functions or roles, not classification labels. It doesn't match users and resources by clearance levels. - - ❌ **MFA** (Multi-Factor Authentication) is an authentication method, not an access control model. - - ❌ **DAC** (Discretionary Access Control) gives resource owners control over access. It’s more flexible but less secure than MAC and doesn't involve mandatory classifications.  **MAC = Mandatory Access Control** - ✅  ---  # QUESTION  Which of the following methods is used by software developers to send new versions of applications rapidly?  - - ❌ A. Continuous development - - ❌ B. Continuous filtering - - ✅ C. Continuous delivery - - ❌ D. Continuous validation  Why the others are wrong: - - ❌ A. *Continuous development* isn't a formal DevOps process. It's a general idea, not a structured method for releasing code reliably. - - ❌ B. *Continuous filtering* is not a recognized software development term in this context. - - ❌ D. *Continuous validation* refers to automated checks but not necessarily about pushing new versions quickly.  🧱 **Continuous Delivery** means: "Every build is always deployable." Developers automate the release pipeline so apps can be pushed out frequently and reliably—sometimes even daily.  --- # QUESTION  Which of the following statements is true regarding IoT?   Why the others are wrong: - - ❌ B. This describes *resiliency* or *fault tolerance*, not IoT. - - ❌ C. That sounds like a *DMZ (Demilitarized Zone)*, not IoT. - - ❌ D. Finding patterns in data is the domain of *machine learning* or *AI*, not the Internet of Things.  🧱 IoT = Internet of Things = A surge of specialized devices (sensors, appliances, etc.) that send collected data to cloud or centralized services for processing.  --- # QUESTION  Which of these adds security functions that greatly reduce the Network Time Protocol vulnerabilities?   Why the others are wrong: - - ❌ A. IPS (Intrusion Prevention System) scans for threats but doesn’t protect NTP specifically. - - ❌ B. WAF (Web Application Firewall) protects web apps from HTTP(S) attacks—not NTP. - - ❌ D. ADC (Application Delivery Controller) balances load and improves performance, not NTP security.  🧱 NTS = Network Time Security: an extension to NTP that protects against spoofing and replay attacks with encryption and authentication.  --- # QUESTION  Your company can only afford to lose a maximum of the last 30 minutes of data in the event of a disaster. Which of the following sections of the corporate business continuity and disaster recovery plan addresses this issue?   Why the others are wrong: - - ❌ A. **RTO (Recovery Time Objective)** = how long it takes to restore service, not how much data you can lose. - - ❌ C. **RSO** is not a standard term in disaster recovery planning. - - ❌ D. **DBO** isn't a recognized term either (might be confused with database outage, but not relevant here).  🧱 **RPO = Recovery Point Objective** This defines how much data loss is acceptable (e.g., 30 minutes of missing data). It sets the *maximum tolerable time* between last backup and a disruption.  --- # QUESTION  Your disaster recovery facility is using a domain name system (DNS) to load-balance the primary and backup sites. You need to verify that the database in the disaster recovery (DR) facility is updated in real-time and remains current with the production replica in the primary data center at all times. What would you configure in the primary data center servers prior to enabling the DNS load balancing?   Why the others are wrong: - - ❌ B. **Mirroring** is typically local and doesn't guarantee real-time remote synchronization like synchronous replication does. - - ❌ C. **RAID 5** protects against disk failure, not remote replication or DR sync. - - ❌ D. **Asynchronous replication** introduces a delay — not acceptable when you need **zero data lag** between primary and DR.  🧱 **Synchronous replication** = every write must complete on both primary and DR before it's confirmed. Ensures **perfect data match**.  --- # QUESTION  What utilities are used to verify domain name-to-IP address mappings? *Each correct answer represents a complete solution. Choose all that apply.*   Why the others are wrong: - - ❌ A. `arp` shows MAC-to-IP address mappings from the local cache, not DNS resolution. - - ❌ C. `ipconfig` displays IP configuration for interfaces — no DNS querying or resolution. - - ❌ E. `traceroute` shows the path packets take but doesn’t resolve domain-to-IP info directly.   --- # QUESTION  Which access control model allows the owner of each controlled resource to decide who can access it and what permission they have?   Why the others are wrong: - - ❌ A. **MFA** (Multifactor Authentication) isn't an access control model — it's a method of verifying identity using multiple factors (e.g., password + phone). - - ❌ C. **RBAC** (Role-Based Access Control) gives access based on a user's role, not on individual ownership of the resource. - - ❌ D. **MAC** (Mandatory Access Control) uses security labels and policies defined by administrators — not the resource owner.   --- # QUESTION  Shara is searching for a cloud-based service that manages all underlying infrastructure, including updating the operating system. What service would you recommend to her?   Why the others are wrong: - - ❌ B. **IaaS** (Infrastructure as a Service) provides basic infrastructure: VMs, storage, and networking. OS updates? That’s on you. - - ❌ C. **CaaS** (Containers as a Service) focuses on container orchestration and runtime — not general infrastructure or OS-level updates. - - ❌ D. **SaaS** (Software as a Service) delivers complete applications (like Gmail, Salesforce). The user just consumes the app — not a platform to build on.   --- # QUESTION What is a visual representation of current cloud operations that consolidates data into an easy-to-read format called?  - - ❌ A. Metric - - ❌ B. Baseline - - ❌ C. Tag - - ✅ D. Dashboard  Why the others are wrong: - - ❌ **A. Metric**: A metric is a single measurement or data point, not a visual representation of multiple operations. - - ❌ **B. Baseline**: A baseline is a reference point for performance, not a display of current operations. - - ❌ **C. Tag**: A tag is a label for organizing resources, not a data visualization tool.  🧱 Think of it like your car’s dashboard: one glance shows speed, fuel, temp, alerts.  --- # QUESTION Your company hosts an application that is used by all the company's customers. The application has low usage during the first three weeks of each month and very high usage during the last week. Which of the following benefits of cloud computing supports cost management for this type of usage pattern?  - - ❌ A. Hyperthreading - - ✅ B. Elasticity - - ❌ C. Cloud bursting - - ❌ D. Overcommitting  Why the others are wrong: - - ❌ **A. Hyperthreading**: That’s a CPU optimization technique, not a cloud cost control strategy. - - ❌ **C. Cloud bursting**: Sounds close—but that’s when *on-prem* systems burst into the cloud. This question assumes the whole workload is already in the cloud. - - ❌ **D. Overcommitting**: That’s about allocating more virtual resources than physically available—not ideal for managing costs during usage spikes.   --- # QUESTION You have designed a web architecture that allows you to have an exact copy of your production fleet that can be brought online to replace your existing deployment for patching and maintenance. Which of these did you implement?  - - ❌ A. Backup target - - ❌ B. QA - - ❌ C. Rolling updates - - ✅ D. Blue-green  Why the others are wrong: - - ❌ **A. Backup target**: That’s for data protection, not live deployment swapping. - - ❌ **B. QA**: This is for testing—not production replacement or live cutover. - - ❌ **C. Rolling updates**: Gradual updates to *live* systems. Doesn't involve an *exact copy* standing by for full cutover.   --- # QUESTION  **You have been involved in a project to migrate a fleet of web servers from one cloud service provider to another. After performing address changes for all of your public-facing web servers, you validate connectivity by connecting from a bastion host located offshore to the new website. However, you find that the browser times out. Which record needs to be modified to allow the remote site to connect to the web server?**  - - ❌ A. NTP - - ❌ B. DHCP - - ✅ C. DNS - - ❌ D. FTP  ---

- ❌ A. RAID 1
- ❌ B. RAID 6
- ❌ C. RAID 5
- ✅ D. RAID 0
- ✅ A. Describes the explosion of small, purpose-built devices that typically collect data and send it to a central location for processing
- ❌ B. The ability of a system to quickly and automatically recover after a failure of one of its components
- ❌ C. A section of the network that hosts servers that need to be reachable via the Internet as well as internally
- ❌ D. The fundamental concern with finding patterns in data
- ❌ A. IPS
- ❌ B. WAF
- ✅ C. NTS
- ❌ D. ADC
- ❌ A. RTO
- ✅ B. RPO
- ❌ C. RSO
- ❌ D. DBO
- ✅ A. Synchronous replication
- ❌ B. Mirroring
- ❌ C. RAID 5
- ❌ D. Asynchronous replication
- ✅ B. nslookup
- ✅ D. dig
- ❌ A. arp
- ❌ C. ipconfig
- ❌ E. traceroute
- ✅ **nslookup** and **dig** are DNS diagnostic tools that query name servers to resolve domain names to IPs.
- ✅ B. DAC
- ❌ A. MFA
- ❌ C. RBAC
- ❌ D. MAC
- ✅ **DAC** (Discretionary Access Control) is the only model where the **owner of the data** decides who gets access and what they can do.
- ✅ A. PaaS
- ❌ B. IaaS
- ❌ C. CaaS
- ❌ D. SaaS
- ✅ **PaaS** (Platform as a Service) gives you the middle ground: the provider manages hardware, storage, network, and OS. You just deploy your code — no sysadmin headaches.
- ✅ **Dashboard** gives you the bird’s-eye view—real-time data, trends, and KPIs in one place. Perfect for cloud ops monitoring.
- ✅ **Elasticity** = scale up when demand spikes, scale down when it drops. Pay for what you use—nothing more.
- ✅ **Blue-green**: You maintain two identical production environments—blue (live) and green (standby). You patch/test in green, then swap DNS/load balancer to make it live. Zero downtime magic.

### Why the others are wrong:
- - ❌ **A. NTP (Network Time Protocol)**
- Handles time synchronization between devices. It has nothing to do with routing web traffic or resolving domain names.
- - ❌ **B. DHCP (Dynamic Host Configuration Protocol)**
- Assigns IP addresses to devices on a local network. The web server already has an IP, but the problem is that DNS hasn't been updated to point to it.
- - ❌ **D. FTP (File Transfer Protocol)**
- Used for transferring files, not for web access or domain resolution.
---
### - ✅ Why DNS is correct:
- DNS (Domain Name System) resolves domain names (like `example.com`) into IP addresses.
- After migrating the server to a new cloud, the **IP changed**, so the **DNS record (e.g. A record)** must be updated to reflect the new IP.
- If not updated, remote clients (like the bastion host) will still try to reach the **old IP**, causing timeouts.
🧱 Think of DNS as the **address book** of the internet — if it has the wrong address, nobody finds your house.
---
# QUESTION
Dimitry is troubleshooting a Linux SQL server that is experiencing poor read/write performance from the middleware servers. The vendor support team is requesting that he sends them packet traces to further investigate the issue. Which command would Dimitry use to collect the traces?
- - ❌ A) arp
- - ✅ B) tcpdump
- - ❌ C) dig
- - ❌ D) ipconfig
Why the others are wrong:
- - ❌ **A) arp** – Only shows the Address Resolution Protocol (ARP) table, which maps IP addresses to MAC addresses. It doesn’t capture packets.
- - ❌ **C) dig** – This is used for DNS lookups, not for monitoring or capturing traffic.
- - ❌ **D) ipconfig** – This is a Windows command for viewing network settings. On Linux, you’d use `ifconfig` or `ip`, but neither is for packet tracing.
🧱 **tcpdump** is a command-line packet analyzer—it captures and logs network traffic in real time, perfect for deep-dive troubleshooting.
---
# QUESTION
A critical application has sensitive data stored in cloud-based object storage in three Canadian public cloud regions. Because of regulatory requirements, a high-security user access solution is required that needs explicitly defined user groups that are allowed to modify specific objects. You are asked to provide a solution that meets these requirements. What would you suggest that the public cloud regions implement?
- - ❌ A) MFA
- - ❌ B) DAC
- - ✅ C) MAC
- - ❌ D) SSO
Why the others are wrong:
- - ❌ **A) MFA** – Multi-Factor Authentication enhances login security but doesn't enforce fine-grained access control over specific objects.
- - ❌ **B) DAC** – Discretionary Access Control gives data owners control over access, which doesn't meet strict regulatory requirements where access must be centrally governed.
- - ❌ **D) SSO** – Single Sign-On simplifies authentication but does not control *who* can access *what* resources at the object level.
🧱 **MAC (Mandatory Access Control)** is designed for high-security environments. Admins centrally define access policies based on security labels and user clearance levels. It’s ideal for regulatory and sensitive-data contexts.
---
# QUESTION
Jane is a Cloud+ architect working on a physical-to-virtual migration to the public cloud. She has matched VM performance levels to her established baselines. She knows that her organization may need to adjust hardware resources in the future. What cloud characteristics can Jane use to match cloud capacity with future growth?
Each correct answer represents a complete solution. Choose all that apply.
- - ✅ A) Elasticity
- - ✅ B) On-demand computing
- - ❌ C) Resource pooling
- - ❌ D) Pay-as-you-know
Why the others are wrong:
- - ❌ **C) Resource pooling** – This describes how cloud providers serve multiple customers from a shared pool of resources. It’s not directly about scaling *your* capacity for growth.
- - ❌ **D) Pay-as-you-know** – This isn’t a real cloud pricing model. The correct term is **pay-as-you-go**, but even then, it refers to billing—not capacity adjustment.
🧱 **Elasticity** lets Jane automatically scale resources up or down to meet demand.
🧱 **On-demand computing** means she can allocate or release compute power instantly as needed—perfect for unpredictable workloads.
---
# QUESTION
You work for a financial institution and want to protect sensitive data. What software would you implement to classify and protect your organization’s confidential and critical data?
- - ❌ A) CA
- - ✅ B) DLP
- - ❌ C) DDoS
- - ❌ D) SSL
Why the others are wrong:
- - ❌ **A) CA** – Certificate Authority issues digital certificates but doesn’t handle data classification or protection.
- - ❌ **C) DDoS** – That’s an *attack*, not a tool. This has nothing to do with classifying or protecting your internal data.
- - ❌ **D) SSL** – Encrypts data *in transit* but doesn’t classify or protect it internally or prevent leaks.
🧱 **DLP (Data Loss Prevention)** is the correct tool—it monitors, classifies, and protects data at rest, in motion, and in use. Perfect fit for a financial institution.
---
# QUESTION
Janine is in the process of implementing a hybrid cloud model that connects her company’s private cloud to a public cloud that supports on-demand web hosting. To ease the management of the remote resources for her network operations center, she wants to implement LDAP (Lightweight Directory Access Protocol) in the remote cloud services to interconnect with her locally hosted Active Directory servers. Which of these is Janine deploying?
- - ❌ A) RSA
- - ✅ B) SSO
- - ❌ C) Token-based 2FA
- - ❌ D) RBAC
Why the others are wrong:
- - ❌ **A) RSA** – Refers to an encryption algorithm or sometimes a token vendor—not the method for accessing multiple systems via shared authentication.
- - ❌ **C) Token-based 2FA** – Adds an extra step to authentication; doesn’t streamline access across systems.
- - ❌ **D) RBAC** – Role-Based Access Control governs *what* you can access, not *how* you sign in to multiple systems.
🧱 **SSO (Single Sign-On)** lets Janine use centralized identity authentication (like LDAP/AD) so users can log in once and access multiple systems—exactly what’s needed for hybrid cloud AD integration.
---
# QUESTION
In which access control model do administrators assign users to one or more roles representing job functions?
- - ✅ A. RBAC
- - ❌ B. MAC
- - ❌ C. MFA
- - ❌ D. DAC
Why the others are wrong:
- - ❌ B. MAC (Mandatory Access Control) is based on classifications and labels assigned by the system, not job roles. It’s rigid and used in secure environments.
- - ❌ C. MFA (Multi-Factor Authentication) is an authentication mechanism, not an access control model.
- - ❌ D. DAC (Discretionary Access Control) lets owners control access to their resources, not roles based on job functions.
🧱 **RBAC (Role-Based Access Control)** is the model that ties access to job duties. Think of it like giving access to the "Accounting role" instead of "Bob from Accounting."
---
# QUESTION
You are reviewing your private cloud’s infrastructure and are validating the resiliency of all systems. The data center has six racks of storage arrays that are configured to each lose one drive and remain operational. The servers hosting the hypervisors interconnect to these arrays and need to access block data that is lossless. What is the interconnect method that is commonly used in the given scenario?
- - ❌ A. Zoning
- - ❌ B. VMSF
- - ✅ C. SAN
- - ❌ D. RAID 5
Why the others are wrong:
- - ❌ A. Zoning is a **method used within SANs** to control access, not the interconnect method itself.
- - ❌ B. VMSF isn't a recognized standard in this context—likely a distractor or typo.
- - ❌ D. RAID 5 is a **redundancy technique**, not an interconnect method. It protects against drive failure, but doesn't provide the networked access SAN does.
🧱 **SAN (Storage Area Network)** is a dedicated high-speed network that provides block-level storage access to servers. It's the backbone of large-scale virtualized environments like this one.
---
# QUESTION
The statement "a service that delivers shared computing resources on-demand via the Internet" describes which of the following?
- - ❌ A. Virtualization
- - ✅ B. Cloud computing
- - ❌ C. Internet of Things
- - ❌ D. Resource pooling
Why the others are wrong:
- - ❌ A. Virtualization is the **tech behind the scenes**—it enables cloud computing but is not a service model itself.
- - ❌ C. Internet of Things (IoT) refers to **networked devices**, not computing resource delivery.
- - ❌ D. Resource pooling is a **feature** of cloud computing, not the full concept.
- ✅ Cloud computing is the correct answer because it **delivers shared, scalable IT resources via the internet**, just as the definition says.
---
