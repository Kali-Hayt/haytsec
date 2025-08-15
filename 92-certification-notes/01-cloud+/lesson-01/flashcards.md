# Lesson 1 – Flashcard Q&A and Explanations  
**Course:** CompTIA Cloud+  
**Lesson:** 01 – Cloud Concepts and Models  

---

### ❓ Q1: What is the term when memory, CPU, and storage are virtualized by the hypervisor?  
✅ **A:** Resource Pooling  
💡 **Explanation:**  
Resource pooling allows multiple clients or tenants to share computing resources—such as memory, CPU, and storage—by abstracting the physical hardware using a hypervisor. These resources are **virtualized**, meaning they are represented as software-defined components that can be dynamically **allocated** and **reassigned** based on demand.

This makes cloud systems efficient, elastic, and scalable because they don’t tie a physical component to a single user. Instead, everything is pooled and delivered as needed.

🧠 **Key Terms:**  
- **Virtualized** = Not tied to physical hardware; software-defined  
- **Hypervisor** = The software that creates and manages virtual machines (VMs)  
- **Allocated** = Assigned from the shared pool to a VM or service

💻 **Example:**  
> You have a physical server with 64 GB RAM.  
> The hypervisor **virtualizes** the RAM into a **resource pool**.  
> You then create 4 virtual machines (VMs), each **allocated** 16 GB RAM.  
> To the VM, it feels like it owns 16 GB, but it's actually just a slice of the total shared pool.


---

### ❓ Q2: What technology enables on-demand computing?  
✅ **A:** Virtualization  
💡 **Explanation:**
**Virtualization** is the technology that powers on-demand computing. It allows physical servers, storage, and networking to be divided into virtual versions — so users can request and use these resources instantly without needing new physical hardware.

Without virtualization, you’d have to wait for someone to build and configure a new server. With virtualization, it happens in seconds.

---

🧠 **Key Takeaways:**

- Virtualization = tech that creates virtual versions of physical resources
    
- Enables cloud providers to offer **instant**, **scalable**, **pay-as-you-go** services
    
- Makes cloud fast, flexible, and powerful
    
---
🛠️ **Example:**

> You launch a VM on AWS → virtualization makes that possible  
> You’re not getting a new physical machine — you’re getting a **virtual one** provisioned on top of existing hardware
---

### ❓ Q3: Harry accesses a public cloud to add three additional web servers to a load-balanced fleet. What service type allows this?  
✅ **A:** On-demand  
💡 **Explanation:**  
**On-demand** is a cloud service model that allows users to provision resources instantly without human interaction from the provider. In this scenario, Harry uses a public cloud (like AWS or Azure) to quickly add three web servers to an existing load-balanced group. This is a classic use of on-demand computing: fast, scalable, and self-service.

🧠 **Key Terms:**

- **Public cloud** = Someone else’s infrastructure (AWS, Azure, etc.)
    
- **Web server** = A server that responds to web requests (like waiters serving data)
    
- **Load-balanced fleet** = A group of servers that share traffic evenly
    
- **On-demand** = Resources are created when needed and removed when done
    

🛠️ **Example:**

> Harry’s app is getting a lot of traffic.  
> He logs into AWS and spins up 3 web servers instantly.  
> These are added to a load balancer to spread the traffic.  
> He pays only for the time those servers are running.
---

### ❓ Q4: A new cloud provider offers court recording storage to all similar firms via a special app. What type of cloud model is this?  
✅ **A:** Community Cloud  
💡 **Explanation:**  
A **community cloud** is a cloud deployment type shared by multiple organizations that have similar requirements, goals, or regulatory needs. In this case, court recording storage is offered to firms that operate in the same industry — meaning they share a common interest (legal compliance, data retention, etc.). The provider also created a **specialized app**, which is another sign this cloud is tailored to a specific **community**.

🧠 **Key Terms:**

- **Community Cloud** = Shared among organizations with common interests (e.g., law firms, hospitals, government agencies)
    
- **Special App** = Custom solution built for the specific needs of that group
    
- **Not open to public**, and **not exclusive to one organization**
    

---

🛠️ **Quick Comparison of Cloud Types:**

|Cloud Type|Description|Who Uses It|
|---|---|---|
|**Public**|Open to anyone|General consumers, startups|
|**Private**|Owned by one org|Banks, defense contractors|
|**Community**|Shared by related orgs|Law firms, universities|
|**Hybrid**|Mix of 2+ cloud types|Enterprises needing flexibility|

---

### ❓ Q5: Tip of the Hat Coffee deploys a custom cloud just for their internal use. What cloud model is this?  
✅ **A:** Private Cloud  
💡 **Explanation:**  
Tip of the Hat Coffee built and deployed a **custom cloud environment** for **internal use only**. This means it is not open to the public, not shared with other companies, and not hosted on shared infrastructure like AWS — making it a textbook example of a **Private Cloud**.

