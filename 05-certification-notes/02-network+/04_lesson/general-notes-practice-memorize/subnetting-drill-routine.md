## CIDR Quick Bits 🧱

- /8   → 255.0.0.0       → 16,777,214 hosts
- /16  → 255.255.0.0     → 65,534 hosts
- /24  → 255.255.255.0   → 254 hosts
- /25  → 255.255.255.128 → 126 hosts
- /26  → 255.255.255.192 → 62 hosts
- /30  → 255.255.255.252 → 2 usable hosts

## Binary Weight Table 🧮

| Bit Position | Weight |
|--------------|--------|
| 1st bit      | 128    |
| 2nd bit      | 64     |
| 3rd bit      | 32     |
| 4th bit      | 16     |
| 5th bit      | 8      |
| 6th bit      | 4      |
| 7th bit      | 2      |
| 8th bit      | 1      |

## Example: /26 (Block Size 64)

Subnet mask in binary:
11111111.11111111.11111111.11000000

Decimal mask:
255.255.255.192

IP blocks (4 subnets of 64 each):
- 192.168.1.0 → 192.168.1.63
- 192.168.1.64 → 192.168.1.127
- 192.168.1.128 → 192.168.1.191
- 192.168.1.192 → 192.168.1.255

## Broadcast & Gateway 🎯

For 192.168.1.64/26:
- Network: 192.168.1.64
- First usable: 192.168.1.65
- Last usable: 192.168.1.126
- Broadcast: 192.168.1.127

