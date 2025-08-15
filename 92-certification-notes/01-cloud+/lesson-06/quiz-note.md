
**Question 1**  
**✅ Correct**  
**Q:** Data replication is often used to store copies of real-time data in remote zones. When there is a need to have the master data immediately updated, and then on the back end update the remote zones, what type of replication would you recommend that your operations department configure?  
- ☐ Synchronous  
- ✅ Asynchronous  
- ☐ Mirroring  
- ☐ RAID 5  
**Explanation:** Asynchronous replication allows the primary system to update immediately without waiting for remote confirmation. Remote zones are updated later, which improves performance and reduces latency.
---
**Question 2**  
**✅ Correct**  
**Q:** Carl has been investigating stale records in his database that were added by other applications but never deleted or timed out after they were no longer in use. This mappings application is now causing issues with the server addressing and troubleshooting. What system is Carl looking at?  
- ☐ SNMP  
- ☐ FTP  
- ✅ DNS  
- ☐ DHCP  
**Explanation:** DNS can store stale or outdated records, especially in dynamic environments. These lingering entries can lead to name resolution problems and incorrect server mappings.
---
**Question 3**  
**✅ Correct**  
**Q:** Jack is preparing to update his company’s business continuity with details on its disaster recovery (DR) backup site. His plan is to have a facility ready with floor space, power, and cooling that has facilities for him to load in his server racks to restore service. What type of DR implementation is Jack deploying?  
- ☐ Hot site  
- ☐ Warm site  
- ✅ Cold site  
- ☐ Rollover  
**Explanation:** A cold site provides the physical infrastructure (space, power, cooling) but no active hardware or data. It's the most cost-effective option, but slowest to bring online.

