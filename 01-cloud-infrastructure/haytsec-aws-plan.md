## ☁️ HaytSec AWS Startup Plan

This document is the tactical launch plan for building out HaytSec’s cloud infrastructure.  
Each phase builds toward a simulated security operation in AWS — hardened, automated, and documented.

---

### 🛫 Phase 0: Local Foundations

- [x] Create `HaytSec` Obsidian vault and folder structure  
- [x] Set up GitHub repo to version control notes and scripts  
- [x] Install Obsidian plugins: Homepage, Calendar, etc.  
- [x] Write initial files:  
  - `haytsec-mission.md`  
  - `about-mr.hayt.md`  
  - `haytsec-aws-startup-plan.md`  
- [ ] Write and organize local documentation under correct folders  
- [ ] Begin tagging (`#cert`, `#lab`, `#cloud`, etc.)

---

### 🚀 Phase 1: AWS Account Setup

- [ ] Create new AWS account(s) dedicated to HaytSec  
- [ ] Enable MFA and harden root user  
- [ ] Configure budget alerts, billing guardrails  
- [ ] Set up Organization & SCPs (if multi-account)

---

### 🏛️ Phase 2: IAM + Identity Foundations

- [ ] Define IAM groups and roles (admin, auditor, automation, etc.)  
- [ ] Create IAM policies (least privilege)  
- [ ] Enable CloudTrail and Config for auditability  
- [ ] Write scripts to rotate access keys, enforce MFA  

---

### 🧱 Phase 3: Infrastructure-as-Code

- [ ] Define Terraform baseline for networking, IAM, logging  
- [ ] Deploy isolated VPC with subnets, NAT gateway, routing  
- [ ] Write IaC for S3 buckets, EC2 templates  
- [ ] Test destroy and rebuild  

---

### 🛡️ Phase 4: Security Tooling

- [ ] Enable GuardDuty, Security Hub, and Config Rules  
- [ ] Deploy custom Lambda for alerting or remediation  
- [ ] Write scripts to:  
  - Simulate basic attacks (port scan, IAM misuse)  
  - Run detection & logging checks  
  - Auto-tag suspicious resources  
  - Auto-lock down misconfigured S3  
- [ ] Build bots for red/blue team operations (attack and defend)

---

### 📖 Phase 5: Documentation + Sharing

- [ ] Document all infrastructure setup in markdown  
- [ ] Publish selected tools/scripts in GitHub repo  
- [ ] Create visual diagrams (Lucidchart, Diagrams.net)  
- [ ] Create \"playbooks\" for:  
  - IAM setup  
  - Cloud deployment flow  
  - Security baselines

---

> *“Build it like it matters. Secure it like you're the last line of defense.”*  
> — Mr. Hayt
