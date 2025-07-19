**Question 1**  
**✅ Correct**  
**Q:** Your IaaS cloud company has announced that there will be a brief outage for regularly scheduled maintenance over the weekend to apply a critical hotfix to vital infrastructure. What are the systems they may be applying patches to?  
Each correct answer represents a complete solution. Choose all that apply.

- ✅ A. Load balancer  
- ✅ B. Hypervisor  
- ✅ C. Router  
- ☐ D. Email server  
- ☐ E. Virtual machine  

**Explanation:**  
Infrastructure patches in an IaaS environment often include network and virtualization components like **load balancers**, **hypervisors**, and **routers**. These are considered critical infrastructure. Virtual machines and email servers are more likely customer-managed or fall under different update policies.

---
**Question 2**  
**✅ Correct**  
**Q:** Which of the following is a tightly coupled computer system that allows for software patching without incurring downtime?

- ☐ A. Blue-green  
- ☐ B. Availability zone  
- ✅ C. Cluster  
- ☐ D. RAID  

**Explanation:**  
A **cluster** is a tightly coupled system of computers that work together as a single unit. It allows workloads to shift between nodes during maintenance tasks like patching, avoiding downtime. Blue-green is a deployment strategy, availability zones are physical data center groupings, and RAID is a storage redundancy method.

---
**Question 3**  
**✅ Correct**  
**Q:** What backup solution requires an administrator or tape jukebox to make it available by inserting a tape or other media into a storage system for retrieval?

- ☐ A. Storage  
- ✅ B. Offline  
- ☐ C. SAN A/B  
- ☐ D. FCON  

**Explanation:**  
**Offline storage** refers to backup media—like tapes or external drives—that aren't immediately accessible. An administrator must physically load them into a system for retrieval. It's slower but provides a high level of protection from cyber threats and data corruption.

---
**Question 4**  
**✅ Correct**  
**Q:** Before a new patch is released to the public, the release manager at a large software development house has requested a report that shows the pass/fails data to verify that the fix does, in fact, work. He is requesting data about the issue it was intended to fix and the results of the tests performed to make sure that the fix does not interfere with other processes and that there are no memory or buffer issues experienced with the patched version of the software. What process was the release manager verifying?

- ☐ A. Orchestration  
- ☐ B. Rollout  
- ✅ C. QA  
- ☐ D. Automation  

**Explanation:**  
**QA (Quality Assurance)** is the process of verifying that a patch or fix works as intended without introducing new issues. The release manager is validating the software’s reliability and performance post-patch, which falls directly under QA testing responsibilities.

---
**Question 5**  
**✅ Correct**  
**Q:** What is the primary purpose of a code review?

- ☐ A. To allow developers to write code without following guidelines  
- ☐ B. To increase development speed by skipping documentation  
- ✅ C. To detect defects, enforce coding standards, and improve software quality  
- ☐ D. To replace automated testing with manual inspection  

**Explanation:**  
The main goal of a **code review** is to ensure that code meets quality standards, is free of defects, and follows organizational or industry best practices. It helps catch bugs early, maintain consistent style, and ensure maintainability and security of the codebase.

---
**Question 6**  
**✅ Correct**  
**Q:** Which of the following may offer new features and benefits in addition to bug fixes?

- ☐ A. Hotfix  
- ☐ B. Patch  
- ✅ C. Version update  
- ☐ D. Rollout  

**Explanation:**  
A **version update** often includes not only bug fixes but also **new features, performance enhancements, and security improvements**. In contrast, hotfixes and patches typically address urgent or minor issues without adding functionality.

---
**Question 7**  
**✅ Correct**  
**Q:** To meet regulatory requirements, your company must provide geographical separation between active and backup data of certain medical records that your company collects and processes. The requirements stipulate that the data cannot leave the country and must be in two or more data centers. As the cloud professional for your company, what recommendations would you offer to meet these requirements?

- ☐ A. Offline  
- ☐ B. Target  
- ☐ C. Incremental  
- ✅ D. Remote  

**Explanation:**  
**Remote backups** stored in multiple geographically separated data centers within the same country meet compliance requirements for **data redundancy and regulatory location restrictions**. This ensures both availability and legal adherence without exporting sensitive medical data.

---
**Question 8**  
**✅ Correct**  
**Q:** Which of the following are the types of queues supported by Amazon SQS?

- ☐ A. FIFO and LIFO queues  
- ✅ B. Standard and FIFO queues  
- ☐ C. Priority and LIFO queues  
- ☐ D. Standard and priority queues  

**Explanation:**  
Amazon SQS supports **Standard** queues (which provide high throughput and at-least-once delivery) and **FIFO** queues (First-In-First-Out for ordered delivery). **LIFO** and **priority** queues are not natively supported in SQS.

---
**Question 9**  
**✅ Correct**  
**Q:** Which of the following defines a structured process for a series of actions that should be taken in order to complete a process?

- ✅ A. Workflow automation  
- ☐ B. Automation  
- ☐ C. Application programming interface  
- ☐ D. Orchestration  

