# QUESTION 1

To collect metrics, you set up your management application to measure what?

- ❌ A. Database  
- ❌ B. Server  
- ❌ C. Hypervisor  
- ✅ D. Objects  

Why the others are wrong:

- ❌ **A. Database** – You monitor databases with specific tools for SQL queries, performance tuning, etc., *not* with a general management app for infrastructure metrics.

- ❌ **B. Server** – It seems logical, but in **cloud environments**, the focus shifts away from physical servers. Management apps often monitor **logical resources** (like VMs, containers, and *objects*) instead.

- ❌ **C. Hypervisor** – A hypervisor *hosts* virtual environments, but metrics aren't typically collected at that layer unless you're dealing directly with VM infrastructure.

---

✅ **D. Objects** – In cloud management, "objects" often refer to **monitored components** like storage objects, network interfaces, or logical resource units. These are what cloud-native monitoring tools (like AWS CloudWatch or Azure Monitor) often track.

---
# QUESTION 2

Object tracking should be aligned with which of the following?

- ✅ A. Service level agreement  
- ❌ B. Baselines  
- ❌ C. Compute tuning  
- ❌ D. Horizontal Scaling  

Why the others are wrong:

- ❌ **B. Baselines** – Baselines help define “normal” system behavior, but they’re **internal performance comparisons**, not tied to **external service promises** like SLAs.

- ❌ **C. Compute tuning** – That’s optimization-focused (e.g., CPU/memory adjustments), not about *monitoring whether service obligations are met*.

- ❌ **D. Horizontal Scaling** – This is a **capacity strategy**, not a measurement or tracking alignment.

---

✅ **A. Service level agreement** – SLAs define the expected **performance, availability, and responsiveness** of services. Object tracking must align with SLAs to **prove compliance and detect violations**.

---
# QUESTION 3

Which of the following is **not** a statistic that you would typically find in a server performance baseline?

- ✅ A. OS update history  
- ❌ B. Disk transfer rate  
- ❌ C. CPU utilization  
- ❌ D. Memory utilization  

Why the others are wrong:

- ❌ **B. Disk transfer rate** – This measures how fast data moves to/from the disk. It’s a **key performance metric** used in baselining I/O.

- ❌ **C. CPU utilization** – A core metric in any performance baseline. It helps determine processing load patterns.

- ❌ **D. Memory utilization** – Essential to spot memory leaks, overuse, or underuse over time.

---

✅ **A. OS update history** – This is **config/audit history**, not a performance stat. It belongs in a patch management report, not a performance baseline.

---
# QUESTION 4

Object tracking can be helpful in identifying which of the following?  
Each correct answer represents a complete solution. **Choose all that apply.**

- ✅ A. Trends  
- ❌ B. Jitter  
- ❌ C. Latency  
- ✅ D. Peak usage  
- ✅ E. Anomalies  
- ❌ F. Capacity  

Why the others are wrong:

- ❌ **B. Jitter** – Jitter refers to inconsistent packet timing on a network. It’s not measured through object tracking — more relevant to real-time communications (VoIP, video).

- ❌ **C. Latency** – Latency is a **delay in communication or processing**, typically monitored by tools focused on **network, application, or API response**, not objects.

- ❌ **F. Capacity** – Capacity planning involves long-term forecasting based on resource limits. It’s usually handled by **capacity management tools**, not raw object tracking.

---

✅ **A. Trends** – Object tracking reveals performance and usage patterns over time. This is core to detecting long-term behavioral trends.

✅ **D. Peak usage** – Object tracking can identify when resources hit maximum usage levels, which is key for scaling and alerting.

✅ **E. Anomalies** – One of the top reasons to track objects: to spot strange behaviors or outliers that indicate problems.

---
# QUESTION 5

Rebecca is writing a change management plan to increase the processing abilities of one of her middleware servers.  
What components can she upgrade to increase server performance?  
**(Choose all that apply.)**

