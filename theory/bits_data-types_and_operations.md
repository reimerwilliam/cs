# Bits, Data Types and Operations

## Bits and Data Types

### A unit of information

We symbolically represent the precence of voltage as "1" and the absence as "0". Each "1" and "0" is a bit (binary digit).

With one wire we can represent only two things (0 or 1). For example if we use 8 bits (corresponding to the voltage on each of 8 wires) we can represent $2^8=256$ different things. In general with $k$ bits, we can distinguish at most $2^k$ distinct items.

### Data Types

Ways to represent a value. A particular representation is a _data type_ if there are operations in the computer that can operate on information that is encoded in that representation.

- Decimal -> 5 = 5
- Unary -> 5 = 11111
- Binary
- Floating point -> $621 = 6.21 * 10^2$

## Integer Data Types

### Unsigned Integers

Has no sign (plus or minus) associated with it. It just has a magnitude. We can represent unsigned integers as strings of binary digits.

**Example:**

Decimal notation: $329 = 3*10^2 + 2*10^1 + 9*10^0$

With 5 Binary digits (base is 2 instead of 10): $5 = 0*2^4 + 0*2^3 + 1*2^2 + 0*2^1 + 1*2^0$

With $k$ bits, we can represent in this positional notation exactly $2^k$ integers, ranging from $0$ to $2^k - 1$.

### Signed Integers

In all three signed data types the representation for 0 and positive integers start with a leading 0.

Below is a 5-bit table showing how the same 5-bit pattern is interpreted as an unsigned integer, signed-magnitude, 1's complement and 2's complement value.

| Representation | Unsigned | Signed Magnitude | 1's Complement | 2's Complement |
| -------------: | :------: | :--------------: | :------------: | :------------: |
|          00000 |    0     |        0         |       0        |       0        |
|          00001 |    1     |        1         |       1        |       1        |
|          00010 |    2     |        2         |       2        |       2        |
|          00011 |    3     |        3         |       3        |       3        |
|          00100 |    4     |        4         |       4        |       4        |
|          00101 |    5     |        5         |       5        |       5        |
|          00110 |    6     |        6         |       6        |       6        |
|          00111 |    7     |        7         |       7        |       7        |
|          01000 |    8     |        8         |       8        |       8        |
|          01001 |    9     |        9         |       9        |       9        |
|          01010 |    10    |        10        |       10       |       10       |
|          01011 |    11    |        11        |       11       |       11       |
|          01100 |    12    |        12        |       12       |       12       |
|          01101 |    13    |        13        |       13       |       13       |
|          01110 |    14    |        14        |       14       |       14       |
|          01111 |    15    |        15        |       15       |       15       |
|          10000 |    16    |        −0        |      −15       |      −16       |
|          10001 |    17    |        −1        |      −14       |      −15       |
|          10010 |    18    |        −2        |      −13       |      −14       |
|          10011 |    19    |        −3        |      −12       |      −13       |
|          10100 |    20    |        −4        |      −11       |      −12       |
|          10101 |    21    |        −5        |      −10       |      −11       |
|          10110 |    22    |        −6        |       −9       |      −10       |
|          10111 |    23    |        −7        |       −8       |       −9       |
|          11000 |    24    |        −8        |       −7       |       −8       |
|          11001 |    25    |        −9        |       −6       |       −7       |
|          11010 |    26    |       −10        |       −5       |       −6       |
|          11011 |    27    |       −11        |       −4       |       −5       |
|          11100 |    28    |       −12        |       −3       |       −4       |
|          11101 |    29    |       −13        |       −2       |       −3       |
|          11110 |    30    |       −14        |       −1       |       −2       |
|          11111 |    31    |       −15        |       −0       |       −1       |

2's complement data type is used on just about every computer manufactured today.

## 2's Complement Integers

The positive integers are represented with the regular positional scheme. With 5 bits, we use exactly half of the $2^5$ codes to represent $0$ and the positive integers from $1$ to $2^4 - 1$. The negative integers was based on the wish to keep the logic circuits as simple as possible. Almost all computers use the same basic mechanism to perform addition. It's called an _arithmetic and logic unit_, usually known by its acronym ALU.

ALU has two inputs and one output. It performs addition by adding the binary bit patterns at its inputs, producing a bit pattern at its output that is the sum of the two input patterns.

For example:

| Binary  |
| :-----: |
|  00110  |
|  00101  |
| ======= |
|  01011  |
