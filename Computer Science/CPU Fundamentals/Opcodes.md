An instruction, a command or an upcode, you may hear different names, but ultimately it is a special number ranging from 1 to several bytes in size, encoded in a special way so that the processor can understand what it needs to do.
That is, any program in any language after translation will be a set of commands for a specific processor.
These commands are stored in memory along with the data.
![[Pasted image 20261009121351.png]]

---


For example, in our super simple and pointless program we put the number 7 in variable x. *VAR X = 7;*
In assembly representation it will be *mov ax, 7* 
that is, put the number 7 in the AX register
![[Pasted image 20261009121450.png]]

in this example, MOV AX is an opcode represented symbolically == and seven 7 is data==

---

## in executable form, such a record will look like this in memory
![[Pasted image 20261009122221.png]]

where the first byte is an opcode and corresponds to the MOV AX command,
and seven is simply represented in binary.

After starting this program, the processor reads a set of bits from memory and understands that the first byte is the MOV AX command.
so it goes into the write state of the AX register.

then he will take our data seven (7) and write it to this register.
This happens with all subsequent commands.

---



# but how does the processor know which command needs to be executed at a given time?

# NEXT PAGE --> [[Program Counter]]
# BACK PAGE --> [[Register Overflow]]