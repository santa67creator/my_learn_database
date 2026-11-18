You've all heard that processors are characterized by their capacity.
![[Pasted image 20260920181750.png]]

## machine word is the maximum number of bits that the processor can operate at a time
*Exchange them with RAM, store them in registers, and so on*

---

![[Pasted image 20260923201527.png]]
## Processors from model 8086 to 80286 were 16-bit and they could not use a lot of memory.
Because a maximum of 16 bits could store a number from 0 to 65535,
which is the address of a byte in RAM that can be accessed.
That is, in theory, it was possible to address 64 kilobytes of addresses, based on this number. 
*But in reality it was possible to address 1 megabyte of memory and we will soon see why this is so*

---

## Starting from 80386... processors became 32 bit, 
This means that the number that could fit in such a register (processor) has become many times larger. 
==This means that the address space that can be addressed also increases to 4GB.== 
*It is 32-bit systems that are called x86*

---

## thanks to which 64-bit processors were born.  
Amd has developed a technology called amd64, 
==This technology itself is an extension of the x86 architecture to a 64-bit architecture with full backward compatibility.== 
*This means that support for 32-bit mode remains.* 
*Emt64-t is also 64 bit processors only from Intel*
Therefore, families of such processors began to be called x86-64



# BACK PAGE --> [[x86 vs ARM vs AVR]]
# NEXT PAGE --> [[REGISTERS]]