- ❌ A. Latency  
- ✅ B. CPU  
- ✅ C. Network I/O  
- ✅ D. RAM  

Why the others are wrong:

- ❌ **A. Latency** – This isn’t a hardware component. Latency is an outcome (delay in data transfer or processing), **not something you can physically upgrade**. You reduce latency by improving other subsystems — like faster CPUs, better I/O, or caching.

---

✅ **B. CPU** – Central Processing Unit. Upgrading to more cores or faster clock speeds directly improves processing power.

✅ **C. Network I/O** – Upgrading network interface cards (NICs), increasing bandwidth, or reducing bottlenecks improves server responsiveness and throughput.

✅ **D. RAM** – More memory means faster data access and better multitasking. Crucial for middleware apps that cache, queue, or run multiple services.

---
# QUESTION 6

Which of the following outlines is of cloud provider SLAs?

- ❌ A. Device configuration  
- ❌ B. DNS configurations  
- ✅ C. Uptime  
- ❌ D. Autocache  

Why the others are wrong:

- ❌ **A. Device configuration** – That’s an **internal infrastructure detail**. SLAs don’t promise how providers configure devices — they promise results (like availability, support time).

- ❌ **B. DNS configurations** – DNS is a service you may configure, but it's not something **guaranteed by SLA** unless explicitly offered (e.g., DNS availability could be part of it, not config specifics).

- ❌ **D. Autocache** – This is a **feature** or service enhancement. Not part of an SLA unless you pay for guaranteed performance of caching layers.

---

✅ **C. Uptime** – This is textbook SLA material. SLAs define availability like “99.9% uptime,” and include consequences (refunds, penalties) if the provider fails to meet it.

---
# QUESTION 7

Autoscaling can be configured to which of the following?  
**(Choose all that apply.)**

- ❌ A. Perform patch management  
- ✅ B. Add capacity  
- ✅ C. Maintain a minimum number of servers  
- ✅ D. Remove capacity  
- ❌ E. Generate metrics reports  

Why the others are wrong:

- ❌ **A. Perform patch management** – That’s handled by configuration management tools (e.g., Ansible, SCCM), not autoscaling policies.

- ❌ **E. Generate metrics reports** – Autoscaling *uses* metrics to make decisions, but **report generation** is handled by **monitoring tools**, not the autoscaler itself.

---

✅ **B. Add capacity** – Autoscaling **increases resources** (like VMs, containers) during high demand automatically.

✅ **C. Maintain a minimum number of servers** – You can define a **floor** (e.g., “Always keep at least 2 servers running”) in an autoscaling group.

✅ **D. Remove capacity** – When demand drops, autoscaling can **de-provision instances** to save cost and optimize usage.

---
# QUESTION 8

What is a visual representation of your current cloud operations?

- ❌ A. Management console  
- ❌ B. Operational matrix  
- ❌ C. Health check  
- ✅ D. Dashboard  

Why the others are wrong:

- ❌ **A. Management console** – This is the **interface** to configure and control resources (like AWS Console), but it's not strictly a *visual representation* of operations.

- ❌ **B. Operational matrix** – Not a standard cloud term. Sounds fancy, but doesn’t refer to a specific, visual, real-time view.

- ❌ **C. Health check** – This checks the **status of a component or service**, not an overview of your operations as a whole.

---

✅ **D. Dashboard** – A dashboard gives you **real-time visual data**: CPU, memory, I/O, alerts, usage graphs. It’s the **go-to tool** for cloud ops visibility.

---
# QUESTION 9

In which of the following formats can cloud-based reports be generated?  
**Choose all that apply.**

- ✅ A. PDF  
- ❌ B. Python  
- ❌ C. JSON  
- ✅ D. Excel  

Why the others are wrong:

- ❌ **B. Python** – It's a programming language, not a report format. You might use Python to **create** or parse reports, but it’s not a *report format*.

- ❌ **C. JSON** – While often used for data interchange in APIs and logging, **CompTIA is referring to human-readable reporting formats**, not structured raw data dumps.

