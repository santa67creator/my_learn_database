## Size RAM - depends on processor memory registers, 

**Multiple of cell size** - Memory consists of cells of 8 bits (1 byte). Therefore, the total amount of RAM is always a multiple of 8 bits

**Important:** If you put 16 GB of RAM in a 32-bit system, the processor will still only be able to use the first 4 GB - the rest is physically inaccessible, because the register cannot store addresses beyond this limit.

![[Pasted image 20260902083607.png]]

**1. Where did the “10 bits” on the slide come from**

This is not a real processor with a 10-bit register - there are almost no such things in nature. The author of the video simply **shows the pattern using different examples** (8 bits, 10 bits, 32 bits) so that you can see the formula itself in action, and not remember a specific number. It’s like in mathematics they show “2+2=4, 3+3=6, 5+5=10” - to understand the principle of addition, and not because these numbers are important.

**10-bit register → 2¹⁰ = 1024 bytes**  
This is where the famous “computer thousand” is born - 1024, and not the usual decimal 1000. This is why in computers 1 KB = 1024 bytes, and not 1000.

**2. How is the maximum number determined**

This is simply a count of possible combinations. Each bit is a light bulb: on (1) or off (0), that is, **2 options per bit**. If you have n light bulbs in a row, and each can be independently in 2 states, then the total combinations are:

$$2 \times 2 \times 2 \times ... (n \text{ раз}) = 2^n$$

Example on 3 bits - all possible options:

```
000, 001, 010, 011, 100, 101, 110, 111
```

This is exactly 8 = 2³ combinations. The maximum number in binary form here is `111` = 7 in decimal, that is, the range from 0 to 7 is exactly 8 values ​​(2³).

Likewise for 10 bits: 2¹⁰ = 1024 possible combinations (addresses 0 to 1023). For 32 bits: 2³² ≈ 4.3 billion combinations.

**3. How is the size of the register itself determined**

But this is no longer a calculation, but a **physical property of iron** - how many trigger lights the engineers physically soldered into the processor during production. This is a fixed number that you do not change programmatically - it is “hardwired” into the chip architecture (32-bit processor, 64-bit, etc.). This is exactly what you find out with the `lscpu` / `getconf LONG_BIT` commands that we discussed - they do not calculate the size, but **read a ready-made, hardware-defined** value.

In short: the register size is a given from the hardware manufacturer, and the maximum number of addresses is pure mathematics (2 to the power of this size).


# BACK PAGE --> [[RAM]]
# NEXT PAGE --> [[RAM Addressing]]