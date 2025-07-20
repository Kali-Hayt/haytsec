# Phase 0 – HaytSec Cloud Primer 🌩️

This primer defines the assumptions, tools, systems, and prep work required before starting AWS configuration.

---

## 🧠 Project Intent

- Build a secure AWS lab from scratch for training and automation.
- Document everything as if it were a real security engineering team playbook.
- Use phases to control complexity and introduce services gradually.

---

## 💻 Systems Used

| Machine | OS                      | Purpose                         |
| ------- | ----------------------- | ------------------------------- |
| Dell    | Windows 11 (WSL)        | Primary for AWS CLI, automation |
| MacBook | Kali Linux (bare metal) | Secondary + Testing             |

---

## 🛠️ Tools Installed

- [ ] `awscli` (AWS CLI v2)
- [ ] `curl`, `wget`, `jq`
- [ ] `git`
- [ ] GPG + file encryption for secrets
- [ ] Obsidian for documentation (`.md`)
- [ ] MFA app (Auth / Google Authenticator)

---

## 🌎 AWS Region Strategy

- Default region: `us-west-2` (Oregon)
- Secondary: `us-east-1` (N. Virginia) — for global services

---

## 📦 Account Planning

- Root account with MFA + budget alerts
- IAM admin (`haytsec-admin`) for all AWS actions
- Future: Organization setup for multi-account testing

---

## 📁 Vault Folder Guide (this repo)

- `01-cloud-infrastructure/` → Full AWS infra plan
- `docs/` → Explanations and policy walkthroughs
- `iac/` → Terraform/scripts (future)
- `security-standards/` → Your internal baseline and goals

---

## 🧾 Billing Controls (Phase 1 preview)

- Budget set: ✅ `$1.00` zero-spend
- Alerts: Email + root protection
- Free Tier watching: RDS, NAT, Elastic IP

---

## 📌 Tags

`#aws/primer` `#haytsec/docs` `#phase-0` `#todo/setup`

---

## 📝 Notes

- This vault is designed to scale with HaytSec.
- Security-first, even in test environments.
- All configs traceable to markdown source.

🔗 Back to [AWS Plan](./haytsec-aws-plan.md)
