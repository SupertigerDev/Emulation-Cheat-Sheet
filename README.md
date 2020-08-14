# Introduction
I'm really new to emulating so I am creating a cheetsheat to help me and others :) Some of this information might be incorrect as i'm not an expert :(

# Index
1. [Significant Bit](#significant-bit)
    * [Examples](#examples)
    * [Code](#code)
2. [Bitwize Operators](#bitwize-operators)
    * [Shifting](#shifting)
    
# Significant Bit
LSB (Least Significant Bit) and MSB (Most Significant Bit) is 1 bit (1 or 0) which is is at the start or end of a byte.
## Examples
```            
LSB: 00000001
            ^
LSB is 1

MSB: 10000000
     ^
MSB is 1
```
## Code
This is how you would get the MSB and LSB in Javascript. This should apply in most programming languages as well.
```js
// LSB of 0xf2 (11110010)
//                     ^
0xf2 & 1
// Result: 0

// MSB of 0xf2 (11110010)
//             ^
0xf2 & 0x80 ? 1 : 0
// Result: 1
```
**Notice**: I dont know if this is the proper way to get the MSB but I think it works :)



# Bitwize Operators
## Shifting
Shifting moves all the bits 1 to the left or 1 to the right depending on the operator you use.
```
Shifting 4 bits to the left:
0x23 << 4 (100011 << 4)
Result: 0x230 (1000110000)

Shifting 4 bits to the right:
0x23 >> 4 (00100011 << 4)
Result: 0x2 (00000010)
```
