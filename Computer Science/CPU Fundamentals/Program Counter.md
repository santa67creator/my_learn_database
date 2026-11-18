![[Pasted image 20261010204604.png]]

Let's start with the fact that after turning on the computer, the processor begins to execute commands at some strictly fixed address.

==BIOS, the basic input/output operating system, is located at this address.==
 Its task is to find the first disk device that was specified, take the first sector from there, load it into memory and transfer control to it.
 That is, instruct the processor to now begin executing commands at the address of this loaded program.

This program is an operating system that subsequently puts the processor into protected mode.
 Then multitasking, working with memory is implemented, various restrictions are set, and so on.
 Next, when we run a program, the operating system allocates space for it, loads it into RAM, such as a hard drive, and then transfers control to it.

---
## What does it mean to transfer control?
==This means telling the processor where in memory it needs to execute the next command.==
 Here, the Instruction Pointer (IP) register is used, which stores a pointer, that is, the address to the next instruction in memory that needs to be executed.
 After the processor has received data from memory at this address, which was in the Instruction Pointer (IP), it updates the value in this register to point to the next instruction in memory.
 That is, it determines the size of the instruction received and adds it to the current value in the Instruction Pointer (IP).

This moves the pointer exactly one instruction forward.
![[Pasted image 20261010205618.png]]



# BACK PAGE --> [[Opcodes]]
# NEXT PAGE --> [[Processor Operating Modes]]