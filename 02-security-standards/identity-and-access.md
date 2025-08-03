# Identity & Access – Phase 1

## 🔐 IAM Strategy Overview
- Root locked down with Passkey + Authenticator MFA
- Least privilege principle applied from start
- Admin and auditor roles defined clearly
- CLI access restricted to trusted workstation (Kali-Hayt)

---

## 👤 IAM Users

### `haytsec-admin`
- 🔧 Full administrative permissions via `AdministratorAccess`
- 🔐 MFA: ✅ Enabled
- 🖥️ Console access: ✅
- 📟 CLI access: ✅ (configured with `aws configure`)
- 🧪 Identity verified via `aws sts get-caller-identity`
- 📍 Login from: Kali-Hayt workstation only

### `haytsec-auditor`
- 👁️‍🗨️ Read-only audit role
- 👥 Group: `read-only-group`
- 🔐 Policy: AWS-managed `ReadOnlyAccess`
- 🔐 MFA: ❌ Not enforced (by design – read-only S3 access via bucket policy)
- 🖥️ Console access: ✅
- 📟 CLI access: ❌ Disabled
- 🔒 No IAM permissions beyond read-only

---

## 🧾 MFA Summary
- ✅ Root account: Passkey + Authenticator App
- ✅ haytsec-admin: Passkey + Authenticator
- ❌ haytsec-auditor: Not required (read-only)

---

## 📋 IAM Policies
- ✅ `ReadOnlyAccess` (AWS managed)
- ⚠️ `AdministratorAccess` temporarily assigned (to be replaced)
- ⏳ Custom least-privilege policies under review for Phase 2

---

## 🧠 Lessons & Notes
- CLI must be locked to secure endpoints (no CLI for auditors)
- IAM user creation must follow documented naming convention
- MFA enforcement = mandatory for privilege roles
- Policy scoping to be refined post Phase 2 network setup

---

#aws/iam  
#security/access  
#mfa  
#identity  
#phase-1  
#haytsec/docs
