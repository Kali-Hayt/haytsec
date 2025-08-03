# 🧱 Phase 2 – Build Status Tracker

Use this file to track which Phase 2 components are still **planned**, which are **optional**, and which have been **implemented and verified**.

---

## 🔧 Planned (Not Yet Built)

| Component       | Status   | Notes                            |
|----------------|----------|----------------------------------|
| VPC            | 🟡 Planned  | Custom CIDR `10.0.0.0/16`         |
| Subnets        | 🟡 Planned  | Public + Private in 2 AZs        |
| NAT Gateway    | ⏳ Optional | Needed for private egress         |
| Route Tables   | 🟡 Planned  | Split routing: public/private    |
| Internet GW    | 🟡 Planned  | Attach to public subnets         |
| S3 Endpoints   | 🟡 Planned  | Billing/logs access in private   |
| SGs + NACLs    | 🟡 Planned  | Scoped per role: web, db, bastion|
| Bastion Host   | ⏳ Optional | Or use Systems Manager Session   |
| Route 53 / DNS | 🔒 Later   | Not in scope yet                 |
| VPC Flow Logs  | 🟡 Planned  | Target: CloudWatch or S3         |

---

## ✅ Implemented

| Component     | Date         | Verified By     |
|--------------|--------------|-----------------|
| *(none yet)* | —            | —               |

---

## 📌 Notes

- This tracker is updated **after** builds are deployed
- For step-by-step tasks and CLI commands, see `phase-2-networking.md`
- You can copy entries from “Planned” to “Implemented” as you progress
- Keep screenshots, CLI output, or S3 URIs for audit trail

---

#phase-2  
#aws/networking  
#haytsec/docs  
#tracking  
#todo