---

✅ **A. PDF** – Standard for professional and printable reporting. Common in compliance, billing, and management reports.

✅ **D. Excel** – Reports can be exported as `.xls` or `.csv` for financials, resource tracking, or usage analysis. Cloud platforms like AWS and Azure support this format directly.

---
# QUESTION 10

Jeff has been monitoring resource usage increases in his web server farm.  
Based on trending data, he knows he'll need to **increase CPU capacity** as usage spikes.  
He wants to automate this through orchestration software in his private cloud.  
**What can he implement to automate this?**

- ❌ A. Bandwidth  
- ✅ B. Autoscaling  
- ❌ C. Workflow applications  
- ❌ D. Templates  

Why the others are wrong:

- ❌ **A. Bandwidth** – That’s a **network resource**, not related to CPU provisioning or scaling compute workloads.

- ❌ **C. Workflow applications** – These are broader automation tools. They might help manage tasks, but they don’t **scale resources** dynamically based on CPU usage.

- ❌ **D. Templates** – Templates define **resource configurations** (like VM sizes or OS settings), but they’re static. They don’t react to *usage conditions*.

---

✅ **B. Autoscaling** – Autoscaling is designed to **automatically adjust compute resources** like CPU, RAM, or entire VM instances **based on demand**.  
In Jeff's case, autoscaling policies tied to CPU usage metrics would trigger orchestration software to add cores or spin up new instances as needed.

---
# QUESTION 11

Which of the following options contain incident reports?  
**Choose all that apply.**

- ✅ A. Support engagements  
- ✅ B. Trouble tickets  
- ❌ C. Latency  
- ❌ D. Scaling  

Why the others are wrong:

- ❌ **C. Latency** – This is a **performance metric**, not a system of record. High latency may trigger an incident, but the metric itself doesn’t **contain** a report.

- ❌ **D. Scaling** – Scaling is a **response action** (like autoscaling). It may happen during an incident, but it doesn’t house the actual **incident documentation**.

---

✅ **A. Support engagements** – These include **case history**, notes, logs, and actions taken — all common elements of an incident report.

✅ **B. Trouble tickets** – Core to ITSM (IT service management). Trouble tickets are **the official record** of incidents, including timestamps, escalation history, and resolution notes.

---
# QUESTION 12

When monitoring performance metrics on one of your servers, you notice that the server is utilizing **100% of the network bandwidth** available to it.  
What modification could you make to the server that will **most likely address the problem**?

- ❌ A. Install a second processor  
- ❌ B. Update the network adapter’s firmware  
- ✅ C. Install a second network adapter  
- ❌ D. Add memory to the system  

Why the others are wrong:

- ❌ **A. Install a second processor** – This helps with **compute tasks**, not network throughput. CPU isn't the bottleneck here.

- ❌ **B. Update the network adapter’s firmware** – May fix bugs, but won't increase the **physical bandwidth limit**. Firmware doesn’t add new lanes to the highway.

- ❌ **D. Add memory to the system** – RAM helps with **multitasking and caching**, not network traffic handling.

---

✅ **C. Install a second network adapter** – Also known as **NIC teaming or bonding**, this adds **more available bandwidth** by spreading traffic across multiple interfaces. It's the go-to fix when you're saturating a single network interface.

---
# QUESTION 13

What are recommended procedures to take when preparing an outage response plan?  
**Choose all that apply.**

- ✅ A. Diagrams  
- ✅ B. Documentation  
- ❌ C. Service level agreement  
- ✅ D. Configuration backups  

Why the others are wrong:

- ❌ **C. Service level agreement** – An SLA is a **contract** that outlines expectations for uptime, support, etc., but it’s not a *procedure* you perform during outage planning. It’s a policy reference — not an action item.

---

✅ **A. Diagrams** – Clear infrastructure diagrams help teams **understand topology**, dependencies, and potential failure points — crucial when tracing outages.

