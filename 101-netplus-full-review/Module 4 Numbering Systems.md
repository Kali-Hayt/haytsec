## 🔢 Binary Place Values (Network Numbering Systems)

Binary place values increase by **powers of 2** from right → left.

| Bit Position (Right→Left) | Exponent | 2^Exponent | Decimal Value |
|---------------------------|----------|------------|---------------|
| 1 (rightmost)             | 0        | 2⁰         | 1             |
| 2                         | 1        | 2¹         | 2             |
| 3                         | 2        | 2²         | 4             |
| 4                         | 3        | 2³         | 8             |
| 5                         | 4        | 2⁴         | 16            |
| 6                         | 5        | 2⁵         | 32            |
| 7                         | 6        | 2⁶         | 64            |
| 8 (leftmost in octet)     | 7        | 2⁷         | 128           |

**Full Octet Range:** 0 → 255 (256 total values)

---

### 💡 Quick Binary → Decimal Conversion
Example: `10101100`

1. Write place values above bits: **128 64 32 16 8 4 2 1**  
2. Multiply each place value by the bit (0 or 1):  
   - 1×128 = 128  
   - 0×64 = 0  
   - 1×32 = 32  
   - 0×16 = 0  
   - 1×8 = 8  
   - 1×4 = 4  
   - 0×2 = 0  
   - 0×1 = 0  
3. Add: 128 + 0 + 32 + 0 + 8 + 4 + 0 + 0 = **172**

Result: `10101100` (binary) = **172** (decimal)

---
  ## 🔄 Decimal → Binary Conversion (8-bit Example)

**Example:** Convert 172 (decimal) to binary.

### Step-by-step:
1. Write binary place values: **128 64 32 16 8 4 2 1**
2. Start with the largest value ≤ 172:
   - 128 fits → write **1** in that column.
   - Subtract 128 from 172 → remainder = 44.
3. Next value (64) is greater than remainder → write **0**.
4. Next value (32) fits → write **1**.  
   - Subtract 32 → remainder = 12.
5. Next value (16) is greater than remainder → write **0**.
6. Next value (8) fits → write **1**.  
   - Subtract 8 → remainder = 4.
7. Next value (4) fits → write **1**.  
   - Subtract 4 → remainder = 0.
8. Remaining columns → write **0**.

**Result:**  
172 (decimal) = `10101100` (binary)

---

### Quick Tips:
- Always start from the **largest place value** and work down.
- In subnetting, work with 8 bits per octet.
- Remainder method avoids mistakes compared to guessing.
---
## 💡 Special Case: 255 in Binary

- **Decimal 255** = `11111111` (binary)
- 8 bits all set to 1 → every place value used:
  - 128 + 64 + 32 + 16 + 8 + 4 + 2 + 1 = 255
- In IPv4 subnet masks, `255` means **all network bits** in that octet.

**Examples:**
- `/8` → 255.0.0.0  
- `/16` → 255.255.0.0  
- `/24` → 255.255.255.0
---
## 🧱 CIDR to Subnet Mask Reference

| CIDR | Binary Mask                                | Decimal Mask        | Host Bits | Usable Hosts* |
|------|--------------------------------------------|---------------------|-----------|---------------|
| /0   | 00000000.00000000.00000000.00000000        | 0.0.0.0             | 32        | 4,294,967,294 |
| /1   | 10000000.00000000.00000000.00000000        | 128.0.0.0           | 31        | 2,147,483,646 |
| /2   | 11000000.00000000.00000000.00000000        | 192.0.0.0           | 30        | 1,073,741,822 |
| /3   | 11100000.00000000.00000000.00000000        | 224.0.0.0           | 29        | 536,870,910   |
| /4   | 11110000.00000000.00000000.00000000        | 240.0.0.0           | 28        | 268,435,454   |
| /5   | 11111000.00000000.00000000.00000000        | 248.0.0.0           | 27        | 134,217,726   |
| /6   | 11111100.00000000.00000000.00000000        | 252.0.0.0           | 26        | 67,108,862    |
| /7   | 11111110.00000000.00000000.00000000        | 254.0.0.0           | 25        | 33,554,430    |
| /8   | 11111111.00000000.00000000.00000000        | 255.0.0.0           | 24        | 16,777,214    |
| /9   | 11111111.10000000.00000000.00000000        | 255.128.0.0         | 23        | 8,388,606     |
| /10  | 11111111.11000000.00000000.00000000        | 255.192.0.0         | 22        | 4,194,302     |
| /11  | 11111111.11100000.00000000.00000000        | 255.224.0.0         | 21        | 2,097,150     |
| /12  | 11111111.11110000.00000000.00000000        | 255.240.0.0         | 20        | 1,048,574     |
| /13  | 11111111.11111000.00000000.00000000        | 255.248.0.0         | 19        | 524,286       |
| /14  | 11111111.11111100.00000000.00000000        | 255.252.0.0         | 18        | 262,142       |
| /15  | 11111111.11111110.00000000.00000000        | 255.254.0.0         | 17        | 131,070       |
| /16  | 11111111.11111111.00000000.00000000        | 255.255.0.0         | 16        | 65,534        |
| /17  | 11111111.11111111.10000000.00000000        | 255.255.128.0       | 15        | 32,766        |
| /18  | 11111111.11111111.11000000.00000000        | 255.255.192.0       | 14        | 16,382        |
| /19  | 11111111.11111111.11100000.00000000        | 255.255.224.0       | 13        | 8,190         |
| /20  | 11111111.11111111.11110000.00000000        | 255.255.240.0       | 12        | 4,094         |
| /21  | 11111111.11111111.11111000.00000000        | 255.255.248.0       | 11        | 2,046         |
| /22  | 11111111.11111111.11111100.00000000        | 255.255.252.0       | 10        | 1,022         |
| /23  | 11111111.11111111.11111110.00000000        | 255.255.254.0       | 9         | 510           |
| /24  | 11111111.11111111.11111111.00000000        | 255.255.255.0       | 8         | 254           |
| /25  | 11111111.11111111.11111111.10000000        | 255.255.255.128     | 7         | 126           |
| /26  | 11111111.11111111.11111111.11000000        | 255.255.255.192     | 6         | 62            |
| /27  | 11111111.11111111.11111111.11100000        | 255.255.255.224     | 5         | 30            |
| /28  | 11111111.11111111.11111111.11110000        | 255.255.255.240     | 4         | 14            |
| /29  | 11111111.11111111.11111111.11111000        | 255.255.255.248     | 3         | 6             |
| /30  | 11111111.11111111.11111111.11111100        | 255.255.255.252     | 2         | 2             |
| /31  | 11111111.11111111.11111111.11111110        | 255.255.255.254     | 1         | 0**           |
| /32  | 11111111.11111111.11111111.11111111        | 255.255.255.255     | 0         | 1***          |

