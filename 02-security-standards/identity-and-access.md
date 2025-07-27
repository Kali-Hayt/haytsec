#haytsec #aws #identity #iam #phase-1 #security-standards #mfa #access-control
# HaytSec Identity & Access Standards

## Guiding Principles
- MFA enforced everywhere
- No root usage except for emergencies
- Break-glass access documented + time-limited

## User Types
- `haytsec-admin`: Admin user, full access (temp)
- `haytsec-auditor`: Read-only role for logging and review
- Root account: Locked down with passkey, alerts enabled

## MFA Policy
- All IAM users must enable MFA within 24 hours of creation
- Supported types: Authenticator apps, security keys (preferred)

---
## haytsec-admin Setup Log

- Created: July 26, 2025  
- User Type: IAM user (console + CLI access)  
- Permissions: AdministratorAccess (temporary)  
- Tags:  
  - created-by: root  
  - role: admin-user  
  - phase: 1  
  - env: bootstrap  
- Access Keys: ✅ Generated  
- CLI Region: us-west-2  
- CLI Verified With: `aws sts get-caller-identity`
---
## haytsec-auditor Setup Log

- Created: July 27, 2025  
- User Type: IAM user (console access only)  
- Group: `read-only-group`  
- Permissions: `ReadOnlyAccess` (AWS managed policy)  
- Tags:  
  - created-by: haytsec-admin  
  - role: audit-user  
  - phase: 1  
- MFA: ❌ Not required (read-only role)
- CLI Access: ❌ Not provisioned (by design)
---
## 🔐 MFA Devices

- ✅ iPhone Passkey (Apple Face ID / Safari integration)
- ✅ Google Account (WebAuthn-based Passkey or Chrome Authenticator)
- Backup: Redundant access via multiple devices
- Verified in AWS Console as “MFA assigned”
---
## 🌍 Region Context

- **CLI Region:** `us-west-2` (Oregon)
- **Console Region:** Set to match CLI for consistency
- **IAM Scope:** Global (not region-specific)
- **Infra Deployment Target:** `us-west-2` for core services
---
### [2025-07-27] Billing Access for IAM Users

- Enabled IAM user access to billing dashboard (via root)
- Verified `haytsec-admin` can now access billing & cost data
- Documented in billing.md