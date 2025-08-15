# QUESTION 1  
A company must process and transform large datasets stored in Amazon S3 for analysis. They seek a serverless ETL solution that can automatically discover data schemas, manage dependencies, and integrate seamlessly with other AWS analytics services. Which AWS service **best** fits these requirements?

- ❌ A. Amazon Kinesis  
- ❌ B. Amazon EMR  
- ✅ C. AWS Glue  
- ❌ D. AWS Data Pipeline  

**Why the others are wrong:**

- ❌ **Amazon Kinesis** – Great for real-time data streaming, but not designed for full ETL workflows or schema discovery.
- ❌ **Amazon EMR** – A managed big data platform, but **not serverless** and requires managing clusters—overkill for this use case.
- ✅ **AWS Glue** – Purpose-built for **serverless ETL**, including schema discovery (via crawlers), job scheduling, and full integration with S3 and AWS analytics services.
- ❌ **AWS Data Pipeline** – Older tool mainly for scheduling and moving data; lacks modern ETL capabilities like schema inference or tight integration with AWS analytics stack.

---
# QUESTION 2  
Mindy has a SQL database back end that runs on a multi-CPU instance that has reached 100 percent utilization. The database supports a single server. Which of the following options does she have to support the requirements of this database?

- ❌ A. Horizontal scaling  
- ❌ B. Bursting  
- ❌ C. Elasticity  
- ✅ D. Vertical scaling  

**Why the others are wrong:**

- ❌ **Horizontal scaling** – Involves adding more servers or nodes. The question states the database supports a **single server**, ruling this out.
- ❌ **Bursting** – Typically refers to short-term CPU performance boosts (like on T-series instances). Doesn’t apply to consistent high CPU use.
- ❌ **Elasticity** – Refers to dynamic allocation based on load, but doesn’t address the physical limits of a single-instance database.
- ✅ **Vertical scaling** – Means upgrading the instance (more CPU/RAM) on a **single machine**, which fits the scenario exactly.
---
# QUESTION 3  
Ethel is the network architect for a hybrid cloud operation and has interconnected her private cloud to a community cloud in another state. She is investigating using the community cloud to supplement her private cloud operations during end-of-month processing. What operation is she going to perform?

- ✅ A. Bursting  
- ❌ B. Vertical scaling  
- ❌ C. Autoscaling  
- ❌ D. Elasticity  

**Why the others are wrong:**

- ✅ **Bursting** – This is exactly what cloud bursting refers to: temporarily using additional resources from a secondary cloud (like the community cloud) when demand spikes.
- ❌ **Vertical scaling** – This involves upgrading the existing instance (CPU, RAM), but doesn’t involve offloading to another cloud.
- ❌ **Autoscaling** – Automatically adjusts resources *within* a cloud service, not across hybrid cloud boundaries like private → community.
- ❌ **Elasticity** – Describes general ability to scale in/out or up/down, but isn’t specific to using *another* cloud’s resources in a hybrid setup.
---
# QUESTION 4  
An organization wants to know what its normal day-to-day web hit count is so that it can plan for the upcoming holiday selling season. Jim’s job is to measure the incoming web requests and graph them against delayed and missed connection counts. What type of dataset is Jim producing?

- ❌ A. Smoothing  
- ✅ B. Baseline  
- ❌ C. Variance  
- ❌ D. Metric  

**Why the others are wrong:**

- ❌ **Smoothing** – A technique used to filter or average data, not the actual dataset itself. It’s applied *after* data is collected.
- ✅ **Baseline** – This is the correct answer. Establishing the normal pattern of web traffic (day-to-day hit count) is building a **baseline** for future comparison.
- ❌ **Variance** – Measures the difference or fluctuation from the baseline. Jim’s just collecting data now—not analyzing deviation yet.
- ❌ **Metric** – A single unit of measurement (like “web hits per minute”), but not a full dataset or trend.
---
# QUESTION 5  
What does the application life cycle include?