**Explanation:**  
**Workflow automation** refers to the use of predefined rules and logic to automate a sequence of actions in a structured way. It ensures tasks are completed in a consistent order, which is essential for reliable process completion.

---
**Question 10**  
**✅ Correct**  
**Q:** When applying a series of patches to your fleet of middleware servers in the cloud, you are concerned about the monitoring systems generating invalid alerts. What parts of the server maintenance process would cause this?  
Each correct answer represents a complete solution. Choose all that apply.

- ☐ A. Rolling upgrades  
- ✅ B. Shutdown  
- ✅ C. Restart  
- ☐ D. API polling  

**Explanation:**  
**Shutdowns** and **restarts** interrupt system availability, which can confuse monitoring tools into triggering invalid alerts. These changes appear as outages, even if they’re planned. **Rolling upgrades** aim to avoid this issue by keeping portions of the system online.  

---
**Question 11**  
**✅ Correct**  
**Q:** Which of the following options is used to combine and execute the multiple tasks that must be completed to accomplish an operation?

- ☐ A. SDN  
- ✅ B. Orchestration  
- ☐ C. REST/API  
- ☐ D. XML  

**Explanation:**  
**Orchestration** is the process of coordinating and managing multiple tasks or workflows, often automated, to achieve a desired outcome. It ensures that tasks are executed in the proper sequence and dependencies are respected.  

---
**Question 12**  
**✅ Correct**  
**Q:** You have been asked to update your entire fleet of Internet-facing web servers to remediate a critical bug. Your supervisor has agreed to operate under reduced computing capacity during the process but stipulates that there can be no downtime. What upgrade approach should you recommend that your company follow to meet these requirements?

- ☐ A. Hotfix  
- ✅ B. Rolling  
- ☐ C. Orchestration  
- ☐ D. Blue-green  

**Explanation:**  
**Rolling upgrades** allow updates to be applied incrementally across servers without taking the entire system offline. Some servers are updated while others continue to serve users, ensuring **zero downtime** with only **reduced capacity** temporarily.

---
**Question 13**  
**✅ Correct**  
**Q:** When a server is undergoing updates, it may be in a state that it will not respond to health checks, API calls, SNMP, or any other means used to monitor its health by network management systems. This may cause false alarms and trigger automated troubleshooting systems. What can be done to prevent false alarms?  
*Each correct answer represents a part of the solution. Choose two.*

- ✅ A. Disable system alerts.  
- ☐ B. Assign a workflow to the orchestration rollout.  
- ☐ C. Edit workflow scripts.  
- ✅ D. Put the system into maintenance mode.  

**Explanation:**  
To prevent monitoring systems from triggering unnecessary alerts during updates:
- **Disabling system alerts** prevents alerts from being sent when the system is expected to be unresponsive.
- **Maintenance mode** explicitly tells monitoring tools that downtime is planned and safe, suppressing automatic troubleshooting actions.

---
**Question 14**  
**✅ Correct**  
**Q:** What type of backup system is intended to provide quick restore access if needed?

- ☐ A. vSAN  
- ☐ B. Replica  
- ✅ C. Online  
- ☐ D. Offline  

**Explanation:**  
**Online** backups are kept readily available for rapid restoration—ideal when uptime is critical.  
**Offline** backups (like tape) are cheaper for long-term storage but much slower to access.

---
**Question 15**  
**✅ Correct**  
**Q:** What type of software change is designed for rapid deployment and to correct a specific and critical issue?

- ☐ A. Version update  
- ☐ B. Rollout  
- ✅ C. Hotfix  
- ☐ D. Patch  

**Explanation:**  
A **hotfix** is a quick, targeted software update meant to address a critical issue—typically security-related or bug-fix—without waiting for a larger update or full patch cycle.

---
**Question 16**  
**✅ Correct**  
**Q:** Developer A and Developer B work on separate branches. Developer A merges their branch using a fast-forward merge. When Developer B tries to merge, Git reports a merge conflict. What is the *most* likely reason?

- ☐ A. Developer A's fast-forward merge caused a conflict for Developer B.  
- ☐ B. An outdated repository forces conflicts.  
- ✅ C. Developer B modified the same lines of code as another merged branch.  
- ☐ D. Three-way merges always cause conflict.  

**Explanation:**  
Merge conflicts most commonly occur when two developers modify the same lines of code. Developer B likely changed the same lines that Developer A had already merged, resulting in Git being unable to reconcile the difference without manual intervention.

---
**Question 17**  
**✅ Correct**  
**Q:** Which of the following is a file-based image of the current state of VM, including the complete operating system and all applications that are stored on it?

- ☐ A. Clone  
- ✅ B. Snapshot  
- ☐ C. Backup  
- ☐ D. Replica  

**Explanation:**  
A snapshot captures the exact state of a virtual machine at a specific point in time, including memory, settings, and disk contents. It's often used for quick recovery or rollback before changes, especially in virtualization environments like VMware or Hyper-V.