---
**Question 4**  
**✅ Correct**  
**Q:** Will is running his backup DR site in a DNS load-balancing rotation for testing. He needs to ensure that the database in the DR facility is updated in real-time and current with the production replica in the primary data center. What type of updates should he define in his primary data center servers before enabling DNS load balancing?  
- ☐ RAID 5  
- ☐ Mirroring  
- ☐ Asynchronous replication  
- ✅ Synchronous replication  
**Explanation:** Synchronous replication ensures real-time, simultaneous updates between primary and DR databases, keeping both sites fully current — which is essential for load-balanced environments.
---
**Question 5**  
**✅ Correct**  
**Q:** Christina has been pinging a new web server by its URL and getting strange and seemingly unexplainable responses from unrecognized systems. She recalls that the new web farm is on a reclaimed subnet that was no longer in use in their cloud server fleet. What would you recommend that she investigate to resolve the issue?  
- ☐ DHCP  
- ✅ DNS  
- ☐ Stale network access control lists  
- ☐ Orphaned services  
**Explanation:** The issue likely stems from stale or incorrect DNS records still pointing the URL to old or incorrect IP addresses within the reclaimed subnet. DNS cleanup is the proper fix here.
---
**Question 6**  
**✅ Correct**  
**Q:** Jerry noticed on his WAN monitoring dashboard that there are peaks in traffic flow from the primary to his hot site. What two things might be taking place?  
- ✅ Synchronous replication  
- ✅ Asynchronous replication  
- ☐ File transfer  
- ☐ Continuity updates  
**Explanation:** Both synchronous and asynchronous replication involve copying data between sites. Synchronous replication happens in real time, while asynchronous replication happens on a delay — both can generate significant WAN traffic depending on timing and data load.
---
**Question 7**  
**✅ Correct**  
**Q:** Tom has been performing an ongoing inventory of his public cloud assets and has found several storage volumes, CPU allocations, VMs, and firewall instances that are not connected to any project and are not being used. On what services is Tom collecting data?  
- ☐ Stale services  
- ✅ Orphaned resources  
- ☐ Dashboard service  
- ☐ DNS  
**Explanation:** Orphaned resources are unused cloud assets (like VMs, volumes, or firewalls) that aren't tied to active projects. Identifying and cleaning these up helps control cost and reduce attack surface.
---
**Question 8**  
**✅ Correct**  
**Q:** What disaster recovery (DR) location can be used to cache data close to your customer and ease access to your fleet of web servers?  
- ☐ Cold  
- ✅ Edge  
- ☐ Zone  
- ☐ Region  
- ☐ Hot  
- ☐ Warm  
**Explanation:** Edge locations are designed to cache content close to the end user, reducing latency and improving access to web services. They're often used in CDN and DR strategies for fast, localized access.
---
**Question 9**  
**✅ Correct**  
**Q:** During a disaster recovery switchover, what network services may need to be modified as part of a multisite failover to the backup site?  
- ☐ FTP  
- ☐ DNS  
- ☐ Active Directory  
- ✅ All of these  
- ☐ DHCP  
**Explanation:** A full DR failover often involves reconfiguring or redirecting multiple services — DNS for name resolution, DHCP for IP addressing, FTP for file access, and Active Directory for identity management.
---
**Question 10**  
**✅ Correct**  
**Q:** To meet regulatory requirements, Jill must store customer transaction records for seven years. The data will most likely never be accessed after the second year and can be stored offline to reduce storage costs. What type of storage operation can Jill implement to achieve her goal?  
- ☐ File transfer  
- ☐ Data store  
- ☐ Replication  
- ✅ Archive  
**Explanation:** Archiving stores infrequently accessed data for long-term retention at a lower cost, ideal for compliance and regulatory requirements like Jill’s.
---
**Question 11**  
**✅ Correct**  
**Q:** Which disaster recovery metrics are used to create a measurable SLA that outlines when you can expect your systems to be back online and how much data loss you sustained after an outage?  
Each correct answer represents a complete solution. Choose all that apply.  
- ✅ RTO  
- ✅ RPO  
- ☐ SLA  
- ☐ DR  
**Explanation:**  
- **RTO (Recovery Time Objective):** Defines how quickly systems must be restored after an outage.  
- **RPO (Recovery Point Objective):** Defines how much data loss is acceptable, measured in time.  
These two metrics are core components of an SLA in disaster recovery planning.
---
**Question 12**  
**✅ Correct**  
**Q:** These cloud facilities provide the ability to connect locally for fast, low-latency connections to the DR location. They can also store, or cache, data at these locations for very fast responses to local user requests. Which of these is explained in the given scenario?  
- ☐ Replication  
- ☐ Region  
- ✅ Edge location  
- ☐ Availability zone  
**Explanation:** Edge locations are distributed facilities used to deliver cached or replicated content quickly and efficiently to nearby users, reducing latency and improving performance.
---
**Question 13**  
**✅ Correct**  
**Q:** Sharon has been directed to put together a disaster recovery (DR) plan based on directives from her company’s executive management team. The company’s core business is operating an e-commerce website selling winter apparel, with 85 percent of its revenue received during the holiday season. If there was a prolonged outage, it would put the company’s ability to continue as a financially viable operation in peril. Sharon has been instructed to create a plan that will restore operations in the shortest amount of time possible. What DR model should Sharon implement?  
- ☐ Warm site  
- ✅ Hot site  
- ☐ Rollover  
- ☐ Cold site  
**Explanation:** A hot site is fully operational and kept in sync with the primary environment, enabling near-instant failover and the shortest recovery time — essential for businesses with critical uptime needs.
---
**Question 14**  
**✅ Correct**  
**Q:** How does backing up Amazon DynamoDB tables help businesses?  
- ☐ By automatically increasing the table's read and write capacity  
- ☐ By moving the table to a different AWS region  
- ☐ By preventing users from adding new data to the table  
- ✅ By ensuring data can be recovered after accidental loss or failure  
**Explanation:** Backups of DynamoDB tables protect against data loss by allowing businesses to restore tables to a previous state after accidental deletion, corruption, or system failure.
---
**Question 15**  
**✅ Correct**  
**Q:** Computer operating systems have mechanisms that grant rights to users for access to system objects like storage volume directories and files, administrator rights, and so on. What should you monitor to make sure that old or unused entries are deleted?  
- ☐ MFA  
- ☐ Dashboard  
- ☐ Stale cache  
- ✅ Access control  
**Explanation:** Access control mechanisms manage user permissions. Regularly auditing access control ensures unused or outdated permissions are removed, reducing security risk.
---
**Question 16**  
**✅ Correct**  
**Q:** Hank is preparing a disaster recovery test drill in advance of the upcoming hurricane season along the Gulf of Mexico. His plan is to create a DR location in the Midwest and have a database server running at that location with a synchronously refreshed data replica. His DR plan calls for activating all other services in the event of a hurricane causing an outage at his primary data center. What model is Hank going to deploy to meet his requirements?  
- ☐ Cold site  
- ✅ Warm site  
- ☐ Hot site  
- ☐ Active/passive  
**Explanation:** A warm site includes pre-installed and running infrastructure (like a synced database), but not all services are active until failover. It strikes a balance between cost and readiness.