- ❌ A. Retirements  
- ❌ B. Migrations  
- ❌ C. Upgrades  
- ❌ D. Deployments  
- ✅ E. All of these  

**Why the others are wrong:**

- ❌ **A–D individually** – Each option is **part** of the application life cycle, but not complete on its own.
- ✅ **E. All of these** – Correct. The application life cycle includes **planning, deployment, upgrades, migrations, and eventual retirement**. It's a full journey from inception to decommission.
---
# QUESTION 6  
To make sure that all customers can access only approved resources, Marie is auditing her public cloud identity systems. She wants to control specific access and operations. What is Marie defining?

- ✅ A. User-based policies  
- ❌ B. Resource-based policies  
- ❌ C. Federated approach  
- ❌ D. Access control lists  

**Why the others are wrong:**

- ✅ **User-based policies** – These define what actions specific users (or groups) can perform on which resources. It’s exactly what Marie is focused on: identity-based access control.
- ❌ **Resource-based policies** – These are attached directly to the resource and are often used when giving cross-account access. They’re not identity-focused.
- ❌ **Federated approach** – This deals with integrating external identity providers (like Google or AD), not directly managing user permissions.
- ❌ **Access control lists (ACLs)** – ACLs are lower-level controls used for very specific access rights (like file permissions), but not usually used for defining cloud identity policies.
---
# QUESTION 7  
To promote consistent cloud monitoring and to reduce configuration overhead, Lisa has created several policies to obtain baseline data. What type of policies is Lisa creating?

- ✅ A. Collection  
- ❌ B. Publishing  
- ❌ C. Notification  
- ❌ D. Dissemination  

**Why the others are wrong:**

- ✅ **Collection** – These policies define **what data should be gathered**, when, and how—perfect for building monitoring baselines.
- ❌ **Publishing** – Involves sharing or broadcasting data that has already been collected—not the act of gathering it.
- ❌ **Notification** – Related to alerts or event-driven messaging, not building baselines.
- ❌ **Dissemination** – Refers to distributing information after it’s processed; again, not the data-gathering stage.
---
# QUESTION 8  
Samantha has been monitoring her cloud web server dashboard, and she notices that the CPU utilization on her company’s database servers has been consistently at more than 80 percent utilization. She checked her baselines and reported that 57 percent utilization is normal. What is she noticing?

- ✅ A. Variance  
- ❌ B. Deviation  
- ❌ C. Baseline imbalance  
- ❌ D. Triggers  

**Why the others are wrong:**

- ✅ **Variance** – Correct. Variance refers to the measurable **difference between current behavior and the baseline**. In this case, the CPU is showing a significant variation from the expected average (57% vs 80%+).
- ❌ **Deviation** – While similar in meaning to variance, deviation is usually a **single instance of difference**, not a monitored trend or average discrepancy over time.
- ❌ **Baseline imbalance** – Not a standard or recognized term in cloud monitoring or performance analysis.
- ❌ **Triggers** – These are used to initiate alerts or actions, but Samantha is *observing* the metric, not responding to an automated threshold breach.
---
# QUESTION 9  
Dimitry has been tasked to develop a cross-cloud provider migration plan as part of his company’s business continuity plan. As he assesses the feasibility of migrating applications from one public cloud provider to another, what does he find is the service model that has the most lock-ins and is the most complex to migrate?

- ✅ A. SaaS  
- ❌ B. PaaS  
- ❌ C. IaaS  
- ❌ D. XaaS  

**Why the others are wrong:**

- ✅ **SaaS** – Correct. SaaS apps are fully managed by the provider. You have little visibility into the backend, and migrating to a different provider often means **replacing the entire application**, not just moving it.
- ❌ **PaaS** – Still has lock-in, but you usually have more control over the app logic, code, and data than you do with SaaS.
- ❌ **IaaS** – Offers the most control and flexibility, making
---
# QUESTION 10  
Dawn has been working in the network operations center (NOC) and has been tasked with performing root-cause analysis on a recent outage that affected the middle-tier web stack in a private cloud. She is looking at the log files and notices that there are more than 430 logs that were generated around the time the site failed. What function does Dawn need to perform to distill all of these log files into a meaningful report?

