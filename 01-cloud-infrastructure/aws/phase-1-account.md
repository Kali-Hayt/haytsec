# AWS Phase 1 – Account & Identity Setup

## 🧾 AWS Root Account Setup
- 📧 Email: JohnHayt@gmail.com (used for root)
- 📱 MFA: ✅ Enabled (iOS Passkey & Google Authenticator)
- 🔒 Billing alerts set: ✅ Yes
- 💳 Card used: ✅ Primary card on file

## 🧍 IAM User & Groups
- 👤 Created IAM user: `haytsec-admin`
- 🔐 Attached Policy: `AdministratorAccess` (temporary, will reduce later)
- 🔒 MFA for IAM user: ✅ Enabled (Passkey + Authenticator backup)
- ✅ Root account now restricted from daily usage

## 📜 Budget & Billing Controls
- 🎯 Budget alert: ✅ Set to **$1 (zero-spend budget)**
- 📊 Cost Explorer: ✅ Enabled + tested via CLI
- 💡 Free Tier alerts: 📌 Planned

## 🌍 Region & CLI Setup
- 🌎 Default Region: `us-west-2` (Oregon)
- 💻 AWS CLI installed on Kali-Hayt: ✅ Installed and working
- 🔑 Access keys: ✅ Created and configured using `aws configure`
- 🧪 Verified via: `aws sts get-caller-identity`

## 📝 Notes
- Free tier covers EC2 (750hrs/month t2.micro), S3 (5GB), Lambda, etc.
- ⚠️ Watch services like NAT Gateway, RDS, and Elastic IPs for surprise charges
- IAM security baseline complete for Phase 1

---

#aws/account-setup  
#security/mfa  
#aws/billing  
#budget-alerts  
#phase-1  
#haytsec/docs  
#todo/setup  

