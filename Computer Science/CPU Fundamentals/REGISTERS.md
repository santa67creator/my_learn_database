## REGISTERS (register memory) - small memory cells located on the processor itself
The processor has two types of memory. These are register memory and cache memory.
We'll talk about cache memory another time, but now we'll look at registers in more detail.
It is in them that the processor loads numbers from memory, they can act as variables, temporary results of calculations can be stored in them, etc. This memory is the fastest because the registers are located directly on the processor.
And he doesn’t need to go anywhere else to get his data. Therefore, read and write operations on registers are faster than operations on RAM ([[RAM]], RAM). 
On flash drives, disks, etc. In general, operations are very slow

![[Pasted image 20260927162743.png]]
*as soon as he starts executing the next command, it needs to be read from memory (ram) and put somewhere (registers) so that he can work with it.*


----

## Registers have sizes of 8, 16, 32 and 64 bits.
![[Pasted image 20260927162349.png]]
i.e. 16 bit processors = register size is 16 bits, 32 bit = 32 bits and so on
### The maximum register size is equal to the processor bit size
![[Pasted image 20260927162225.png]]

## in addition, the register (registers) must be a multiple of the RAM cell 
##### WHY IS THIS SO?
There are two main types of addressing: byte addressing and verbal byte addressing.
about this see here --> [[RAM Addressing]]
verbal addressing --> the size of one cell is equal to a machine word, for example 32 bits, and the processor addresses not bytes, but words.
Let's imagine our computer uses byte addressing and has a 32-bit processor installed. 
In order for the processor to start working, it needs to completely fill its 32-bit register. To fill it, the processor needs to read 4 cells from memory because 4 multiplied by 8 turns out to be 32, so 4 cells fit exactly into the register without leaving any free space.
![[Pasted image 20260927181740.png]]
###### now imagine that the register is not 32 but, for example, 34 bits
With such a register size, we will not be able to fill it evenly with data from memory.
because if we take the same 4 cells, we get 32 ​​bits, and there will be two more empty bits left. 
if we try to take the fifth cell, it does not fit into the remaining two bits, so we will have to discard the extra 6 bits from the last byte that do not fit.
![[Pasted image 20260927182438.png]]
==to prevent this from happening, the size must be
register was a multiple of the memory cell size ==

----

## FULL SCHEME
![[Pasted image 20260927182710.png]]



# BACK PAGE --> [[Bitness and Word Size]]
# NEXT PAGE --> [[Why Byte Addressing Is Faster]]