- ❌ A. Event analysis  
- ✅ B. Event correlation  
- ❌ C. Logging  
- ❌ D. Baseline  

**Why the others are wrong:**

- ❌ **Event analysis** – Sounds close, but it's more general. It refers to reviewing a single event or its effects. Dawn needs to connect **multiple events across logs**.
- ✅ **Event correlation** – Correct. Event correlation is the process of connecting related events across multiple sources and timestamps to identify the root cause—exactly what Dawn needs.
- ❌ **Logging** – Logging is the process of collecting the data—not analyzing or organizing it.
- ❌ **Baseline** – This refers to normal operating thresholds, not log analysis or incident investigation.
---
# QUESTION 11  
Bob is configuring an event notification service and notices that many different devices and services can be subscribers to the notification system’s published events queue. The notification services offer each event to be sent to a fan-out of multiple devices that can act upon the received information. What are examples of the notification server’s receivers?

- ❌ A. Service queues  
- ❌ B. Text message  
- ✅ C. All of these  
- ❌ D. A smartphone application  
- ❌ E. Email  
- ❌ F. APIs  

**Why the others are wrong:**

- ✅ **All of these** – Correct. Notification services like AWS SNS or similar platforms can send to **queues (e.g., SQS)**, **email**, **SMS**, **mobile apps (via push)**, and **webhooks/APIs**. This is classic fan-out architecture.
- ❌ **A–F individually** – All are valid examples, but choosing just one ignores the fact that notification systems support *multiple* receivers simultaneously.
---
# QUESTION 12  
Carol is collecting information on objects to monitor in her community cloud deployment. She is interested in establishing a baseline to produce a trend analysis report. What are some objects that she could natively monitor?

- ❌ A. Total storage capacity  
- ❌ B. Task runtime  
- ❌ C. Instance initialization time  
- ❌ D. Availability  
- ✅ E. All of these  
- ❌ F. MTBF  

**Why the others are wrong:**

- ✅ **All of these** – Correct. All of the listed metrics—storage, task duration, boot time, and availability—are native to most cloud monitoring systems and useful for trend and baseline reporting.
- ❌ **A–D individually** – Each is valid, but picking just one misses the broader view that Carol is tracking **multiple operational parameters**.
- ❌ **F. MTBF (Mean Time Between Failures)** – Important for reliability analysis, but it's typically **calculated**, not directly monitored in real-time.
---
# QUESTION 13  
George and Wendy are working together as cloud engineers to combine two like systems into one. What type of activity would necessitate this?

Each correct answer represents a complete solution. **Choose two.**

- ✅ A. Acquisition  
- ✅ B. Merger  
- ❌ C. Bursting  
- ❌ D. Divestiture  

**Why the others are wrong:**

- ✅ **Acquisition** – When one company acquires another, combining similar systems is a common integration task.
- ✅ **Merger** – Two companies merging often need to **unify IT systems**, including cloud services.
- ❌ **Bursting** – Refers to temporary scale-out to a secondary cloud (not combining systems).
- ❌ **Divestiture** – Opposite of a merger—splits assets/systems rather than combining them.
---
# QUESTION 14  
Elaine works in IT security, and she is reviewing user account policies. She needs to strengthen passwords by enforcing a mandatory minimum of a non-dictionary word that is six or more characters in length, contains at least one uppercase letter, and contains a special character. What is she defining?

- ✅ A. Password complexity  
- ❌ B. Password policies  
- ❌ C. Single sign-on  
- ❌ D. Password strengthening approach  

**Why the others are wrong:**

