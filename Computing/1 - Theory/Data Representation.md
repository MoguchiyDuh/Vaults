# Computer Data Representation

## Two's Complement Algorithm

In two's complement, the most significant bit (**MSB**) of a binary number indicates the sign (0 = positive, 1 = negative). The remaining bits represent the **magnitude** using a weighted system.

### Mathematical Definition:
$$\boxed{x = -a_{n-1} \cdot 2^{n-1} + \sum_{i=0}^{n-2} a_i \cdot 2^i}$$

### Conversion Steps:

**Positive to Negative:**
1. Write the binary number
2. Invert all bits (one's complement)
3. Add 1 to the result

**Negative to Positive:**
1. Write the two's complement number
2. Invert all bits
3. Add 1 to get the positive equivalent

### Range for n-bit numbers:
- **Minimum**: $-2^{n-1}$
- **Maximum**: $2^{n-1}-1$
- **8-bit range**: **-128** to **127**
- **16-bit range**: **-32,768** to **32,767**

### Advantages:
- Arithmetic operations work identically for positive and negative numbers
- Only one representation for zero (000...0)
- Simplifies hardware design in CPUs and ALUs
- Easy overflow detection

### Example:
**Convert -5₁₀ to 8-bit two's complement:**
- Start with +5: `00000101₂`
- Invert bits: `11111010₂` (one's complement)
- Add 1: `11111011₂` (two's complement)

**Verification:**
- `11111011₂` = -1×2⁷ + 1×2⁶ + 1×2⁵ + 1×2⁴ + 1×2³ + 0×2² + 1×2¹ + 1×2⁰
- = -128 + 64 + 32 + 16 + 8 + 0 + 2 + 1 = -5₁₀

---

## CPU Flags (Status Register)

| Flag | Name | Purpose | Set When | Examples (8-bit) |
|------|------|---------|-----------|------------------|
| **C/CY** | Carry | Unsigned overflow | Result > 255 (8-bit) or > 65535 (16-bit) | `255 + 1 = 0` (C=1) |
| **P** | Parity | Error detection | Even number of 1s in result | `0110 0101` (4 ones, P=1) |
| **V/O** | Overflow | Signed overflow | Result outside signed range | `127 + 1 = -128` (V=1) |
| **Z** | Zero | Zero result | All bits of result are zero | `128 - 128 = 0` (Z=1) |
| **S/N** | Sign | Negative result | MSB of result is 1 | `5 - 10 = -5` (S=1) |
| **AC** | Auxiliary Carry | BCD arithmetic | Carry from bit 3 to bit 4 | `0x0F + 0x01` (AC=1) |

### Flag Details:
- **Carry (C)**: Used for unsigned arithmetic, indicates borrow in subtraction
- **Overflow (V)**: Occurs when adding two positives gives negative, or two negatives give positive
- **Parity (P)**: Only considers the low byte (8 bits) of the result

---

## Real Number Representation

### Floating Point Representation:
$$\boxed{N = (-1)^S \cdot M \cdot B^E}$$

Where:
- **S**: Sign bit (0 = positive, 1 = negative)
- **M**: Mantissa/Significand (fractional part)
- **B**: Base (usually 2 for binary)
- **E**: Exponent = Stored Value - Bias

## IEEE 754 Standard

### Single Precision (32-bit)


<img src="Pictures/single_precision_ieee.jpg" width=500 height="auto" style="display: block; margin: auto">

### Double Precision (64-bit)

<img src="Pictures/double_precision_ieee.jpg" width=500 height="auto" style="display: block; margin: auto">