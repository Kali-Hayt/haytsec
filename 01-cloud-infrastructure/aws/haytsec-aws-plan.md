# HaytSec AWS Infrastructure Plan
#haytsec #aws #plan #phases #cloud-infra

## Overview
This plan outlines the phased buildout of HaytSec’s secure AWS cloud infrastructure. Each phase represents a milestone with goals, outputs, and documentation.

---

## Phase 0 – Primer & Systems Prep
✅ Local tools ready (CLI, git, GPG, MFA apps)  
✅ Account strategy and region policy defined  
✅ Obsidian vault structured and synced

🔗 Related: `phase-0-primer.md`

---

## Phase 1 – Account & Billing Foundation
✅ Root MFA + email lock  
✅ Budget alert at $1.00 cap  
✅ Cost Explorer enabled (via console + CLI)  
✅ IAM admin created (`haytsec-admin`) with MFA  
✅ CLI configured and tested (Kali-Hayt)  
🧭 Region selected: us-west-2 (CLI + console aligned)  
🔒 Root account locked for daily use

- [[aws/phase-1-account]]
- [[security-standards/identity-and-access]]
- [[aws/phase-1-next-actions]]
- [[2025-07-26-iam-cli-setup]]

---

## Phase 2 – Networking & Zones
🚧 Define core VPC layout (single-region)  
🚧 Public/private subnet strategy  
🚧 NACLs vs SGs baseline  
🚧 Route tables and IGW/NAT

🔗 Future: `phase-2-networking.md`

---

## Phase 3 – Identity & Access Hardening
🚧 Create roles, groups, policies for least privilege  
🚧 Start automation for access key rotation  
🚧 Enable CloudTrail logging + config rules

🔗 Future: `phase-3-security.md`

---

## Phase 4 – Compute & Services
🚧 Test EC2 launch in private subnet  
🚧 Begin automation / shell access via SSM  
🚧 ECS container preview

🔗 Future: `phase-4-compute.md`

---

## Phase 5 – Storage & Data Controls
🚧 S3 bucket policies + versioning  
🚧 Encrypt by default (KMS)  
🚧 IAM + bucket ACL governance

🔗 Future: `phase-5-storage.md`

---

## Phase 6 – Monitoring & Alerts
🚧 CloudWatch alarms + budget triggers  
🚧 GuardDuty, Config, Security Hub trial  
🚧 First threat detection scenario

🔗 Future: `phase-6-monitoring.md`

---

## Long-Term Tracks
- IaC: Terraform or CDK integration  
- Multi-account via AWS Organizations  
- Incident simulation + automated response  
- External logging to SIEM  
- Compliance mapping (NIST, CIS, SOC2-lite)

---

## Tags
#aws-plan #haytsec #infrastructure #phases #todo
