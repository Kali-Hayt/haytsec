# QUESTION 1
Which of the following are software representations of a cloud network?

✅ B. Templates  
❌ A. Software-defined storage  
❌ C. Tokens  
❌ D. Hotfix  

Why the others are wrong:
- ❌ Software-defined storage: This virtualizes storage resources, not the network.
- ❌ Tokens: Used for access/authentication, not for network representation.
- ❌ Hotfix: A patch for bugs or security issues, unrelated to network structures.

🧱 Templates define software representations like virtual routers, subnets, and firewall rules in cloud network blueprints.

---
# QUESTION 3  
Common cloud resources in your deployment that may saturate over time include which of the following?  
Each correct answer represents a complete solution. Choose all that apply.

✅ C. Storage  
✅ D. CPU  
❌ A. Power  
❌ B. Monitoring  

Why the others are wrong:
- ❌ **Power** – Cloud power supply is abstracted and managed by the provider, not a resource that saturates from a tenant’s perspective.  
- ❌ **Monitoring** – This is a control and observability function, not a resource that "saturates" like compute or disk.  

🧱 **CPU** and **Storage** are resource-bound assets that can hit usage limits (saturation), causing performance issues if not scaled.

---
# QUESTION 4  
**Software as a service (SaaS) orchestration systems are whose responsibility in the public cloud?**

- ❌ A. Customer  
- ✅ B. Provider  
- ❌ C. Vendor  
- ❌ D. None of these  

Why the others are wrong:  
- ❌ **Customer**: Only consumes the service; they don’t manage orchestration.  
- ❌ **Vendor**: Often overlaps with “provider,” but in this case CompTIA is specific—"provider" is the correct term.  
- ❌ **None of these**: Clearly false; someone *does* manage orchestration, and that’s the provider.  

---
# QUESTION 5  
**During a recent downtime window, the server team was applying patches to an application and the networking team was upgrading a router’s interface to 10 Gbps. When the network was down for the upgrade, the server team complained that they could not download the needed software patches. During a post-downtime status meeting, it was determined which process should be modified to prevent this from happening in the future?**

- ❌ A. Application programming interface calls  
- ❌ B. Orchestration  
- ❌ C. Automation  
- ✅ D. Change management  

Why the others are wrong:  
- ❌ **Application programming interface calls**: APIs are used for system interactions—not for coordinating human or team activities during downtime.  
- ❌ **Orchestration**: This refers to automating multiple tasks together but doesn’t cover the human coordination or scheduling across teams.  
- ❌ **Automation**: Again, this is about technical task execution—not managing process alignment across departments.  
- ✅ **Change management** is the right answer because it handles how changes are proposed, reviewed, scheduled, and communicated. This failure was about poor coordination—classic change management issue.

---
# QUESTION 6  
**Which of the following metrics is used to measure API performance?**

- ✅ A. Requests per second  
- ❌ B. Connections per second  
- ❌ C. Total lookups per second  
- ❌ D. IOPS  

Why the others are wrong:  
- ✅ **Requests per second** directly measures how often an API is called—core to understanding performance under load.  
- ❌ **Connections per second** relates more to networking or web servers than APIs specifically.  
- ❌ **Total lookups per second** is vague and more relevant to DNS or database operations.  
- ❌ **IOPS (Input/Output Operations Per Second)** measures disk or storage speed—not API behavior.

---
# QUESTION 7  
**Hank designed an application tier for his company’s new e-commerce site. He decided on using an IP subnet that uses a /28 IPv4 subnet. He is planning for a maximum of 14 servers. You are brought in as a cloud architect to validate your design. What other devices may be on this subnet other than the servers that would also require IP address assignments?**

- ❌ A. Default gateway  
- ❌ B. Domain name system  
- ❌ C. Network time protocol  
- ✅ D. All of these  

Why the others are wrong:  
- ❌ **Default gateway** is just one necessary device—but not the only one.  
- ❌ **DNS (Domain Name System)** servers may also need static or reserved IPs.  
- ❌ **NTP (Network Time Protocol)** servers are vital for time sync and also need IPs.  
- ✅ **All of these** is correct because **every listed service** typically requires an IP in the subnet, consuming part of the limited address space.

---
# QUESTION 8  
**Jim has added a new group of users to his Infrastructure as a Service (IaaS)–based NoSQL database. Which of the following license requirements does he need to investigate to ensure compliance?**

- ❌ A. Current connections  
- ❌ B. Named users  
- ❌ C. Total connections  
- ✅ D. All of these  
- ❌ E. Usage metrics  

Why the others are wrong:  
- ❌ **Current connections** show how many users are connected *now*, but not total usage trends.  
- ❌ **Named users** is one licensing model, but not the only concern.  
- ❌ **Total connections** reflects maximum simultaneous users, but doesn't cover usage limits or assigned users.  
- ❌ **Usage metrics** helps track activity, but it's only part of what needs to be monitored.  
- ✅ **All of these** is correct because licensing compliance often involves multiple dimensions: active users, total users, concurrent connections, and usage trends.

---
# QUESTION 9  
**Performance issues are measured by the load on a system. Which of the following should Jane be concerned about as she integrates her new marketing group into her platform as a service (PaaS) cloud fleet?**

- ❌ A. Licensing  
- ❌ B. Cores  
- ✅ C. Users  
- ❌ D. Application programming interfaces  