---
**Question 18**  
**✅ Correct**  
**Q:** What is the primary purpose of hardware pass-through in virtualized environments?

- ☐ A. To abstract physical hardware from virtual machines  
- ☐ B. To improve hypervisor abstraction layers  
- ☐ C. To enhance software-based emulation  
- ✅ D. To allow virtual machines direct access to physical hardware components  

**Explanation:**  
Hardware pass-through (often using technologies like VT-d or AMD-Vi) allows a VM to directly access physical hardware such as a GPU or network card. This bypasses the hypervisor for that device, reducing latency and increasing performance—especially for resource-intensive tasks like gaming, scientific computing, or high-speed networking.

---
**Question 19**  
**✅ Correct**  
**Q:** A system administrator needs to install a software package on a Ubuntu server while ensuring all dependencies are automatically resolved. Which command should they use?

- ☐ A. `rpm -i package.rpm`  
- ☐ B. `yum install package-name`  
- ✅ C. `apt-get install package-name`  
- ☐ D. `dpkg -i package.deb`  

**Explanation:**  
On Ubuntu (a Debian-based system), `apt-get install` is the preferred method for installing packages because it automatically resolves and installs dependencies. `dpkg` does not handle dependencies, and `rpm`/`yum` are used in Red Hat-based systems like CentOS or Fedora.

---
**Question 20**  
**✅ Correct**  
**Q:** What backup method creates a master copy of a system image and uses it as a template to create additional systems?

- ☐ A. Full backup  
- ☐ B. Replicate  
- ✅ C. Cloning  
- ☐ D. Snapshot  

**Explanation:**  
Cloning creates an exact, master image of a system which can be used to spin up identical systems repeatedly. It is commonly used in deployment and provisioning scenarios.

---
**Question 21**  
**✅ Correct**  
**Q:** What type of software change is designed to address a known bug or issue and to bring a system up-to-date with previous bug fixes?

- ☐ A. Hotfix  
- ✅ B. Patch  
- ☐ C. Version update  
- ☐ D. Rollout  

**Explanation:**  
A patch is intended to fix known bugs or security issues and includes previous bug fixes, making it cumulative and ideal for ongoing maintenance.

---
**Question 22**  
**✅ Correct**  
**Q:** Which of the following automation systems are used for patch management?  
Each correct answer represents a complete solution. Choose all that apply.

- ✅ A. Ansible  
- ✅ C. Chef  
- ✅ E. Puppet  
- ☐ B. Cloudpatch  
- ☐ D. Cloud Deploy  
- ☐ F. DevOps  

**Explanation:**  
Ansible, Chef, and Puppet are widely used configuration management tools that support patch management as part of their automation capabilities.  
Cloudpatch is less commonly recognized in enterprise environments, while DevOps is a methodology, and Cloud Deploy focuses on application deployment, not patching.

---
**Question 23**  
**✅ Correct**  
**Q:** What type of backup operation is based on the change of the source data since the last backup was performed?

- ✅ A. Incremental  
- ☐ B. Differential  
- ☐ C. Full  
- ☐ D. Online  

**Explanation:**  
Incremental backups only copy the data that has changed since the *last backup of any type* (usually the last incremental), making them fast and efficient.  
Differential backups, in contrast, copy all data changed since the last *full* backup.

---
**Question 24**  
**✅ Correct**  
**Q:** What is the primary purpose of the RPM?

- ☐ A. To compile source code into executable binaries  
- ☐ B. To configure network settings  
- ☐ C. To monitor system performance metrics  
- ✅ D. To manage the installation, updating, and removal of software packages  

**Explanation:**  
RPM stands for **Red Hat Package Manager**. It's a powerful package management system used to install, update, uninstall, verify, and manage software packages on Red Hat–based Linux systems like RHEL and CentOS.

---
**Question 25**  
**✅ Correct**  
**Q:** Your company’s primary application is critical to the power generation industry and must be highly available. When critical patches need to be installed, downtime is not an option that your customers can tolerate. You have designed a web architecture to take this into account and that allows you to have an exact copy of your production fleet that can be brought online to replace your existing deployment for patching and maintenance. What type of model did you implement?

- ☐ A. DevOps  
- ☐ B. Cluster  
- ☐ C. Rolling  
- ✅ D. Blue-green  

**Explanation:**  
The **blue-green deployment model** uses two identical environments (Blue and Green). One serves production traffic while the other is idle. Updates are applied to the idle one and traffic is switched over once validated—this minimizes downtime and risk.

---
**Question 26**  
**✅ Correct**  
**Q:** What backup type offers the advantage of a complete and up-to-date copy of your data in one operation?

- ☐ A. Online  
- ✅ B. Full  
- ☐ C. Differential  
- ☐ D. Incremental  

**Explanation:**  
A **full backup** captures all data in one operation, creating a complete and up-to-date copy. It’s the most comprehensive method, though it takes more time and storage than incremental or differential backups.
