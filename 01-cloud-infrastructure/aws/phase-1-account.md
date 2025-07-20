# AWS Phase 1 – Account & Identity Setup

## 🧾 AWS Root Account Setup
- 📧 Email: JohnHayt@gmail.com (used for root)
- 📱 MFA: Enabled via [authenticator app or hardware]
- 🔒 Billing alerts set:  ✅ Yes
- 💳 Card used: primary card 

## 🧍 IAM User & Groups
- 👤 Created IAM user: `haytsec-admin`
- 🔐 Attached Policy: `AdministratorAccess` (temporary, will reduce later)
- ⚠️ MFA for IAM user: **Not yet enabled**
- ⛔ Root account still used for now — **daily-use lockout not implemented yet**


## 📜 Budget & Billing Controls
- 🎯 Budget alert: set to **$1 (zero-spend budget)**
- 🕒 Cost Explorer pending: initializing (24-hour wait after first visit)
- 💡 Set up Free Tier alerts


## 🌍 Region & CLI Setup
- 🌎 Default Region: `us-west-2` (Oregon)
- 💻 AWS CLI installed on Kali-Hayt: ❌ Not yet installed
- 🔑 Access keys: ❌ Not yet generated or configured in `.aws/credentials`


## 📝 Notes
- Free tier covers EC2 (750hrs/month t2.micro), S3 (5GB), Lambda, etc.
- Watch out: NAT Gateway, RDS, and elastic IPs = 💸 quick charges

#aws/account-setup  
#security/mfa  
#aws/billing  
#budget-alerts  
#phase-1  
#haytsec/docs  
#todo/setup 

🔗 Back to [AWS Plan](./haytsec-aws-plan.md)