Even though it's a customer-facing business, the question says the cloud is used internally — meaning **no public access**. It also hints at a **lack of scalability**, which is a common limitation of private clouds (you need to buy more hardware to scale).

🧠 **Key Points:**

- **Private Cloud** = owned/controlled by one company, fully isolated
    
- Not the same as using AWS with a VPC (that's public cloud with private feel)
    
- Public websites can still be hosted by private cloud — depends on **who owns the infrastructure**
    
🧠 **Extra insight:**

- **Private cloud** is often built **on-premises**
    
- It lacks the scalability of public cloud unless the company adds more hardware
    
- Tip of the Hat is likely using **IaaS** to build everything from the ground up

🔧 **Likely Model Used:**

- **IaaS**, since they’re building from scratch (choosing OS, installing apps)
---

### ❓ Q6: Henry creates a volume on the cloud SAN. What storage type is being used?  
✅ **A:** Block Storage  
💡 **Explanation:**  
Henry is using a **Storage Area Network (SAN)**, which provides **block-level storage**. This means the storage acts like a virtual hard drive — fast, flexible, and perfect for running applications, virtual machines, or databases.

🧠 **Key Concepts:**

- **Block Storage** = Raw chunks of storage, formatted and used like a physical disk
    
- **SAN (Storage Area Network)** = A dedicated high-speed network that connects storage devices to servers
    
- SAN handles **speed**, **reliability**, and **centralized access** to storage
    
- Only one type of storage is provided by SAN: **Block Storage**
    

📦 Henry creates a **volume** = a slice of that block storage  
The physical drives are managed in the background — Henry just gets a clean, fast drive ready to use.

*Henery uses Cloud SAN which he have to pay more to create more volumes.
### 🧠 Summary Line (Flashcard-Ready):

> **You create a volume and give it to the SAN.**  
> The **SAN takes over all responsibilities** — storage delivery, speed, availability, and reliability.

---

🛠️ What the SAN Handles **for that volume**:

- Makes sure it's **always accessible**
    
- Routes it over a **high-speed network**
    
- Keeps it **safe** with RAID or redundancy
    
- Lets the server use it like a **local hard drive**

---

### ❓ Q7: What technology enables widespread cloud deployment?  
✅ **A:** Automation  
💡 **Explanation:**  
**Automation** is the key technology that makes cloud deployment **fast, smooth, scalable, and secure**. It eliminates the need for manual setup by letting scripts, templates, and orchestration tools handle repetitive tasks — like creating servers, networks, firewalls, and backups — automatically.

🧠 **Why Automation Matters:**

- Speeds up deployment time (seconds vs hours)
    
- Reduces human error (security, config, naming mistakes)
    
- Enables large-scale rollouts (hundreds of servers at once)
    
- Supports consistency (same setup every time)
    
- Integrates with CI/CD, DevOps, and Infrastructure as Code (IaC)
    

---

### 🔧 Real Examples of Cloud Automation:

| Tool                   | What It Does                                        |
| ---------------------- | --------------------------------------------------- |
| **AWS CloudFormation** | Automates creation of cloud resources via templates |
| **Terraform**          | Cross-platform infrastructure as code               |
| **Ansible / Puppet**   | Automates configuration management                  |
| **CI/CD Pipelines**    | Auto-build, test, deploy code                       |

---

### ❓ Q8: True or False? The public cloud provider is ultimately responsible for your storage data.  
✅ **A:** False  
💡 **Explanation:**  
This is **False** because of the **Shared Responsibility Model**.  
In the public cloud, the **cloud provider** is responsible for securing the **cloud infrastructure**, but **you** are responsible for securing **your own data**.

That includes:

- Setting permissions
    
- Enabling encryption
    
- Managing backups
    
- Controlling who has access
    

🛡️ If your data is lost or exposed due to misconfiguration, it’s on **you**, not the provider.

---

### 🧠 Shared Responsibility Breakdown:

|Responsibility|Cloud Provider|You|
|---|---|---|
|Physical security|✅|❌|
|Network & hardware|✅|❌|
|Data encryption|❌|✅|
|Identity & access (IAM)|❌|✅|
|Backup & recovery|❌|✅|

---

### ❓ Q9: What backend systems allow for on-demand provisioning of cloud resources?  
✅ **A:** Automation  
💡 **Explanation:**  
The **back-end** powers everything users don't directly see. It processes requests, stores data, runs logic, and communicates with the front-end. In cloud environments, **automation** is used to manage, scale, and deploy the back-end quickly and reliably — without manual steps.

---

### 🧠 Key Back-End Components:

- **Servers** (EC2, containers)
    
- **Databases** (MySQL, MongoDB)
    
- **Code/logic** (Node.js, Python, Java)
    
- **APIs** (REST, GraphQL)
    
- **Storage** (S3, SAN volumes)
    
- **Security** (IAM, firewalls, encryption)
    

---

### ⚙️ How Automation Supports the Back-End:

|Task|Automated With|
|---|---|
|Deploy code|CI/CD (e.g., GitHub Actions, Jenkins)|
|Launch servers|Scripts, Terraform, CloudFormation|
|Scale resources|Auto-scaling groups|
|Monitor performance|CloudWatch, Prometheus, custom tools|

---

### ❓ Q10: The establishment of average usage over time is used for what type of cloud reporting?  
✅ **A:** Baseline Reporting  
### 💡 Explanation:

A **baseline** is like the **"default speed"** your car runs at on a normal day.

> In cloud or IT terms, it’s the **average** or **standard** level of performance (CPU, memory, traffic, etc.)  
> — used to **measure changes**, **detect issues**, or **optimize resources.**

---

### 🧠 Why Baselines Matter:

- 📊 If something suddenly **uses more CPU than the baseline**, it might be overloaded or under attack.
    
- 🛡️ Helps with **monitoring**, **alerting**, and **security detection**
    
- 🔧 Used in **capacity planning**, scaling, and budgeting
    

---

### ⚙️ Real-World Example:

| System          | Normal Baseline | Alert If…                                  |
| --------------- | --------------- | ------------------------------------------ |
| CPU Usage       | 25% average     | Spikes to 80%? 📣 alert!                   |
| Disk I/O        | 100 MB/s        | Drops to 5 MB/s? Could mean failure or lag |
| Network Traffic | 10 GB/day       | Jumps to 100 GB/day? Could be data leak    |

---
### ❓ Q11: To collect metrics, what do you set up your management application to monitor?  
✅ **A:** Objects  
### 💡 Explanation:

- **Metrics** = performance data (CPU usage, memory, disk, latency, etc.)
    
- **Objects** = the cloud resources being watched (VMs, disks, apps, databases)
    

Cloud platforms **collect metrics from objects** so you can:

- Monitor performance
    
- Trigger alerts (when a value spikes or drops)
    
- Auto-scale resources
    
- Diagnose and fix problems
    

---

### 💻 Real-Life Comparison: **Task Manager on Kali**

|Task Manager Feature|Cloud Equivalent|
|---|---|
|CPU/RAM stats|Metrics|
|Running processes|Objects|
|Ending a task|Management action|
|Watching spikes|Real-time alerts|

---

### ❓ Q12: A video hosting company’s servers slow down after releasing a popular movie. What resource pool should be increased?  
✅ **A:** Network I/O  
### 💡 Explanation:

When demand increases (like a viral video release), the service must handle more users, data, and bandwidth. Instead of buying physical servers, cloud providers **automatically scale resources** up or down:

- Add more **virtual servers**
    
- Distribute load with **load balancers**
    
- Boost **bandwidth or storage speed**
    
- Maintain performance **without delay**
    

---

### 🧠 Traditional vs. Cloud:

|Traditional IT|Cloud-Based|
|---|---|
|Buy new servers|Auto-scale virtual machines|
|Install hardware|Elastic infrastructure|
|High upfront cost|Pay-as-you-go|
|Slow response|Instant scaling|

✅ **I/O** = **Input/Output**  
It’s how data **moves in and out** of a system, resource, or application.

---

### ❓ Q13: An app server suffers poor performance due to excessive pagefile activity. What resource pool needs adjusting?  
✅ **A:** Memory  (RAM) -Not Storage
### 💡 Explanation:

- When a system runs out of **RAM**, it uses the **page file** (disk space) to fake memory.
    
- This is called **paging** or **swapping**, and it's way slower than using real RAM.
    
- That’s why performance tanks.
    

---

### ⚠️ Common Mistake:

> This isn’t a **storage space** problem —  
> it’s a **speed + memory** problem.

---

### 🧠 Correct Cloud Fix:

| Problem                  | Fix                                          |
| ------------------------ | -------------------------------------------- |
| App paging to disk       | Add more **RAM**                             |
| Sluggish response        | Upgrade to a VM with higher **memory specs** |
| Cloud page file overload | Resize or auto-scale memory resources        |

### TL;DR:

> Page file overload = system begging for RAM.  
> Don’t give it more disk — give it more memory.
---

### ❓ Q14: During a database server migration, how do you prevent write latency issues?  
✅ **A:** Storage  
### 💡 Explanation:

Write latency happens when data takes too long to be saved to disk.  
During a database migration, there's a high volume of **write operations**, and if the storage is slow (like using an HDD), it becomes a **bottleneck**, slowing everything down.

To prevent that, you need **fast, low-latency storage**, such as:

- **SSD (Solid State Drive)** – much faster than traditional disks
    
- **Provisioned IOPS volumes** – in cloud platforms like AWS, this guarantees high-performance writes
    
- **Optimized cloud storage classes** – built for high input/output workloads
    

You don’t fix write latency by adding more storage **space** — you fix it by upgrading to **faster, high-performance storage**.

---

### 🧠 TL;DR:

> Storage controls **how fast** your data is written —  
> and during migration, you need **speed**, not just capacity.

---
