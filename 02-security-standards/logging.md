# 🛡️ Logging Standards – HaytSec

## Overview

This document outlines the CloudTrail logging setup for HaytSec's AWS infrastructure. It covers configuration, encryption, validation, delivery, and access control.

---

## 📜 CloudTrail Configuration

- **Trail Name**: `haytsec-orgtrail`
- **Scope**: Multi-region (all AWS regions)
- **Type**: Account trail (not org-wide)
- **Region**: `us-west-2` (Home Region)
- **S3 Bucket**: `haytsec-billing-logs`
- **Log Prefix**: `AWSLogs/636768525341/CloudTrail/`

---

## 🔐 Encryption & KMS

- **Encryption**: SSE-KMS
- **KMS Key**: `alias/haytsec-cloudtrail-key`
- **Key Permissions**:
  - `cloudtrail.amazonaws.com`: `GenerateDataKey*`, `Decrypt`, `DescribeKey`
  - `haytsec-admin`, root: `kms:*`
  - Decryption is restricted to valid CloudTrail encryption context

---

## ✅ Log File Validation

- **Enabled**: Yes
- **Digest Files Location**:  
  `haytsec-billing-logs/AWSLogs/636768525341/CloudTrail-Digest/`
- **Verification**: CLI and S3-confirmed
- **Use Case**: Audit integrity checks, incident response

---

## 📦 Delivery Status

- Logs confirmed in:  
  `AWSLogs/636768525341/CloudTrail/us-west-2/YYYY/MM/DD/`
- Digest files confirmed in:  
  `CloudTrail-Digest/`
- Billing CSVs present for monthly and allocation reports
- Last successful log: `2025-08-03T07:08:00Z` (verified)

---

## 🔒 S3 Access Control (Confirmed)

- ✅ `s3:GetObject` allowed only to:  
- `haytsec-auditor` IAM user
- ✅ All other access denied via explicit `Deny` in bucket policy
- ✅ CloudTrail `PutObject` remains unrestricted via `cloudtrail.amazonaws.com`

> ✅ Bucket policy applied 2025-08-03  
> ✅ Tested with `aws s3 ls` using both admin and auditor profiles

---

## 📁 Tagging & Structure

- Folder: `02-security-standards/`
- Tags: `#logging`, `#cloudtrail`, `#phase-1`, `#haytsec/docs`

---

## 📌 Notes

- CLI verified via `get-trail-status`, `describe-trails`, `list-objects`
- Event generation confirmed with test actions (EC2, IAM, S3)
- Digest files used to validate log integrity
- Consider scripting log validation with AWS CLI or Python for future audit automation
