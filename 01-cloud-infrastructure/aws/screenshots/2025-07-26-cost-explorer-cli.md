---
tags: [#billing, #audit/screenshot, #phase/1, #env/bootstrap]
title: Cost Explorer Verified (CLI)
created: 2025-07-26
created-by: haytsec-admin
related-phase: 1
summary: Output of `aws ce get-cost-and-usage` confirms Cost Explorer is enabled and working.
---

```json
{
    "ResultsByTime": [
        {
            "TimePeriod": {
                "Start": "2025-07-25",
                "End": "2025-07-26"
            },
            "Total": {
                "UnblendedCost": {
                    "Amount": "0",
                    "Unit": "USD"
                }
            },
            "Groups": [],
            "Estimated": true
        }
    ],
    "DimensionValueAttributes": []
}
```