✅ **B. Documentation** – Always needed. This includes **response steps, escalation contacts, and recovery playbooks**.

✅ **D. Configuration backups** – Absolutely. Having backups of your firewall rules, server configs, and cloud templates allows for **rapid recovery or rollback** after an outage.

---
# QUESTION 14

When configuring a machine image, which of the following compute resources do you define?  
**Choose all that apply.**

- ✅ A. Clock speed  
- ❌ B. Tabletop  
- ❌ C. Call tree  
- ✅ D. Cores  

Why the others are wrong:

- ❌ **B. Tabletop** – This refers to **tabletop exercises** (simulation training for outages or incidents). Has nothing to do with configuring VMs.

- ❌ **C. Call tree** – A **communications flowchart** for incident response. Not part of machine image setup.

---

✅ **A. Clock speed** – Defines how fast the CPU processes instructions (GHz). Some cloud platforms let you select or prioritize **performance tiers** tied to CPU speed.

✅ **D. Cores** – Specifies how many CPU threads the machine gets. More cores = more processing power for parallel tasks or heavier workloads.

---
# QUESTION 15

What does triage in IT and cybersecurity primarily focus on?

- ✅ A. Prioritizing and classifying incidents based on severity and impact  
- ❌ B. Preventing all cyber threats before they occur  
- ❌ C. Replacing human analysts with AI completely  
- ❌ D. Ensuring that all alerts are treated equally  

Why the others are wrong:

- ❌ **B. Preventing all cyber threats before they occur** – That’s ideal but **not realistic**, and **not the role of triage**. Prevention is a broader goal of security architecture.

- ❌ **C. Replacing human analysts with AI completely** – Nope. AI supports triage but **can’t fully replace** human judgment in context-heavy security decisions (yet).

- ❌ **D. Ensuring that all alerts are treated equally** – That's exactly what **triage prevents**. Triage exists **because** all alerts aren’t equal — you must rank them by urgency.

---

✅ **A. Prioritizing and classifying incidents based on severity and impact** – This is the textbook definition of **triage**. In both medicine and cybersecurity, triage determines **what to respond to first** based on potential damage or urgency.

---
# QUESTION 16

How can relational database read performance be improved?  
**Choose all that apply.**

- ❌ A. Auto-sizing  
- ❌ B. Scoping horizontally  
- ✅ C. Adding a read replica  
- ✅ D. Scaling vertically  

Why the others are wrong:

- ❌ **A. Auto-sizing** – This is a **cloud infrastructure feature** for autoscaling resources (like VM memory or disk), not a targeted method for improving DB read performance.

- ❌ **B. Scoping horizontally** – While *horizontal scaling* (e.g., sharding) is used in large-scale databases, **CompTIA Cloud+ focuses more on standard replication and vertical scaling techniques**.

---

✅ **C. Adding a read replica** – Read replicas allow traffic to be distributed between multiple servers, relieving pressure from the primary DB and improving **read performance**.

✅ **D. Scaling vertically** – Increasing CPU, RAM, or IOPS on the database server boosts performance — especially for read-heavy workloads.

---

# QUESTION 17

Reports are often provided to which interested parties?  
**Choose all that apply.**

- ❌ A. Cloud provider operations  
- ✅ B. Accounting  
- ❌ C. Customers  
- ✅ D. Marketing  
- ✅ E. Management  

Why the others are wrong:

- ❌ **A. Cloud provider operations** – The **provider** generates the reports — they don't typically receive them as a stakeholder in the customer's internal reporting structure.

- ❌ **C. Customers** – Unless you’re an MSP (Managed Service Provider), internal operational reports are usually **not shared directly with external customers**.

---

✅ **B. Accounting** – Needs reports for **cost analysis, billing, and budgeting**.

✅ **D. Marketing** – May use system usage trends and analytics for **strategy and planning**.

✅ **E. Management** – Requires reports for **performance tracking, decision-making, and compliance oversight**.

---
# QUESTION 18

