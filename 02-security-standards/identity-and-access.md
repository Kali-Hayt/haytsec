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

## 🔐 MFA Devices

- ✅ iPhone Passkey (Apple Face ID / Safari integration)
- ✅ Google Account (WebAuthn-based Passkey or Chrome Authenticator)
- Backup: Redundant access via multiple devices
- Verified in AWS Console as “MFA assigned”

## 🌍 Region Context

- **CLI Region:** `us-west-2` (Oregon)
- **Console Region:** Set to match CLI for consistency
- **IAM Scope:** Global (not region-specific)
- **Infra Deployment Target:** `us-west-2` for core services
