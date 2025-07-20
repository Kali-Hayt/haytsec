# ☁️ HaytSec AWS Infrastructure Plan

This document defines the complete AWS build lifecycle for HaytSec.  
Each phase matches a vault folder under `01-cloud-infrastructure/aws/`.  
All phases emphasize hardened security, automation potential, and long-term auditability.

> 🔒 “Build deliberately. Harden everything. Automate where it hurts.” — Mr. Hayt

---

## 🧰 Phase 0 – Primer & Tooling

📂 Folder: [`./phase-0-primer/`](./phase-0-primer/)

- Define architecture goals and training intent
- Set regions: `us-west-2` primary, `us-east-1` for global
- Prep local systems (CLI, secrets, MFA, vault structure)
- Decide on account design and IAM admin names
- Setup tagging conventions and vault structure
- 🔗 Related: [`docs/billing/`](./docs/billing/), `iac/README.md` (future)

---

## 🛫 Phase 1 – Account & Billing Foundation

📂 Folder: [`./phase-1-account/`](./phase-1-account/)  
📸 Audit: [`./screenshots-audit/`](./screenshots-audit/)  
📑 Docs: [`./docs/billing/`](./docs/billing/)

- Root MFA + email lock
- Budget alert at $1.00 cap
- Billing alarm notifications
- Enable Cost Explorer + usage reports
- Begin AWS Organizations & SCP exploration (future)

---

## 🌐 Phase 2 – Networking Foundation

📂 Folder: [`./phase-2-networking/`](./phase-2-networking/)

- VPC creation with CIDR split
- Subnets: public vs. private
- Route tables per zone
- IGW + NAT Gateway
- Elastic IPs, DHCP, DNS options
- Network ACLs vs. SGs planning

---

## 🔐 Phase 3 – IAM & Security Services

📂 Folder: [`./phase-3-security/`](./phase-3-security/)

- IAM groups: Admin, Automation, Audit
- Roles and policies with least privilege
- Enforce MFA and session duration
- CloudTrail global trail + log bucket
- AWS Config + resource recorder
- KMS key setup (S3, EBS encryption)
- Secrets Manager usage patterns
- SCP policy drafts (if org used)

---

## 🖥️ Phase 4 – Compute Layer

📂 Folder: [`./phase-4-compute/`](./phase-4-compute/)

- Hardened AMIs (public or custom)
- Launch templates for EC2
- Bastion host with IP restrictions
- Security Group templates per tier
- Auto scaling group prototypes
- Cloud-init or bootstrap scripts
- Compute tagging conventions

---

## 📦 Phase 5 – Storage Architecture

📂 Folder: [`./phase-5-storage/`](./phase-5-storage/)

- S3 versioning, encryption (SSE-KMS)
- Bucket policies and ACL lockdown
- Lifecycle rules: IA, Glacier, delete
- Block public access (org level + bucket)
- Storage logging (CloudTrail, S3 access logs)
- Early research: EFS, RDS, Backups

---

## 📊 Phase 6 – Monitoring & Audit Stack

📂 Folder: [`./phase-6-monitoring/`](./phase-6-monitoring/)

- CloudTrail across all regions
- CloudWatch logs, alarms, metrics
- CloudWatch dashboards
- AWS Config rules (custom + managed)
- Enable:
  - GuardDuty
  - Security Hub
  - AWS Inspector
- Trusted Advisor audit script

---

## 🛠️ Infrastructure-as-Code (IaC)

📂 Folder: [`./iac/`](./iac/)

- Terraform module layout
- Phase-based module execution
- State file handling plan
- Secrets strategy (env vars, tfvars, encrypted files)
- Runbooks: `plan`, `apply`, `destroy`
- Future: GitHub Actions or Lambda for CICD

---

## 🧾 Supporting Docs

📂 Docs: [`./docs/`](./docs/)  
📸 Screenshots: [`./screenshots-audit/`](./screenshots-audit/)

- Markdown-based guides per service
- SCP templates and policy references
- IAM strategy docs
- Diagrams (draw.io, lucidchart exports)
- Playbooks for red/blue team, hardening checklists

---

## 📌 Tags

`#haytsec` `#aws` `#cloud` `#build-plan` `#phase-map`

---

🔗 Return to: [`Phase 0 Primer`](./phase-0-primer.md)
