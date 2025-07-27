# AWS Billing Overview

This document captures the current state of billing configurations for the HaytSec AWS root account.

---

## 🧾 AWS Billing Setup

- 📅 **Billing Alerts**: ✅ Enabled using **Zero Spend Budget**  
  - 🔔 Trigger: Spend exceeds **$1.00**
  - 🔐 Alert Email: Matches root email (JohnHayt@gmail.com)
- 📈 **Budget Name**: `My Zero-Spend Budget`
- 🧠 **Notes**:
  - Zero Spend Budget is great for **early warning** during AWS exploration.
  - Will adjust thresholds when real workloads start.

---

## ✅ Cost Explorer

- 📅 Enabled on: July 26, 2025
- 📊 Current Spend: $0.00
- 🔄 Will update after 24 hours of usage tracking
- 🧪 Will use this for:
  - Visualizing EC2/S3/NAT charges
  - Testing budget alerts
  - Verifying free-tier usage


---

## 💳 Payment Info

- 🔐 Card used: **Primary credit card**
- 🧾 Invoices: Accessible via the AWS Billing Dashboard
- 🧰 Tools available:
  - Billing Dashboard
  - Budgets
  - Reports
  - Free Tier Tracker

---

## ✅ Billing Audit Checklist

- ✅ Budget Alert — alert created ($1.00 zero-spend)
- ✅ Billing Summary — screenshot saved
- ✅ Cost Explorer — enabled (July 26, 2025)
- ✅ Free Tier page — screenshot saved
- ✅ Payment Method — screenshot saved
- ✅ MFA on Root — passkey registered (July 26, 2025)
- ✅ Monthly Report — activated (legacy CSV)
- ✅ Cost Allocation Report — activated


---
## 🔐 IAM Billing Access

- [2025-07-27] Enabled IAM user access to billing dashboard (configured from root)
- Verified that `haytsec-admin` can access Billing, Budgets, and Cost Explorer
- This allows non-root IAM users to manage budgets and reports during normal operations
---
## 📦 S3 Billing Logs

- [2025-07-27] Created dedicated bucket `haytsec-billing-logs` (region: `us-west-2`)
- Verified bucket accessibility with `aws-programmatic-access-test-object`
- Enabled legacy monthly and cost allocation reports
- Applied default bucket policy for `billingreports.amazonaws.com`
- AWS will begin delivering CSV logs starting **next billing cycle**
- 📸 See monthly delivery logs: `HaytSec/98-system-logs/aws-billing-screenshots/YYYY-MM`

✅ Billing logs pipeline configured  
⬜ Monitor for first CSV delivery

---



## Tags

#aws/billing  
#aws/account-setup  
#haytsec/docs  
#phase-1  
#budget-alerts  
#free-tier  
#security/mfa  
#todo/setup