Carl has noticed a slowdown in the response times of his Structured Query Language (SQL) database and has been tasked with investigating the root cause of the delays. He has decided to configure his monitoring application to gather additional data on what may be the cause of the delays. What are some of the objects on which you would recommend that he collect data?

**Each correct answer represents a complete solution. Choose all that apply.**

- ✅ A. Read replica I/O  
- ❌ B. Jitter  
- ✅ C. CPU  
- ❌ D. Latency  

Why the others are wrong:

- ❌ **B. Jitter** – This is only relevant in real-time network traffic, not SQL database troubleshooting. It's a red herring.
- ❌ **D. Latency** – While latency is a **symptom**, it's not a **cause** you can directly monitor on a SQL server object level. You’d look at **query execution time**, **disk I/O**, or **CPU**, not generic latency.

✅ **Read replica I/O** and **CPU** are the two metrics that give you the root-level diagnostic power for SQL bottlenecks. Always go to the source!

---
# QUESTION

Which of the following types of scaling involves adding servers to a pool?

- ❌ A. Vertical  
- ✅ B. Horizontal  
- ❌ C. Elasticity  
- ❌ D. Autoscale  

Why the others are wrong:

- ❌ **A. Vertical** – This means upgrading an existing server’s resources (CPU, RAM, etc.), not adding servers.
- ❌ **C. Elasticity** – This refers to the *capability* to scale in/out or up/down automatically based on demand, but doesn’t define the *type* of scaling.
- ❌ **D. Autoscale** – Like elasticity, this is the *mechanism*, not the *direction*. Autoscaling can scale horizontally or vertically depending on the config.

✅ **Horizontal scaling** = adding more nodes/servers into a pool. Think “scaling out,” not just “scaling up.”

---
# QUESTION

Where are reports generated?

- ❌ A. Logging servers  
- ❌ B. Databases  
- ❌ C. Hypervisor  
- ✅ D. Cloud management  

Why the others are wrong:

- ❌ **A. Logging servers** – These *store logs*, but they don’t generate formatted reports. They’re raw data sources.
- ❌ **B. Databases** – These *store structured data* that can be queried, but they don’t *create* reports by themselves.
- ❌ **C. Hypervisor** – It manages virtual machines, not reporting functions. It’s infrastructure, not analytics.

✅ **D. Cloud management** – This is the correct answer because cloud management platforms *aggregate*, *analyze*, and *generate* reports across the environment (e.g., usage, cost, performance).

🧱 Think of cloud management as the "mission control" — it's where reporting, orchestration, and policy enforcement all come together.

---
# QUESTION

Sharon posted a new software update to her company’s popular smartphone application. After announcing the release, she has been monitoring her dashboard information and has noticed a large spike in activity. What cloud resource should she focus on?

- ❌ A. Storage  
- ❌ B. API  
- ✅ C. Network bandwidth  
- ❌ D. CPU  

Why the others are wrong:

- ❌ **A. Storage** – A software update might increase storage use slightly, but a **spike in user activity** isn't a storage problem.
- ❌ **B. API** – APIs handle requests, but unless there’s evidence of failures or overload at the endpoint level, bandwidth is the broader issue to examine first.
- ❌ **D. CPU** – CPU usage may spike, but it's typically **secondary** to the bandwidth bottleneck when mass downloads or access hits.

✅ **C. Network bandwidth** – When lots of users download an update or interact with cloud services simultaneously, **network resources** get hammered. Bandwidth saturation leads to slow response times, dropped connections, or timeouts — all symptoms Sharon is likely seeing.

🧠 Imagine a surge of people hitting a website to download a big app update — that crushes your pipes first, not your processors.

---
# QUESTION

Capacity and utilization reporting often contains data on which of the following objects?

- ✅ A. CPU  
- ❌ B. OS version  
- ❌ C. Volume tier  
- ✅ D. RAM  

Why the others are wrong:

- ❌ **B. OS version** – That’s a configuration detail, not capacity or utilization. It’s not something that "uses" resources.
- ❌ **C. Volume tier** – This is a *classification* (e.g., SSD vs. HDD), not a metric of usage or capacity.

