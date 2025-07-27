## 🧾 CloudTrail Setup - HaytSec

### Trail Configuration
- **Trail name:** `haytsec-orgtrail`
- **Trail type:** Multi-region
- **Region:** `us-west-2 (Oregon)`
- **Organization trail:** No (this is an account trail)
- **Log destination:** S3 bucket `haytsec-billing-logs`
- **Prefix:** *(none set)*

---

### 🔐 Encryption
- **Encryption type:** SSE-KMS (enabled)
- **KMS Key alias:** `alias/haytsec-cloudtrail-key`

#### Key Permissions:
- ✅ `cloudtrail.amazonaws.com` allowed to:
  - `kms:GenerateDataKey*`
  - `kms:Decrypt`
  - `kms:DescribeKey`
- ✅ Root user and `haytsec-admin` have full access (`kms:*`)
- ✅ Conditions restrict decryption to CloudTrail context

---

### ✅ Status Check
- Logging: **Enabled**
- Verified S3 folders:
  - `AWSLogs/636768525341/CloudTrail/`
  - `AWSLogs/636768525341/CloudTrail-Digest/`

---

### 📄 KMS Key Policy

```json
{
  "Version": "2012-10-17",
  "Id": "Key policy created by CloudTrail",
  "Statement": [
    {
      "Sid": "Enable IAM User Permissions",
      "Effect": "Allow",
      "Principal": {
        "AWS": [
          "arn:aws:iam::636768525341:user/haytsec-admin",
          "arn:aws:iam::636768525341:root"
        ]
      },
      "Action": "kms:*",
      "Resource": "*"
    },
    {
      "Sid": "Allow CloudTrail to encrypt logs",
      "Effect": "Allow",
      "Principal": {
        "Service": "cloudtrail.amazonaws.com"
      },
      "Action": [
        "kms:GenerateDataKey*",
        "kms:Decrypt"
      ],
      "Resource": "*",
      "Condition": {
        "StringEquals": {
          "kms:EncryptionContext:aws:cloudtrail:arn": "arn:aws:cloudtrail:us-west-2:636768525341:trail/haytsec-orgtrail"
        }
      }
    },
    {
      "Sid": "Allow CloudTrail to describe key",
      "Effect": "Allow",
      "Principal": {
        "Service": "cloudtrail.amazonaws.com"
      },
      "Action": "kms:DescribeKey",
      "Resource": "*"
    },
    {
      "Sid": "Allow principals in the account to decrypt log files",
      "Effect": "Allow",
      "Principal": {
        "AWS": "*"
      },
      "Action": [
        "kms:Decrypt",
        "kms:ReEncryptFrom"
      ],
      "Resource": "*",
      "Condition": {
        "StringEquals": {
          "kms:CallerAccount": "636768525341"
        },
        "StringLike": {
          "kms:EncryptionContext:aws:cloudtrail:arn": "arn:aws:cloudtrail:*:636768525341:trail/*"
        }
      }
    },
    {
      "Sid": "Enable cross account log decryption",
      "Effect": "Allow",
      "Principal": {
        "AWS": "*"
      },
      "Action": [
        "kms:Decrypt",
        "kms:ReEncryptFrom"
      ],
      "Resource": "*",
      "Condition": {
        "StringEquals": {
          "kms:CallerAccount": "636768525341"
        },
        "StringLike": {
          "kms:EncryptionContext:aws:cloudtrail:arn": "arn:aws:cloudtrail:*:636768525341:trail/*"
        }
      }
    }
  ]
}
