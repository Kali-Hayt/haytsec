### 🔹 Flashcard 1 of 17

#### ❓ **Question:**

What is a cloud service that provides a virtual server platform but not the operating system or applications?

#### ✅ **Answer:**

IaaS

#### 🧠 **Explanation:**

Infrastructure as a Service (IaaS) provides basic cloud infrastructure—like virtual machines, storage, and networking. **You install and manage the OS and applications yourself.** It's ideal for flexible, scalable environments where you control most of the stack except the hardware layer, which the provider manages.

---
### 🔹 Flashcard 2 of 17

#### ❓ **Question:**

What is a virtual network device that connects virtual machines together at layer 2?

#### ✅ **Answer:**

Virtual switch

#### 🧠 **Explanation:**

A **virtual switch** (vSwitch) operates at **OSI Layer 2**, just like a physical switch. It enables communication between virtual machines (VMs) on the same host or across hosts in a virtualized environment. Think of it as a software version of a regular Ethernet switch — it handles MAC addresses, forwarding frames, and sometimes VLAN tagging — but all inside your hypervisor.

---
### 🔹 Flashcard 3 of 17

#### ❓ **Question:**

BigCo has asked you as a Cloud+ consultant to connect its private cloud to a community cloud to access a human resource application. What type of cloud delivery model would you implement?

#### ✅ **Answer:**

Hybrid

#### 🧠 **Explanation:**

A **Hybrid cloud** combines **two or more cloud types** (private, public, or community) that remain unique entities but are **bound together** by standardized or proprietary technology. In this case, connecting a **private cloud** to a **community cloud** forms a **hybrid environment**, allowing data and applications to move between the two. It offers flexibility and scalability while keeping sensitive data under tighter control.

---
### 🔹 Flashcard 4 of 17

#### ❓ **Question:**

Hosted email falls under this cloud service delivery model.

#### ✅ **Answer:**

SaaS

#### 🧠 **Explanation:**

**SaaS (Software as a Service)** provides **fully managed applications** over the internet. Hosted email like **Gmail** or **Microsoft 365** is a classic example — the provider handles the infrastructure, operating system, and application itself. Users just log in and use the service without worrying about maintenance or deployment.

---
### 🔹 Flashcard 5 of 17

#### ❓ **Question:**

For redundancy, public clouds are segregated by these geographic divisions.

#### ✅ **Answer:**

Regions

#### 🧠 **Explanation:**

**Regions** are large, geographically distinct areas used by cloud providers (like AWS, Azure, GCP) to separate data centers. This separation enhances **redundancy**, **availability**, and **fault tolerance** by isolating resources. If one region fails (say, `us-west-1`), others (like `us-east-1`) can continue operations — minimizing disruption.

---
### 🔹 Flashcard 6 of 17

#### ❓ **Question:**

What is a type of replication that is eventually consistent?

#### ✅ **Answer:**

Asynchronous

#### 🧠 **Explanation:**

**Asynchronous replication** means that data is copied from one system to another with a delay. It's **eventually consistent**, meaning the systems will match **over time**, but not instantly. This is useful when low latency is needed and some delay in data consistency is acceptable — such as across **geographically distant data centers**. It's faster than synchronous replication but may risk **temporary mismatches**.

---
### 🔹 Flashcard 7 of 17

#### ❓ **Question:**

Connie is part of the cloud migration team at an insurance company. She is investigating a Windows server in the data center that runs natively on a high-end server platform. She wants to move it to an IaaS provider. What type of migration does she need to perform?

#### ✅ **Answer:**

P2V

#### 🧠 **Explanation:**

**P2V** stands for **Physical to Virtual** migration. Connie is moving a **physical server** (on-premise, native hardware) into a **virtualized environment** hosted by a cloud provider (like AWS EC2, Azure VM — part of IaaS). This process involves converting the physical system’s disk into a virtual machine image, so it can run in the cloud’s virtual infrastructure.

---

### 🔹 Flashcard 8 of 17

#### ❓ **Question:**

You have been brought in to assist a company’s project to move sensitive storage data to a public cloud. The company requires that the data be indecipherable if accessed by an unauthorized party. What general term is used to describe this operation?

#### ✅ **Answer:**

Obfuscation

#### 🧠 **Explanation:**

**Obfuscation** is a broad term for making data unintelligible or confusing to unauthorized viewers. In cloud computing, this can involve **encryption**, **tokenization**, or **data masking**. While encryption is more specific, obfuscation covers the general concept of hiding the original meaning or format of data for security purposes.

---

### 🔹 Flashcard 9 of 17

#### ❓ **Question:**

What is the storage arrangement that divides different types of storage requirements into different offerings?

#### ✅ **Answer:**

Tiering

#### 🧠 **Explanation:**

**Tiering** is a storage strategy that categorizes data based on performance needs, access frequency, or cost efficiency.

- **Hot data** (frequently accessed) might live on high-speed SSDs.
    
- **Cold data** (rarely accessed) gets moved to cheaper, slower storage like magnetic drives or even cloud archive services.  
    This helps balance cost and performance across workloads.
