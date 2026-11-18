The classic rule for obtaining **additional code** (two's complement): "invert the bits, then add one."

==take the number -5 of type byte
five in binary will look like 0101
and we need a sign that we must put in the most significant bit of this number, let's call it the sign bit ==

![[Pasted image 20260906121923.png]]

We will assume that zero is a conditional plus (+), and one is a conditional minus (-). 
since the number is negative, we add one to the resulting number (1101), invert all the bits except the sign bit (1010) and add one to the resulting number (1011) 
we got minus 5 represented in two's complement code. (11111011)
and it is in this form that it will be stored in memory. the remaining bits in the byte will be filled with the sign bit. in our case, units. 
y positive number 5, the most significant bits would be filled with zeros.

**What happens step by step for -5:**

1. `0101` is 5 in regular binary.
2. Invert all bits (change 0→1, 1→0): `0101` → `1010`. This is called **reverse code** (one's complement).
3. Add a binary unit to the reverse code (`0001`):
 ![[Pasted image 20260906125043.png]] We get `1011`

**Why add one at all**, and not stop at the reverse code (`1010`)? Because the reverse code has an unpleasant feature - two representations of zero (`0000` and `1111`), and arithmetic does not work with it. Adding one eliminates this: the two's complement code has exactly one zero (`0000`), and normal addition/subtraction in this system works correctly "on its own", with no special rules for negative numbers - the processor does not need to know that a number is negative in order to correctly add it to another.


## **we need to add 7 and minus 5**
![[Pasted image 20260906125454.png]]

we convert 7 and minus 5 into binary form and get two numbers that just need to be added, we discard the sign bit of the resulting answer and get 2 in the decimal system


# BACK PAGE --> [[Various Data Types]]
# NEXT CHAPTER --> [[Language Structure]]