✅ **A. CPU** – Core resource. Utilization reporting *definitely* monitors CPU use.  
✅ **D. RAM** – Another major resource. Memory usage is key to understanding system performance and planning scaling.

🧱 Capacity reporting = "How much?"  
🧱 Utilization reporting = "How much is being used?"

---
# QUESTION

Upgrading to a newer operating system may require that you update what?

✅ C. Baseline  
❌ A. Storage  
❌ B. Application Changes  
❌ D. RAM  

Why the others are wrong:

- ❌ **A. Storage** – While newer OS versions can be larger, upgrades rarely *require* additional storage unless you're low on space already.
- ❌ **B. Application Changes** – Apps might need updates, but that’s more about compatibility. It’s not always mandatory unless specific features break.
- ❌ **D. RAM** – Like storage, some upgrades *recommend* more RAM, but it’s not required unless minimum specs increase.

✅ **C. Baseline** – After upgrading an OS, you must capture a new baseline for performance, security, and system behavior. Your old benchmarks are now obsolete.  
Think of it like moving to a new house – you need a fresh inventory of everything before and after.

🧱 Always re-establish a known-good baseline after major system changes. It's your new normal.

---
# QUESTION

Which of the following applications tracks a process from start to finish?

✅ B. Workflow  
❌ A. Orchestration  
❌ C. NTP  
❌ D. API  

Why the others are wrong:

- ❌ **A. Orchestration** – Orchestration *automates* and coordinates tasks, but it doesn’t inherently *track* the flow. Think conductor, not reporter.
- ❌ **C. NTP** – Network Time Protocol just syncs clocks. It’s vital for *when* things happen, but it doesn’t monitor *what* is happening.
- ❌ **D. API** – APIs allow applications to talk to each other. They don’t track processes by themselves — they’re messengers, not managers.

✅ **B. Workflow** – A workflow application is designed specifically to track, manage, and automate a business or technical process *from beginning to end*. It logs each step and its status — perfect for visibility and control.

🧱 Workflow = step-by-step process tracking  
🎯 Think of a ticketing system: open, assign, escalate, resolve — that’s a workflow.

---
# QUESTION

Servers in high-performance computing clusters share which of the following?

✅ C. Availability zone  
❌ A. Latency  
❌ B. Vertical Scaling  
❌ D. Service level agreements  

Why the others are wrong:

- ❌ **A. Latency** – While low latency is *desired*, it’s not something servers "share" in a structural or architectural sense — it’s an outcome, not a shared resource.
- ❌ **B. Vertical Scaling** – HPC clusters use *horizontal scaling* (adding more nodes), not vertical (upgrading individual machines).
- ❌ **D. Service level agreements** – SLAs are agreements between *customers and providers*, not something servers themselves "share."

✅ **C. Availability zone** – Servers in HPC clusters are typically placed in the same **availability zone** to reduce latency and ensure fast, efficient communication between nodes. Shared AZ = shared network backbone = optimized performance.

🧱 HPC = clustered compute nodes  
🏗️ Placing nodes in the same AZ ensures they're close — physically and logically.

---
# QUESTION

Which of the following types of scaling involves replacing an existing server with another that has more capabilities?

✅ D. Vertical  
❌ A. Horizontal  
❌ B. Elasticity  
❌ C. Autoscale  

Why the others are wrong:

- ❌ **A. Horizontal** – Adds more servers to a pool, not upgrade individual servers. Think *scale out*, not *scale up*.
- ❌ **B. Elasticity** – Describes the ability to automatically scale *in or out* (horizontally) based on demand, not the method of scaling.
- ❌ **C. Autoscale** – This is a process, not a type. It can apply to horizontal or vertical scaling, depending on configuration.

✅ **D. Vertical** – This is *scale up*: swapping a machine for one with more CPU, RAM, or storage. One machine, bigger muscles.