\* Usable hosts excludes network & broadcast addresses.  
\** /31 is used for point-to-point links (no usable hosts in the normal sense).  
\*** /32 identifies exactly one host.

---
### 🧱 How the 8-4-2-1 Rule is Built

Hexadecimal uses **4-bit binary groups** (nibbles).  
Each bit position has a value based on **powers of 2**, starting from the rightmost bit.

**Right → Left:**
- 2⁰ = 1
- 2¹ = 2
- 2² = 4
- 2³ = 8

**Place Value Row:** `8 | 4 | 2 | 1`

**How to Convert Binary → Decimal in Hex:**
1. Write the place values (8, 4, 2, 1) above the 4-bit binary number.
2. For each **1** in binary, add the corresponding place value.
3. Skip values where the bit is **0**.

**Example:**
- Binary: `0110`
- Place values: 8 | 4 | 2 | 1
- Calculation: 0 + 4 + 2 + 0 = **6**
---
## 🔢 Hexadecimal (Base-16) Reference

### 🧱 Basics
- **Base:** 16 (values 0–15)
- **Digits:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
- **Why hex?**
  - Compact way to represent binary (1 hex digit = 4 binary bits)
  - Common in IPv6 addresses, MAC addresses, memory addresses

---

### 🔄 Hex ↔ Decimal ↔ Binary

| Hex | Decimal | Binary  |
|-----|---------|---------|
| 0   | 0       | 0000    |
| 1   | 1       | 0001    |
| 2   | 2       | 0010    |
| 3   | 3       | 0011    |
| 4   | 4       | 0100    |
| 5   | 5       | 0101    |
| 6   | 6       | 0110    |
| 7   | 7       | 0111    |
| 8   | 8       | 1000    |
| 9   | 9       | 1001    |
| A   | 10      | 1010    |
| B   | 11      | 1011    |
| C   | 12      | 1100    |
| D   | 13      | 1101    |
| E   | 14      | 1110    |
| F   | 15      | 1111    |

---

### 💡 Conversion Tricks

**Binary → Hex:**
1. Group binary bits into **4-bit chunks** (from right to left).
2. Convert each 4-bit group into its hex equivalent.

Example:  
`11010111` (binary) → group → `1101 0111` → `D7` (hex)

**Hex → Binary:**
- Replace each hex digit with its **4-bit binary equivalent**.

Example:  
`2F` (hex) → `0010 1111` (binary) → decimal = 47

---

### 📌 Common Uses of Hexadecimal

**IPv6 Addresses:**  
- Written in hex for compactness (1 hex digit = 4 bits).  
- Example: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
- Can be shortened: `2001:db8:85a3::8a2e:370:7334`

**MAC Addresses:**  
- 48-bit hardware addresses, shown as 12 hex digits (6 bytes).  
- Example: `00-1A-92-3F-5B-2C` or `00:1A:92:3F:5B:2C`  
- No direct connection to IPv6 unless using **EUI-64** autoconfig.

**Memory / Registers:**  
- Hex used in programming and debugging for memory values.  
- Example: `0xFF` = 255 decimal = `11111111` binary.

---

💡 **Why the exam cares:**  
- Hex is faster to read/write than long binary strings.  
- Essential for IPv6, MAC addressing, memory analysis, and network troubleshooting.