- ✅ **Password complexity** – Correct. Complexity rules include requirements like minimum length, use of uppercase, numbers, and special characters.
- ❌ **Password policies** – Broader category that may include expiration, history, reuse limits, etc. Complexity is **a subset** of this.
- ❌ **Single sign-on (SSO)** – Deals with access control and user authentication across multiple systems, not password composition.
- ❌ **Password strengthening approach** – A vague term, not a formal policy or technical standard.
- ---

# QUESTION 15  
Which of the following is the ability to dynamically add resources such as storage, CPUs, memory, and even servers?

- ✅ A. Elasticity  
- ❌ B. Auto-scaling  
- ❌ C. Bursting  
- ❌ D. Community cloud  

**Why the others are wrong:**

- ✅ **Elasticity** – Correct. Elasticity is the **core cloud concept** referring to automatically expanding or contracting resources based on demand.
- ❌ **Auto-scaling** – A feature that **enables** elasticity, but not the broader concept itself.
- ❌ **Bursting** – Temporary use of external resources (e.g., public cloud) during a spike—not a general dynamic allocation model.
- ❌ **Community cloud** – A cloud model shared by multiple organizations, unrelated to dynamic scaling.
---
# QUESTION 16  
Christina is configuring her public cloud object storage bucket for granular access from a new Linux VM. She wants to set the permissions on the storage system. What would you recommend?

- ✅ A. Access control list  
- ❌ B. Single sign-on  
- ❌ C. User-based  
- ❌ D. Federations  

**Why the others are wrong:**

- ✅ **Access control list (ACL)** – Correct. ACLs are commonly used for **object storage buckets** (like in AWS S3, Azure Blob, or GCP Storage) to control read/write access at a **fine-grained level**.
- ❌ **Single sign-on (SSO)** – Deals with authentication across services, not with object-level access permissions.
- ❌ **User-based** – General term, but not as precise or applicable as using ACLs for object storage.
- ❌ **Federations** – Used for identity management across domains or organizations—not relevant for managing **bucket access** directly.
---
# QUESTION 17  
To increase her organization’s security posture, Allison is reviewing user accounts that access the fleet cloud resources. Allison notices that, although the summer interns have left to go back to school, their accounts are still active. She knows that they will return for the winter corporate announcements and new-product rollouts to assist in the project over winter break. What would you suggest Allison do with these accounts?

- ❌ A. Change the access control.  
- ❌ B. Modify the confederation settings.  
- ❌ C. Change the resource access definitions.  
- ✅ D. Disable the accounts.  
- ❌ E. Delete the accounts.  
- ❌ F. Do nothing.  

**Why the others are wrong:**

- ❌ **A. Change the access control** – Doesn’t fully address the security concern; access control doesn’t deactivate the account.
- ❌ **B. Modify federation settings** – Irrelevant here. Federation relates to identity trust across domains, not temporary internal access.
- ❌ **C. Change resource access definitions** – Too broad, and may not effectively suspend the user accounts themselves.
- ✅ **D. Disable the accounts** – Correct. This is **best practice** for temporary deactivation while retaining the accounts for future use. No need to re-create them later.
- ❌ **E. Delete the accounts** – Too permanent. These users are expected to return, so deletion would cause unnecessary overhead.
- ❌ **F. Do nothing** – That’s a security risk. Leaving unused accounts active is a common vulnerability (or even audit failure).  

🛡️ **Pro Tip:** In cloud environments, disabling temporary users is a lightweight but effective access control strategy. 

---
# QUESTION 18  
Liza is reviewing the maintenance responsibilities between her company and its public cloud service provider. She notices that the cloud provider takes responsibility for the operating system, and she needs to assume responsibility for any applications or services running on the operating system. Under what type of service model is Liza operating?

- ❌ A. XaaS  
- ❌ B. IaaS  
- ✅ C. PaaS  
- ❌ D. SaaS  

**Why the others are wrong:**

