# AWS Phase 1 – Account & Identity Setup

## 🧾 AWS Root Account Setup
- 📧 Email: JohnHayt@gmail.com (used for root)
- 📱 MFA: ✅ Enabled (iOS Passkey & Google Authenticator)
- 🔒 Billing alerts set: ✅ Zero-spend budget active ($1.00)
- 💳 Card used: ✅ Primary card on file

---

## 🧍 IAM Users & Access

### haytsec-admin (Primary Admin)
- 👤 IAM user with full console + CLI access
- 🔐 Permissions: `AdministratorAccess` (temporary — to be scoped down)
- 🔒 MFA: ✅ Enabled (Passkey + Authenticator backup)
- 🔑 CLI access configured via `aws configure` on Kali-Hayt
- 🧪 Verified via: `aws sts get-caller-identity`

### haytsec-auditor (Read-only Auditor)
- 👤 IAM user in group `read-only-group`
- 🔐 Permissions: `ReadOnlyAccess` (AWS managed)
- 🔒 Console login: ✅ Enabled
- 🔐 MFA: ❌ Not required (read-only)
- 🔒 CLI access: ❌ Disabled by design

---

## 💰 Billing & Budget Controls
- 🎯 Budget alert: ✅ $1.00 (Zero-spend)
- 📊 Cost Explorer: ✅ Enabled + tested via CLI
- 📄 Billing logs delivered to `haytsec-billing-logs` bucket
- 📁 Free Tier tracking active; alerts pending

---

## 🌍 Region Strategy
- 🌎 Default: `us-west-2` (Oregon)
- 🧭 Secondary: `us-east-1` (documented for DR planning)
- ✅ Region pinned in both CLI & Console views

---

## 🛡️ Logging Infrastructure
- ✅ CloudTrail trail `haytsec-orgtrail` enabled (multi-region)
- ✅ Logs delivered to: `haytsec-billing-logs/AWSLogs/...`
- ✅ SSE-KMS encryption with `alias/haytsec-cloudtrail-key`
- ✅ Log file validation enabled (digest chain confirmed)
- ✅ Digest delivery verified: `CloudTrail-Digest/`
- ✅ Access to logs restricted via bucket policy (auditor-only enforced)
- 📄 See `logging.md` for detailed logging setup

---

## 📝 Phase 1 Notes
- IAM security baseline established
- Budget enforcement and logging pipeline functional
- CLI bootstrapped on Kali-Hayt workstation
- All configurations versioned in Obsidian
- ⚠️ Caution: Monitor NAT Gateway & Elastic IP for cost leaks

---

#aws/account-setup  
#security/mfa  
#aws/billing  
#budget-alerts  
#logging  
#phase-1  
#haytsec/docs