Why the others are wrong:  
- ❌ **Licensing** impacts compliance or cost, not immediate performance.  
- ❌ **Cores** matter, but performance issues start with excessive user load, which leads to scaling needs.  
- ✅ **Users** directly reflect system load in a PaaS environment — too many can cause bottlenecks.  
- ❌ **Application programming interfaces** can be monitored, but users are the root cause of load here.

---
# QUESTION 10  
**Dale has been monitoring storage volume utilization and is writing a change request to add capacity. He has decided to automate the volume allocation size. Which of the following features can he take advantage of?**

- ❌ A. Bandwidth  
- ❌ B. Tabletops  
- ✅ C. Elasticity  
- ❌ D. Templates  

Why the others are wrong:  
- ❌ **Bandwidth** relates to network throughput capacity, not storage sizing.  
- ❌ **Tabletops** are valid cybersecurity simulation exercises, but they don't automate or manage storage — they’re used for incident response training.  
- ✅ **Elasticity** enables dynamic resource scaling (up or down), which is what Dale needs.  
- ❌ **Templates** are used to deploy consistent environments, not to auto-adjust storage volumes.

---
# QUESTION 11  
**Cloud capacity can be measured by comparing current usage to which of the following?**

- ❌ A. Network time protocol  
- ❌ B. Automation  
- ❌ C. Orchestration  
- ✅ D. Baseline  

Why the others are wrong:  
- ❌ **Network time protocol (NTP)** is for synchronizing system clocks, not measuring capacity.  
- ❌ **Automation** is used to streamline tasks, not directly measure usage or capacity.  
- ❌ **Orchestration** coordinates automated tasks across systems — it’s about control, not metrics.  
- ✅ **Baseline** provides a reference point for normal or expected performance — perfect for measuring usage trends and capacity planning.
---
# QUESTION 12  
**What is the primary purpose of Amazon CloudWatch Dashboards?**

- ✅ A. To provide a unified interface for monitoring AWS resources  
- ❌ B. To manage user access and permissions  
- ❌ C. To automate infrastructure provisioning  
- ❌ D. To deploy applications across multiple AWS regions  

Why the others are wrong:  
- ❌ **B. User access and permissions** are managed with IAM (Identity and Access Management), not CloudWatch.  
- ❌ **C. Infrastructure provisioning** is handled by services like AWS CloudFormation, not CloudWatch.  
- ❌ **D. Deploying across regions** involves tools like CodeDeploy, not monitoring dashboards.  
- ✅ **CloudWatch Dashboards** let you visualize and track metrics across AWS services from a single pane of glass — think of it like mission control for your cloud.

---
# QUESTION 13  
**Large batch processing jobs are common for which type of application?**

- ✅ A. Database  
- ❌ B. IP address  
- ❌ C. Domain name system  
- ❌ D. Network time protocol  

Why the others are wrong:  
- ❌ **B. IP address** is a network identifier — not a type of application. No batch processing going on here.  
- ❌ **C. DNS** resolves domain names to IPs — fast, light, not batch-oriented.  
- ❌ **D. NTP** just syncs time. It's low-bandwidth and continuous, not suited to batch tasks.  
- ✅ **Databases**, especially data warehouses, often run big batch jobs — think nightly analytics, ETL pipelines, and report generation.

---
# QUESTION 14  
**Capacity boundaries can cause which of the following?**  
Each correct answer represents a complete solution. Choose all that apply.

✅ A. Request drops  
❌ B. API abends  
✅ C. Increased latency  
❌ D. Workflow loops  

Why the others are wrong:  
- ✅ **A. Request drops**: Systems hit max capacity → incoming requests get dropped.  
- ✅ **C. Increased latency**: Queues build, processes slow — classic symptom of saturation.  
- ❌ **B. API abends** are *application errors* caused by bugs or integration faults, not usually direct symptoms of resource limits.  
- ❌ **D. Workflow loops** are caused by flawed process logic, not capacity thresholds.


---
# QUESTION 15  
**Which of the following options determines the size of a group of servers in the same subnet?**

❌ A. Domain name system  
❌ B. Default gateway  
✅ C. CIDR block  
❌ D. Network time protocol  

Why the others are wrong:  
- ❌ **A. Domain name system** (DNS) maps hostnames to IPs — it doesn’t determine how many IPs exist in a subnet.  
- ❌ **B. Default gateway** is just the exit point from the subnet, not what defines its size.  
- ✅ **C. CIDR block** (Classless Inter-Domain Routing) defines the IP range and subnet size. Example: `/28` gives you 16 IPs total.  
- ❌ **D. Network time protocol** (NTP) keeps clocks in sync — has zero to do with IP allocation or subnetting.

---
# QUESTION 16  
**Connie has noticed an increase in the response time of the structured query language (SQL) database application... she verified a steady increase in read requests. What should she focus her troubleshooting on?**

❌ A. CPU  
✅ B. Storage  
❌ C. Networking  
❌ D. Memory  

Why the others are wrong:  
- ❌ **A. CPU** spikes typically correlate with processing logic or high write activity, not simple read queries.  
- ✅ **B. Storage** is the key bottleneck for read-heavy workloads. If read latency increases, your disk I/O is likely stressed.  
- ❌ **C. Networking** would affect all traffic, not just read performance from a local database deployment.  
- ❌ **D. Memory** could help with caching, but the root issue is how fast the disk responds to reads.

🧱 **Storage I/O = heart of read performance** in databases. Reads go straight to disk if not cached.

---
#quiz #cloud-plus #comptia 