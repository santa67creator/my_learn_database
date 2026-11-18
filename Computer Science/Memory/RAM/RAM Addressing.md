## Byte addressing - ==each Byte is a separate address==

![[Pasted image 20260902073847.png]]

## Verbal addressing is several groups of bytes in one memory cell 
*(one big address)*

![[Pasted image 20260902074403.png]]

The number is not received by each byte, but by the whole **machine word** (for example, 2, 4 or 8 bytes at once). Then address 0 is the first 2 bytes, address 1 is the next 2 bytes, not the next byte

**Word** (machine word) is **how many bytes the processor can process/read at one time**, as one unit.

**Why is this even necessary?**  
The processor does not access memory one bit or byte at a time in its internal registers - it takes data in whole "bundles" of a fixed size. This is the word - **the basic unit with which the processor actually operates** internally (as opposed to the byte, which is the basic unit of memory itself, that is, addressing).

**The processor processes byte addressing faster than word addressing**
!--Byte addressing is better suited for working with strings! (hello word)
!--verbal addressing is better suited for working with numbers! (01234567)



# BACK PAGE --> [[RAM Size]]
# NEXT CHAP CHAPTER --> [[MEMORY CORE]]