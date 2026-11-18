Processors have many of them (registers) and their availability, and their number depends on the specific model.
But all of them can be conditionally divided into two groups - these are special-purpose registers and general-purpose registers.
*general purpose registers can be used by programmers at their discretion.*

However, there is a formal agreement between compilers and operating systems on the use of some of them. 
Not all registers are available, some of them are available only in privileged mode, that is, in the 16-bit mode in which the OS operates.
## GENERAL PURPOSE REGISTERS 
ACTS as a variable, parameters, and as temporary storage for calculation results. 
Consider the AX register, it is a 16-bit register, and consists of two parts, the low and high parts AH, AL, 8 bits each.
When processors became 32-bit, the registers expanded to 32-two bits (EAX). And at the same time, it was necessary to preserve the old registers for compatibility with old programs, so the registers began to look like a kind of nesting doll

![[Pasted image 20261002145626.png]]


# BACK PAGE --> [[Why Byte Addressing Is Faster]]
# NEXT PAGE --> [[Special-Purpose Registers]]