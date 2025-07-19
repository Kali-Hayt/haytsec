### ❓ Flashcard 1

**Q:** You are explaining to a new hire at your private cloud data center about the process to follow when modifying systems and services in the cloud. What is this process called?

✅ **A:** Change management

---

**Why the others are wrong:**
- ❌ Lockout: Refers to denying access to a system, not managing changes.
- ❌ Horizontal: Likely refers to horizontal scaling, unrelated to change processes.
- ❌ I don't know: Not a valid answer for certification... or real life. 😅
---
### ❓ Flashcard 2

**Q:** True or false? In a single primary database, database write performance can be improved by scaling horizontally.

✅ **A:** False

---

**Why the others are wrong:**
- ❌ Horizontal: Horizontal scaling adds more *read replicas* or parallel systems — not helpful for **writes** in a single primary DB.
- ❌ Lockout: Unrelated to scaling or performance.
- ❌ I don't know: Not helpful when you're being tested. 😅

🧠 **Note:** To improve write performance in a single primary DB, you'd need vertical scaling (more CPU/RAM) or database sharding—not horizontal scaling alone.

---
### ❓ Flashcard 3

**Q:** What authentication configuration will ignore a dictionary login attack after a set number of failed attempts?

✅ **A:** Lockout

---

**Why the others are wrong:**
- ❌ Change management: Involves procedural IT changes, not authentication defenses.
- ❌ Vertical: Refers to scaling resources (CPU, RAM), not access control.
- ❌ I don't know: That option will never defend against brute-force attacks 😅

🛡️ **Tip:** A lockout policy protects systems by disabling login attempts after too many failures — a strong deterrent to dictionary or brute-force attacks.

---
### ❓ Flashcard 4

**Q:** Tom’s SQL database backend runs on a multi-CPU instance that often reaches 100% utilization. The database can operate on only a single server. What scalability model can he implement?

✅ **A:** Vertical

---

**Why the others are wrong:**
- ❌ Horizontal: Requires distributing workload across multiple systems — not possible here since it’s limited to **one** server.
- ❌ False: Not a valid answer in this context.
- ❌ I don't know: Don’t be Tom. Know your scale strategies. 😄

🧠 **Reminder:**  
**Vertical scaling** = add more resources (CPU, RAM) to a **single** machine.  
**Horizontal scaling** = add more machines/instances.

---
### ❓ Flashcard 5

**Q:** During peak usage times, BigCo’s fleet of Internet-facing e-commerce servers often reaches maximum CPU utilization. The managers like that the cloud is resilient enough to add and remove servers on demand. What type of scaling are they implementing?

✅ **A:** Horizontal

---

**Why the others are wrong:**
- ❌ Vertical: Adds more resources to a single machine, not multiple servers.
- ❌ Change management: Refers to planning and approving changes, not scaling.
- ❌ I don't know: But now you do. 😉

🧠 **Tip:**  
**Horizontal scaling** = scaling out by adding/removing servers.  
**Vertical scaling** = scaling up by upgrading a server’s hardware.

---
### ❓ Flashcard 6

**Q:** What cloud automation feature allows cloud services to expand and contract based on actual usage?

✅ **A:** Elasticity

---

**Why the others are wrong:**
- ❌ Change management: Involves planned procedural updates, not dynamic resource adjustment.
- ❌ Horizontal: Describes *how* to scale (adding nodes), not *when or why*.
- ❌ I don't know: Not a strategy you want to deploy in the cloud. 😅

🧠 **Pro tip:**  
Elasticity = **automated** scaling up/down based on demand  
Scalability = **ability** to scale  
Horizontal = **direction** of scaling  

----
### ❓ Flashcard 7

**Q:** What type of scaling involves replacing an existing server with another that has more capabilities?

✅ **A:** Vertical

---

**Why the others are wrong:**
- ❌ False: Not a type of scaling — just a distractor.
- ❌ Lockout: Refers to authentication control, not infrastructure.
- ❌ I don't know: But now you do. 🔧

🧠 **Vertical scaling** = upgrading the same server with more CPU, RAM, storage, etc.  
**Horizontal scaling** = adding more servers, not replacing one.
