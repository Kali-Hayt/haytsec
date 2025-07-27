# Phase 1 – Next Actions for HaytSec
🗓️ Updated: July 26, 2025

This checklist captures the remaining critical tasks for completing Phase 1 (Account & Identity Setup) of the HaytSec AWS build.

---

## 🔐 Identity & Access

- ✅ Enable MFA for IAM user `haytsec-admin`
- ✅ Stop using root account for daily use
- ✅ Test login access for `haytsec-admin` with MFA enabled
- ✅ Document MFA setup + recovery plan in `identity-and-access.md`
- ✅ Add backup IAM user with `SecurityAudit` permissions
- ✅ Log IAM changes in `identity-and-access.md`
- ✅ **Create `haytsec-auditor` IAM user with `ReadOnlyAccess` policy**
- ✅ **Log `haytsec-auditor` setup** in `identity-and-access.md`
- ✅ **Document IAM changes** in `phase-1-account.md`
---

## ⚙️ CLI & Credential Configuration

- ✅ Install AWS CLI v2 on Kali-Hayt
- ✅ Generate access keys for `haytsec-admin`
- ✅ Run `aws configure` to bootstrap CLI profile
- ✅ Test basic command: `aws sts get-caller-identity`
- ✅ Document CLI setup in `phase-0-primer.md`

---

## 💰 Billing & Monitoring

- ✅ Enable Cost Explorer after 24-hour wait
- ✅ CLI confirms Cost Explorer active (2025-07-26)
- ✅ Set up **usage reports** and daily spend tracking
- ✅ Update `billing.md` after Cost Explorer is active
- ✅ Test budget alert with sandbox service (optional)

---
## 📝 Documentation Reminders

- 🔲 Create `incident-response-playbook.md` in `security-standards/`
- ✅ Log IAM changes in `identity-and-access.md`
- ✅ Record IAM user, MFA type, and access key fingerprint securely

---

## 🌎 Region Strategy

- ✅ Select default AWS region for infrastructure
- ✅ Documented: `us-west-2` (primary), `us-east-1` (secondary)
- 🔲 Bookmark Console region view: https://us-west-2.console.aws.amazon.com/
- 🔲 Set region explicitly in Terraform or IaC config later

---
## 📜 Logging Setup – Phase 1

✅ Create dedicated S3 bucket for CloudTrail logs (e.g., `haytsec-cloudtrail-logs`)
✅Enable CloudTrail in all regions (management events, read/write)
✅ Configure log delivery to S3 bucket  
  └── ✅Use SSE encryption and restrict public access
- [ ] Enable log file validation (integrity hashes)
- [ ] Restrict access to log bucket using IAM policies  
  └── Only allow `haytsec-auditor` or designated log readers
- [ ] Test logging by signing in and checking for events in the S3 bucket
- [ ] Document logging setup in `identity-and-access.md` or `logging.md`


---
## Tags

#haytsec/docs  
#aws/account-setup  
#security/mfa  
#aws/billing  
#budget-alerts  
#phase-1  
#todo/setup
