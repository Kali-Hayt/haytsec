# 2025-07-26 – IAM User & CLI Bootstrap Log

## 👤 IAM User: haytsec-admin

- Created via root account using AWS Console
- Username: `haytsec-admin`
- Console access: ✅ Enabled (custom password)
- Programmatic access: ✅ Enabled
- Permissions: `AdministratorAccess` (temporary)
- Tags:
  - created-by: root
  - role: admin-user
  - env: bootstrap
  - phase: 1

---

## 🔐 Access Key Setup

- Access key generated for `haytsec-admin`
- Stored securely in Firefox password manager (user-managed)
- Used for CLI bootstrap

---

## 💻 CLI Configuration (Kali-Hayt via WSL)

- AWS CLI v2 installed
- Region: `us-west-2`
- Output format: `json`
- Configured using `aws configure`
- Verified identity with:

```bash
aws sts get-caller-identity
```

✅ Output showed correct IAM user ARN and account ID.

---

## 📝 Notes

- Root account no longer used for CLI access
- MFA for `haytsec-admin` is still pending
- Next: Document setup in `identity-and-access.md`, then enable MFA