- **A. XaaS** ❌  
  "Everything as a Service" is a general term that encompasses many models (SaaS, PaaS, IaaS, etc.). It’s too broad and not a specific model Liza would directly operate under.

- **B. IaaS** ❌  
  In IaaS, the **customer manages the operating system**. Since the cloud provider is managing the OS here, it cannot be IaaS.

- **D. SaaS** ❌  
  In SaaS, the provider handles **everything** — including the application. Liza is responsible for managing applications, which excludes SaaS.

```markdown
✅ Correct = PaaS (Platform as a Service)  
Liza doesn’t touch the OS, but she **does** manage the apps — textbook PaaS setup.
```

Let me know if you'd like this bundled into a quiz review set!

---
# QUESTION 19  
Matt is preparing for an upcoming promotion that his company is offering during a major soccer game. He needs to determine his options to add capacity to his company’s web server farm so that it can handle the anticipated additional workload. You are brought in to consult with him on his options.  
Which of the following options do you recommend as possible solutions?

Each correct answer represents a complete solution. Choose all that apply.

- ✅ A. Vertical scaling  
- ❌ B. Horizontal scaling  
- ❌ C. Community cloud  
- ✅ D. Cloud bursting  
- ✅ E. Elasticity  

Why the others are wrong:

- **B. Horizontal scaling** ❌  
  Not ideal here—it involves adding more servers, which requires load balancing and may not be practical short-term.

- **C. Community cloud** ❌  
  Irrelevant in this context; it’s about shared infrastructure between organizations, not dynamic scaling.

✅ **Correct answers explained**:

- **A. Vertical scaling**: Add CPU, memory, or disk to existing servers quickly.  
- **D. Cloud bursting**: Automatically shifts excess load to public cloud during traffic spikes.  
- **E. Elasticity**: Dynamically adjusts resource usage based on demand—perfect for unpredictable events.

---
# QUESTION 20  
Allison is preparing to modify a network access control list and add three firewall rules to her private cloud HR systems. She is planning on submitting a detailed plan to accomplish these tasks. What process is Allison following?

- ❌ A. Change advisory  
- ✅ B. Change management  
- ❌ C. Rollout  
- ❌ D. Cloud automation  

Why the others are wrong:

- **A. Change advisory** ❌  
  A *change advisory board (CAB)* reviews changes but is not the process itself. Allison is submitting the plan, not reviewing others.

- **C. Rollout** ❌  
  Rollout is the *deployment* phase, not the planning or approval phase Allison is in.

- **D. Cloud automation** ❌  
  Automation implies the changes are scripted and auto-deployed. Allison is manually planning changes—not automating them.

✅ **B. Change management**  
She’s submitting a detailed plan before making system changes. That’s textbook **change management**: evaluate, plan, approve, then implement.

---
# QUESTION 21  
Donald has been tasked by the IT security group in his company to prevent dictionary login attacks to the company’s VMs running in a private cloud at a remote data center. You have been brought in to offer him advice to deter the random but steady login attacks. What would you recommend Donald to enable to prevent this type of cyberattack?

- ✅ A. Lockout policy  
- ❌ B. Access control list  
- ❌ C. Single single-on  
- ❌ D. Lightweight directory access protocol  

Why the others are wrong:

- **B. Access control list** ❌  
  ACLs control *who* can access a system, not *how often* they can try to log in. Doesn’t address brute-force/dictionary-style login attempts directly.

- **C. Single single-on** ❌  
  Even if you had single sign-on (which is redundant here), it doesn’t mitigate password guessing attacks—it just centralizes credentials.

- **D. Lightweight directory access protocol** ❌  
  LDAP is a protocol for directory services. It’s not a defense mechanism—it’s how user authentication is performed.

✅ **A. Lockout policy**  
This is exactly what stops dictionary attacks. After a certain number of failed login attempts, the account gets locked—slamming the door on brute-force.
