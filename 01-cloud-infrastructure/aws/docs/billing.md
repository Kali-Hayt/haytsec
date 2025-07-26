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

## ✅ Billing Audit Checklist Status

- [x] Budget Alert — alert created ($1.00 zero-spend)
- [x] Billing Summary — ✅ screenshot saved
- [x] Cost Explorer — ✅ enabled (July 26, 2025)
- [x] Free Tier page — ✅ screenshot saved
- [x] Payment Method — ✅ screenshot saved
- [x] MFA on Root — ✅ passkey registered (July 26, 2025)


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
