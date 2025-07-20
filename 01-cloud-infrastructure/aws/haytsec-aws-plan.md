## ☁️ HaytSec AWS Infrastructure Plan

This document tracks HaytSec’s full cloud infrastructure deployment lifecycle.  
Each phase maps directly to a folder in the vault under `01-cloud-infrastructure/aws/`.  
Every build decision is security-first, automation-ready, and audit-backed.

---

### 🧰 Phase 0 – Primer & Tooling

📂 `phase-0-primer/`

- Overview of AWS core services
- CLI and SDK setup
- Credential handling (profiles, vaults, secrets)
- Account structure planning (root vs. org vs. delegated admin)
- Link to `iac/` folder and Terraform strategy
- Quickstarts and install notes

---

### 🛫 Phase 1 – Account & Billing Foundation

📂 `phase-1-account/`  
📸 `screenshots-audit/`  
📂 `docs/billing/`

- Root MFA setup
- Budget alerts and free tier tracking
- Billing alarm configuration
- Cost Explorer, usage reports
- Create org and enable SCPs (if multi-account)
- Setup baseline account guardrails

---

### 🌐 Phase 2 – Networking Foundation

📂 `phase-2-networking/`

- VPC design (CIDR blocks, AZ placement)
- Public vs. private subnets
- Internet Gateway (IGW), NAT Gateway
- Route Tables, NACLs
- DHCP options sets
- Elastic IPs

---

### 🔐 Phase 3 – IAM & Security Services

📂 `phase-3-security/`

- IAM groups, users, roles
- MFA enforcement policies
- Custom policies with least privilege
- CloudTrail global + regional setup
- AWS Config tracking
- SCP examples (if using AWS Org)
- KMS and encryption keys
- Secrets Manager / Parameter Store

---

### 🖥️ Phase 4 – Compute Layer

📂 `phase-4-compute/`

- Hardened AMI strategy
- EC2 provisioning templates (launch templates, autoscaling)
- Security Group design per layer
- Bastion host setup
- Bootstrap scripts / cloud-init
- Compute tagging conventions

---

### 📦 Phase 5 – Storage Architecture

📂 `phase-5-storage/`

- S3 buckets (naming, versioning, encryption)
- Bucket policies and access control
- Lifecycle rules and cost management
- Glacier and archival strategy
- Cross-region replication (if applicable)
- RDS / EFS / Backup notes (TBD)

---

### 📊 Phase 6 – Monitoring & Audit

📂 `phase-6-monitoring/`

- CloudTrail trails and log delivery
- CloudWatch logs, metrics, alarms, dashboards
- AWS Config rules and compliance baselines
- GuardDuty, Security Hub, Inspector setup
- Trusted Advisor usage
- Custom Lambda alerts (future phase)

---

### 🔧 Infrastructure as Code (IaC)

📂 `iac/`

- Terraform module structure
- Plan → Apply → Destroy flow
- Secrets handling
- Multi-phase automation pipeline
- Links back into each phase folder’s IaC modules

---

### 🧾 Audit & Documentation

📂 `docs/`, 📸 `screenshots-audit/`

- Screenshot proof for every AWS config step
- Time-stamped billing/usage audits
- Diagrams: VPC, IAM hierarchy, flowcharts
- Playbooks:
  - IAM setup
  - EC2 deployment
  - S3 hardening
  - Detection & response patterns

---

> **“Build deliberately. Harden everything. Automate where it hurts.”**  
> — Mr. Hayt