---
### 🔹 Flashcard 10 of 17

#### ❓ **Question:**

Jill is the storage administrator for her company’s private cloud. She is deploying a new storage array that groups multiple disks into one logical drive. What storage technology is this?

#### ✅ **Answer:**

RAID

#### 🧠 **Explanation:**

**RAID** (Redundant Array of Independent Disks) combines multiple physical drives into a single logical unit to improve performance, redundancy, or both.

- **RAID 0** = Speed
    
- **RAID 1** = Mirroring (redundancy)
    
- **RAID 5/6/10** = Balance of performance + fault tolerance  
    Jill is most likely using a RAID level that fits her organization’s needs for uptime and storage efficiency.
    

---
### 🔹 Flashcard 11 of 17

#### ❓ **Question:**

What is a disk array technology that can withstand the simultaneous failure of two SSD drives?

#### ✅ **Answer:**

RAID 6

#### 🧠 **Explanation:**

**RAID 6** uses **dual parity**, meaning it can survive **two simultaneous drive failures** without losing data.  
This makes it more fault-tolerant than RAID 5 (which only tolerates one failure), but it also has a higher overhead in terms of write performance.

Use RAID 6 when:

- You have critical data
    
- You need high availability
    
- You can afford extra parity disk space

---

### 🔹 Flashcard 12 of 17

#### ❓ **Question:**

What is a service delivery model where the cloud provider takes responsibility for all operating system maintenance but the customer is responsible for the applications?

#### ✅ **Answer:**

PaaS (Platform as a Service)

#### 🧠 **Explanation:**

In **PaaS**, the cloud provider handles:

- **Infrastructure**
    
- **Operating system**
    
- **Runtime environment**
    

You, the customer, only manage:

- **Your apps**
    
- **Your data**
    

Think of it like a kitchen where the stove, fridge, and utensils are provided—you just cook the meal. Great for developers who want to focus on code, not servers.

---
### 🔹 Flashcard 13 of 17

#### ❓ **Question:**

Lynn is documenting the maintenance responsibilities between her company and its public cloud provider. She notices that the cloud provider takes responsibility for all operating system updates and patches, and she needs to assume responsibility for the applications and services running on the operating system. Under what type of service delivery model is she operating?

#### ✅ **Answer:**

PaaS (Platform as a Service)

#### 🧠 **Explanation:**

This is classic **PaaS**:

- The **provider** handles the OS, updates, security patches.
    
- **Lynn’s team** manages their apps and services.
    

PaaS is like renting a fully furnished apartment: the landlord handles repairs and utilities—you just live your life and decorate the space (aka, run your app).

---
### 🔹 Flashcard 14 of 17

#### ❓ **Question:**

What is a separate network operating in your private cloud that is accessed both internally and externally?

#### ✅ **Answer:**

**DMZ (Demilitarized Zone)**

#### 🧠 **Explanation:**

A **DMZ** acts like a digital buffer zone:

- It’s isolated from your internal LAN.
    
- External users (like customers or remote users) can access services like web servers.
    
- But direct access to the internal network is restricted.
    

It’s like the lobby of a secure building: the public can enter the lobby, but they can’t go upstairs without a keycard.

---
### 🔹 Flashcard 15 of 17

#### ❓ **Question:**

Erving is asking you about cloud virtualization techniques and wants to know what a software representation of his three-tier public cloud deployment is called. What is he referring to?

#### ✅ **Answer:**

**Templates**

#### 🧠 **Explanation:**

In cloud environments:

- **Templates** are predefined software blueprints.
    
- They include operating systems, pre-installed applications, and configurations.
    
- Great for **standardizing deployments** like multi-tier architectures (web, app, database).
    

Think of it like a ready-to-go meal kit for cloud servers—just deploy and cook.

---
### 🔹 Flashcard 16 of 17

#### ❓ **Question:**

What cloud service provider document outlines assured system uptime and network performance guarantees?

#### ✅ **Answer:**

**Service level agreement**

#### 🧠 **Explanation:**

- A **Service Level Agreement (SLA)** is a formal contract between a cloud provider and the customer.
    
- It defines expected **uptime**, **latency**, **support response times**, and **penalties** if service isn't met.
    
- For example: _“99.9% uptime guaranteed per month”_ or _“support response within 1 hour.”_
    

If it's not in the SLA, it’s not guaranteed — always read the fine print.

---
### 🔹 Flashcard 17 of 17

#### ❓ **Question:**

Jonathan is asking you about a networking service to which he needs to make updates. This service is used to translate human-readable names to network addresses understood by computers. What service is this?

#### ✅ **Answer:**

**DNS** (Domain Name System)

#### 🧠 **Explanation:**

- **DNS** converts easy-to-remember domain names like `example.com` into IP addresses like `93.184.216.34`.
    
- Without DNS, we’d all be typing raw IPs just to check email or shop online. No thanks.
    
- Updating DNS records can involve A, CNAME, MX, TXT records, etc.
    
- It’s like the **phonebook of the internet** — but way cooler and a lot faster.