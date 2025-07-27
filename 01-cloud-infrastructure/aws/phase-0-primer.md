# 🧪 Phase 0: Local Environment & CLI Setup

This primer documents the tools and environment setup for HaytSec prior to launching AWS infrastructure. Focus is on preparing CLI access, vault structure, and secure practices.

---

## 🛠️ Tools Installed
- ✅ `awscli` (AWS CLI v2) – configured for `haytsec-admin` on Kali-Hayt  
- ✅ `curl`, `wget`, `jq` – basic network tools for CLI + JSON  
- ✅ `git` – version control for docs and scripts  
- [ ] GPG + file encryption tools for secure secret storage  
- ✅ Obsidian – `.md` vault for documentation  
- ✅ MFA app – iOS Authenticator (Google/Apple)  

---

## 🧪 CLI Setup Validation

```bash
aws configure
aws sts get-caller-identity
```

- Configured profile: `haytsec-admin`  
- Region: `us-west-2`  
- CLI access: ✅ Verified  
- Access key scope: CLI-only  

---

## 🔐 Local Vault Path

- Primary vault location: `/mnt/c/Users/John Hayt/Desktop/HaytSec`  
- CLI files and logs organized under: `01-cloud-infrastructure/aws/`  
- Logs: `98-system-logs/`, `99-personal-logs/`  

---

## 📁 Structure Confirmed

- Folder tree verified via `tree -L 3` in Kali-Hayt WSL  
- Separate folders for infrastructure, standards, scripts, logs, and certifications  
- Markdown-based note-taking system actively in use  
