# Phase 1 – Next Actions for HaytSec
🗓️ Updated: July 26, 2025

This checklist captures the remaining critical tasks for completing Phase 1 (Account & Identity Setup) of the HaytSec AWS build.

---

## 🔐 Identity & Access

- [x] ✅ Enable MFA for IAM user `haytsec-admin`
- [x] ⛔️ Stop using root account for daily use
- [x] 🧪 Test login access for `haytsec-admin` with MFA enabled
- [x] ✅ Document MFA setup + recovery plan in `identity-and-access.md`
- [x] ✅ Add backup IAM user with `SecurityAudit` permissions
- [x] ✅ Log IAM changes in `identity-and-access.md`

---

## ⚙️ CLI & Credential Configuration

- [x] 💻 Install AWS CLI v2 on Kali-Hayt
- [x] 🔑 Generate access keys for `haytsec-admin`
- [x] 🧰 Run `aws configure` to bootstrap CLI profile
- [x] 🧪 Test basic command: `aws sts get-caller-identity`
- [x] 📄 Document CLI setup in `phase-0-primer.md`

---

## 💰 Billing & Monitoring

- [x] ~~📊 Enable **Cost Explorer** after 24-hour wait~~
- [x] ~~✅ CLI confirms Cost Explorer active (2025-07-26)~~
- [ ] 🛠️ Set up **usage reports** and daily spend tracking
- [ ] 📜 Update `billing.md` after Cost Explorer is active
- [ ] 🧪 Test budget alert with sandbox service (optional)

---

## 📝 Documentation Reminders

- [ ] 🧱 Create `incident-response-playbook.md` in `security-standards/`
- [x] ✅ Log IAM changes in `identity-and-access.md`
- [ ] 🪪 Record IAM user, MFA type, and access key fingerprint securely

---

## 🌎 Region Strategy

- [x] ~~✅ Select default AWS region for infrastructure~~
- [x] ~~Documented: `us-west-2` (primary), `us-east-1` (secondary)~~
- [ ] Bookmark Console region view: https://us-west-2.console.aws.amazon.com/
- [ ] Set region explicitly in Terraform or IaC config later

---

## Tags

#haytsec/docs  
#aws/account-setup  
#security/mfa  
#aws/billing  
#budget-alerts  
#phase-1  
#todo/setup