---
**Question 17**  
**✅ Correct**  
**Q:** James has been directed by his employer’s finance department that they cannot afford to lose any more than 30 minutes of data in case of a database failure or other catastrophic event. James has updated his corporate business continuity plan and has had his cloud provider update its SLA. What was the metric that was changed?  
- ☐ RSA  
- ☐ SLA  
- ☐ RTO  
- ✅ RPO  
**Explanation:** The RPO (Recovery Point Objective) defines the maximum acceptable amount of data loss measured in time. A 30-minute window means the RPO is 30 minutes.
---
**Question 18**  
**✅ Correct**  
**Q:** What service provides permit and deny policies that require regular review to delete unused entries?  
- ✅ Firewalls  
- ☐ Active Directory  
- ☐ DNS  
- ☐ DHCP  
**Explanation:** Firewalls use permit and deny rules to control traffic. These rule sets must be reviewed regularly to remove obsolete or unused entries that could create security gaps.
---
**Question 19**  
**✅ Correct**  
**Q:** Sharon is a network engineer for your firm and is investigating the WAN connection to the hot site. In the event of operations being moved to the backup location, she wants to make sure that the load capacity is available. What should she be **most** concerned about?  
Each correct answer represents a complete solution. Choose two.  
- ☐ SLA  
- ☐ QOS  
- ✅ Bandwidth starvation  
- ✅ Peak capacity  
**Explanation:**  
- **Bandwidth starvation** occurs when critical systems don’t receive the bandwidth they need due to congestion.  
- **Peak capacity** must be evaluated to ensure the WAN link can handle the full load during failover to the hot site.
---
**Question 20**  
**✅ Correct**  
**Q:** Cloud dashboards allow for monitoring and sometimes configuring maintenance operations with the cloud provider. If you have regularly scheduled backups for your cloud storage volumes, you can configure the cloud provider to perform specific operations for you using what back-end systems?  
- ☐ Replication  
- ☐ Orphaned  
- ☐ Synchronous  
- ✅ Automation  
**Explanation:** Automation systems allow cloud providers to carry out scheduled tasks like backups or maintenance operations without manual intervention, improving efficiency and reliability.

---
**Question 21**  
**✅ Correct**  
**Q:** Mark has been reviewing disaster recovery planning, and after receiving direction from his company’s board of directors, it has been determined that they can only withstand a maximum of 36 hours of downtime. Mark is updating his DR plan with this new metric. What part of the plan should he modify?  
- ☐ DBO  
- ☐ RSO  
- ☐ RPO  
- ✅ RTO  
**Explanation:** The **RTO (Recovery Time Objective)** defines how quickly systems must be restored after an outage. A 36-hour downtime tolerance directly relates to the RTO.
