---
source: /tmp/watch-klx0yrn8/download/video.mp4
title: video.mp4
duration: 33:47
watched_at: 2026-09-15T16:13:45.933895+00:00
intent: understand cores and PCs — easy to understand explanation of each theme in the video
hero_frames: [frame_0001.jpg, frame_0017.jpg, frame_0033.jpg, frame_0049.jpg, frame_0065.jpg]
transcript_source: whisper (groq)
---
 
# video.mp4

## TL;DR

- The CPU is the computer's "brain" that endlessly executes translated machine instructions — every program in every language becomes a sequence of these encoded commands in memory.
- Registers are the CPU's fastest memory; they grew from 16-bit (AX) to 32-bit (EAX) to 64-bit (RAX) like a matryoshka doll, preserving backward compatibility across the whole x86 family from the 8086 to modern Core i7.
- The OS owns the machine via privilege levels (ring 0 = OS, ring 3 = your apps), CPU modes (real → protected → 64-bit), and virtual memory/paging that gives each program the illusion of owning all RAM.
- Interrupts let devices (keyboard, etc.) grab the CPU's attention instantly, saving/restoring program state — this same switching mechanism is the foundation of multitasking (processes → threads).
- Cores (the viewer's stated interest) appear briefly at the end: three types of multiprocessing — multiple sockets, multiple cores per chip, and virtual cores (one physical core presenting two logical ones).

## Key moments

- **[00:45] Two CPU makers, one standard problem** — Intel and AMD both make CPUs, but many programming languages × many instruction sets = chaos; solved by unified instruction set architectures.
- **[02:31] x86 vs ARM vs AVR** — x86 for PCs/servers, ARM for phones/tablets, AVR for microcontrollers (cars, TVs); software is not portable across them.
- **[03:41] Bitness** — 16-bit (64 KB–1 MB), 32-bit (4 GB, "x86"), 64-bit (AMD64, which Intel licensed as EM64T rather than fragment the standard).
- **[06:53] Registers introduced** — tiny memory cells directly on the CPU, the fastest memory in the machine, acting as variables (see frame_0017.jpg).
- **[11:59] The register matryoshka** — AX → EAX → RAX, each generation nesting the previous one for backward compatibility.
- **[13:31] Overflow demo** — 120 + 10 in an 8-bit signed register wraps around to −126; same-sign operands with opposite-sign result = overflow (see frame_0033.jpg).
- **[17:27] Boot flow** — CPU starts at a fixed address (BIOS) → loads first disk sector → OS takes over → switches CPU to protected mode; Instruction Pointer drives all subsequent execution.
- **[19:37] Three CPU modes** — real address (16-bit), protected (32-bit, sandboxed apps), 64-bit; Intel/AMD docs call them Legacy/IA-32 and Long mode (see frame_0049.jpg).
- **[22:06] Privilege rings** — levels 0–3; ring 0 = OS with full access, ring 3 = user apps; rings 1–2 rarely used in practice.
- **[25:56] Virtual memory & paging** — logical address → descriptor tables → virtual address → page directory/page tables → physical address; 64-bit mode caps at 2⁵² bytes physical / 2⁴⁸ virtual (see frame_0065.jpg).
- **[28:17] Interrupts** — hardware (devices, prioritized), exceptions (CPU-generated protection violations), software (programmer `int` command); handler saves state, runs, restores state.
- **[32:37] Multiprocessing types** — multi-socket motherboards, multi-core processors, and virtual cores; deliberately left shallow in the video.

## Hook microscope (0-10s)

- Frames: 20 at 2 fps
- Word-level transcript (1 words):

```
[2.16s] Processor
```

Cold-open hook: the video opens directly on the thesis — “the processor is the brain of the computer, executing instructions obtained by translating programs from high-level languages to machine level” ([00:00]–[00:07], single word “Processor” landing at 2.16s over the opening visual). Pattern: **in-medias-res claim + exclusivity framing** — no greeting, no intro animation, straight into the material, followed at [00:23]–[00:35] by a scarcity/justification frame (“few people make this content because it’s hard to perceive, therefore this video is mandatory viewing”). The hook targets self-identified programmers' curiosity about what happens "behind the scenes" - an educational hook rather than an entertainment one.

## Editorial profile

_No scene-change data — likely a static/screen-recorded source._

Single-presenter lecture with static slides/screencast-style visuals (no scene changes detected); long-form, patient pacing — 33 minutes of sequential whiteboard-style explanation with worked examples (register layouts, overflow arithmetic, address translation chains).

## Quotable moments

- "The processor is the brain of the computer, executing a set of instructions obtained by translating programs from high-level languages down to machine level." [00:00]
- "All application programs working on the computer are like children in a sandbox, limited to the capabilities that the operating system itself provides." [20:37]
- "Sometimes you need to push apart the layers of abstraction and look at what's underneath the hood." [33:18]
- "If you watched this video to the end, in half an hour you learned more about the computer than some programmers who spend a whole year studying the next framework hoping to attain enlightenment." [33:23]
- "Growth begins where complexity begins; where ease begins, degradation is born." [33:38]

## Entities mentioned

- People: none mentioned by name
- Companies:
- Tools / products: 
- Places: none

## Concepts surfaced

- **Instruction set architecture (ISA)** — the common standard of commands a CPU family understands; solves the many-languages × many-processors problem and enables backward compatibility.
- **Bitness / machine word** — how many bits the CPU handles at once; determines addressable memory (16-bit ≈ 1 MB, 32-bit = 4 GB, 64-bit capped at 2⁵² physical / 2⁴⁸ virtual).
- **Registers** — tiny fastest-memory cells on the CPU; general-purpose (programmer variables) vs special-purpose (segment, stack, flags, Instruction Pointer).
- **Register matryoshka** — RAX ⊃ EAX ⊃ AX ⊃ AH+AL: each wider generation nests the previous, keeping old code working.
- **Integer overflow** — when a result doesn't fit the register, high bits are cut and counting wraps to the opposite end (120+10 → −126 in 8-bit signed).
- **Byte vs word addressing** — byte addressing wins for text-heavy workloads (single-character overwrite), word addressing for number-heavy ones.
- **Assembly language** — symbolic one-line-per-machine-command language; per-architecture, reveals what high-level abstractions compile down to.
- **Fetch-execute cycle** — CPU reads the instruction at the Instruction Pointer, advances the pointer by the instruction's size, executes; repeats until power-off.
- **Boot chain** — fixed address → BIOS → first disk sector → OS → protected mode.
- **CPU modes** — real address (16-bit, no protection) → protected (32-bit, sandboxed) → 64-bit; vendor docs name them Legacy/IA-32 and Long mode.
- **Privilege rings** — 4 levels, 0 (OS, full access) to 3 (user apps); bans cascade downward; in practice only 0 and 3 are used.
- **Address translation** — logical address (segment + offset) → descriptor tables → virtual address → page directory/page tables → physical address.
- **Virtual memory / paging** — the OS gives every program the illusion of owning the full address space; pages are fixed-size blocks mapped via page tables.
- **Interrupts** — hardware (device signals via controller, prioritized), exceptions (CPU-generated protection violations), software (`int` command / OS system calls); state is saved and restored around the handler.
- **Multitasking illusion** — processes split into threads that switch rapidly with state save/restore, appearing simultaneous.
- **Multiprocessing types** — multi-socket, multi-core, virtual cores (hyperthreading-style).

## Transcript

_Source: whisper (groq)._

```
[00:00] processor is the brain of a computer that executes a set of instructions that is obtained during broadcasting
[00:07] programs from high level languages to machine level all this happens behind the scenes and in the usual
[00:13] mortals don't need to know what's going on there, people who call themselves programmers need it though
[00:19] would like to have an idea of how the work of a computer is organized with the participation of processor memory
[00:24] operating systems and finally application level programs, few people make such content for the reason
[00:30] the complexity of its perception, so this video is a must watch and everything you will learn
[00:35] here will undoubtedly expand your horizons in the field of programming and so we will talk about processors
[00:45] and it’s worth starting with the fact that currently there are two large companies that produce
[00:51] processors are Intel and AMD, but you should understand that there are many processor models, all
[00:57] they differ in speed and cost and the most important thing is that each of them has its own
[01:04] a specific set of commands that they are capable of executing, hence the problem that arises
[01:09] lies in the variety of programming languages, assuming that each creator of his own language
[01:16] will translate the program into its own individual set of instructions, which it considers
[01:21] is the most correct, then in this case each of the processors will have to be able to execute programs
[01:27] in all possible languages, not just one of them. If you don't understand what it means
[01:32] translation of the programming language, and here is a set of instructions and so on, then watch the video
[01:38] is about programming languages, the link to which is in sleep mode in the description. Second
[01:44] the problem is that the software needs to be written backwards compatible
[01:50] for older processor models could also work on new ones with new versions
[01:54] processors must support some new commands to solve both of these problems
[02:00] some kind of single standard, a single architecture of a set of commands so that programs written in
[02:05] in different languages could be translated into a common form for all into a set of commands for a specific
[02:11] processor architectures, that is, processors must support some unified architecture of which
[02:18] will be followed by developers of programming language translators when translating a program into its
[02:23] low level representation There are quite a few instruction set architectures and let's take three of them
[02:31] them, related to different areas, the x86 architecture is a whole family of processors that
[02:38] are used in our personal computers and servers based on the r.m. architecture. used in
[02:43] most smartphones and tablets and the avi ar architecture which is used in microcontrollers
[02:48] embedded systems such as cars TV and so on each of these architectures supports
[02:55] its own set of commands so software written for x86 will not work on Maria and
[03:02] and others, we will further talk about x86 processors as the most commonly used processors
[03:09] in practice, almost every one of you writes programs for them or wrote them at some point during
[03:14] of his programming education, the name x86 appeared for historical reasons and here
[03:21] refers to a whole family of processors starting from 8086 to modern core family and so on
[03:27] further thanks to the unified architecture that they all inherit from the program that was written
[03:34] for the 8086 processor will also be executed on the core i7, you all heard that processors are characterized by
[03:41] bit depth what is it bit depth is the value that determines the size of the machine
[03:47] words machine word is the maximum number of bits that the processor can operate at a time
[03:53] Exchange them with RAM, store them in registers, and so on.
[03:58] Processors from model 8086 to 80286 were 16-bit and they could not use a lot of memory.
[04:08] Because 16 bits could store a maximum number from 0 to 65535,
[04:15] which is the address of a byte in RAM that can be accessed.
[04:21] That is, in theory, it was possible to address 64 kilobytes of addresses, based on this number.
[04:28] But in reality it was possible to address 1 megabyte of memory and we will soon see why this is so.
[04:34] Subsequent processors, starting with model 8386, became 32-bit and therefore the number that could fit in such a register became many times larger.
[04:46] This means that the address space that can be addressed also increases.
[04:50] up to 4 gigabytes of a 32-bit system and was called x86, but the technology did not stand up
[04:58] on site and during their development, companies a m d developed a technology called a m d
[05:04] 64 thanks to which 64-bit processors were born, this technology itself is an extension
[05:13] x86 to 64-bit architecture with full backward compatibility this means
[05:20] that support for 32-bit mode remains, so the family of such processors began to bear the name
[05:27] x86 64 main competitor Intel could not stay away for long and its processor too
[05:35] should have become 64-bit but if intel implements their own 64-bit
[05:43] architecture then this will again lead us to the problem with different processor architectures and development
[05:49] software will again become complex due to the lack of any standardization
[05:54] intel understood this perfectly well and in order not to complicate the situation, they simply licensed the technology from mmd
[06:02] amd 64 with minor changes calling it and m64 t so in fact these two technologies are one and the same
[06:11] However, Intel still has its own 64-bit technology called a and 64 but
[06:19] it is intended for use on high-performance server systems in
[06:25] As a result, the data size during calculations and addressing increased to 64 bits, and these are the processors that are now used in most computers.
[06:35] After turning on the computer, the processor begins to endlessly execute commands and does not finish until the computer is turned off.
[06:44] But before he starts executing the next command, he needs to read it from memory and put it somewhere so that he can work with it.
[06:53] For these purposes, the processor has two types of memory. These are register memory and cache memory.
[07:00] We'll talk about cache memory another time, but now we'll look at registers in more detail.
[07:05] Registers are small memory cells located on the processor itself.
[07:10] It is in them that the processor loads numbers from memory.
[07:13] They can serve as variables and can store temporary results of calculations.
[07:19] This memory is the fastest because the registers are located directly on the processor and it does not need to go anywhere else to get data.
[07:28] Therefore, read and write operations with registers are performed much faster than operations with the same RAM, not to mention slow external memory, such as disks, flash drives, and the like.
[07:41] Registers have sizes of 8, 16, 32 and 64 bits.
[07:46] bits the maximum register size is equal to the processor bit size, that is, 16 bits
[07:52] processors register size is 16 bit 32 bit 32 bit and so on in addition to this
[07:59] register must be a multiple of the RAM cell why this is so from the video about memory
[08:06] we know that there are two main types of addressing: byte addressing and verbal byte addressing.
[08:13] when each memory cell is equal to one byte and each byte has its own address at which
[08:19] 32 32
[08:35] addressing and a 32-bit processor is installed for the processor to start working it needs to be completely
[08:41] fill your register with 32 bits; in order to fill it, the processor needs to read from memory
[08:48] 4 cells because 4 multiplied by 8 turns out to be 32, so 4 cells fit exactly into the register not
[08:56] leaving free space, now imagine that the register is not 32 but, for example, 34 bits
[09:03] with such a register size we will not be able to fill it exactly with data from memory because if
[09:09] we take these same 4 cells, we get 32 bits and there will be two more empty bits left if we try
[09:16] take the fifth cell, it does not fit into the remaining two bits so you have to discard
[09:22] extra 6 bits from the last byte that didn’t fit so that this doesn’t happen you need the size
The [09:28] register was a multiple of the size of the memory cell, but despite the fact that it is a multiple, everything fits exactly
[09:36] the processor has to read 4 cells from memory at once instead of one because in our
[09:42] The computer uses byte addressing, not verbal addressing.
[09:45] And at first glance it seems that this is ineffective, but
[09:48] is actually a byte-addressable processor
[09:52] work faster than with verbal due to the fact that
[09:55] what is the main type of information that the processor works with
[09:58] is text.
[09:59] We are constantly writing, reading or editing something
[10:02] text.
[10:03] Depending on the encoding, the character may occupy
[10:05] memory different number of bytes, but minimum size,
[10:08] which is used in the ASCII standard is 7 bits. For example, to change the second letter in the text,
[10:15] when byte addressing, the processor needs to find the address of this symbol in memory and rewrite it
[10:21] to another symbol. If verbal addressing is used, then the entire line will be in one
[10:28] 32-bit cell. And in order for us to find the required character in this line, we need to place the entire cell
[10:35] into the register, then search bit by bit for where the desired symbol is, discard extra bits, and so on
[10:41] It turns out that for computers where text processing predominates, it is better suited
[10:46] byte addressing and in computers for working with numbers verbal returning is better suited
[10:53] The processor has quite a lot of registers and their presence and quantity depends on the specific model
[11:00] but all of them can be divided into two groups: special-purpose registers and registers
[11:07] general purpose register can be used by programmers at their discretion
[11:12] However, there are formal agreements between compilers and operating systems on the use
[11:18] some of them plus not all registers are available for us to use because many of them are available
[11:24] only in privileged mode in which the operating system runs the general register
[11:29] assignments act as variable parameters and as temporary storage for results
[11:36] calculations consider the ax register it is a 16-bit register and consists of two parts
[11:42] junior and senior parts on Eichi al. 8 bits each when processors became 32 bit then
[11:50] then the registers expanded to 32 bits, and at the same time it was necessary to preserve the old registers for compatibility with old programs.
[11:59] Therefore, the registers began to look like a kind of nesting doll.
[12:02] First, they added the letter E, Extended, to their names, and these 16-bit registers became 32-bit.
[12:10] That is, AX became known as EAX, BX, EBX, and so on.
[12:15] And the 32-bit EAX register became 16-bits plus the 16-bit AX register, which can still be accessed.
[12:25] After the advent of 64-bit systems, the registers again received an extension, becoming 64-bit, and the letter I in their name was changed to R.
[12:35] As a result, EAX became known as RAX, while backward compatibility was still maintained.
[12:40] RAX consists of a 32-bit plus a 32-bit EAX register, which in turn consists of a 16-bit plus a 16-bit AX register, which is still divided into two 8-bit registers H and AL.
[12:56] Special purpose registers, as the name suggests, are intended for some specific content in them.
[13:03] For example, segment registers store memory addresses.
[13:06] Stack registers point to the beginning of the frame and the top of the stack.
[13:11] Flag registers contain various bits that reflect the state of the result of a previous operation.
[13:18] The Command Instruction Pointer contains the address of the command to be executed next, and so on.
[13:25] But what will happen to the register if we try to write a number into it that does not fit into its dimensions?
[13:32] For example, we have 8-bit registers and we add two numbers 120 plus 10.
[13:38] Both numbers 120 and 10 fit into one byte, so first we will write them into the AH and AL registers.
[13:46] And now we will try to add them, writing the result to the AH register.
[13:51] The problem here is that the numbers from minus 128 to 127 fit into the sign byte.
[13:57] 7 that is, the result of the expression 130 simply will not fit into this register, in this case it happens
[14:03] so-called overflow overflow can occur in two cases if two are added
[14:09] large positive numbers or two large negative ones are subtracted in this case the most significant bits
[14:15] which do not fit into the register are cut off and the result will be the number that
[14:21] is left after this clipping; in fact, the overflow means that after going beyond the boundary
[14:28] valid we continue counting from the opposite end in this example we reach 127 and remains
[14:36] add three more by adding one we get to the opposite end to the number minus 128 and
[14:43] we continue to add to it so the output is the number minus 126 if we add
[14:50] is a number with one sign; at the output we get another sign, which means an overflow has occurred so that you can
[14:57] was to use registers in your code and to understand how they work you need to write a program in languages
[15:03] as close as possible to level machines that provide access to work with hardware
[15:09] provided directly and such languages include assembly language, which is a low-level language
[15:15] programming consisting of a symbolic designation of machine instructions, the assembler itself is
[15:21] program is a translator of this language into machine code where all these symbolic commands will be
[15:27] are represented as binary codes that correspond to these commands according to
[15:32] processor architecture, that is, an assembly program consists of a set of instructions for
[15:36] of a specific processor family, this means that x86 uses its own set of commands and
[15:42] and its own assembler for RAM processors there will be a different set of commands and therefore a different
[15:48] assembler this language allows you to understand how the processor executes your program, that is
[15:54] all these abstractions of programming languages in the form of variable conditions of object cycles and so on
[15:59] Further, at a low level, this is all working with registers, processor commands and working with memory, and so on
[16:07] The processor reads instructions from memory into its register, and then begins executing them.
[16:13] Instruction, command or upcode, you hear different names, but ultimately it is a special number ranging in size from 1 to several bytes, encoded in a special way so that the processor can understand what it needs to do.
[16:27] That is, any program in any language after translation will be a set of commands for a specific processor.
[16:34] processor. These commands are stored in memory along with the data. For example, in our super simple and
[16:39] for a purposeless program we put the number 7 in variable x. In assembly representation it will be
[16:46] moveax7 ax 7 moveax x 7 x
[17:02] about the code and corresponds to the command husband a x seven is simply represented in binary after launch
[17:09] of this program, the processor reads a set of bits from memory and understands that the first byte is
[17:14] of the command move a x so it moves the write state to the register a x then it will take our data
[17:20] seven and writes it to this register. This happens with all subsequent commands, but where does the processor come from?
[17:27] knows what command needs to be executed at a given time, let's start with the fact that after turning on
[17:34] computer processor begins to execute commands at some rigidly fixed address at
[17:40] The BIOS, the basic input/output operating system, is located at this address.
[17:45] Its task is to find the first disk device that was specified, take the first sector from there, load it into memory and transfer control to it.
[17:54] That is, instruct the processor to now begin executing commands at the address of this loaded program.
[18:01] This program is an operating system that subsequently puts the processor into protected mode.
[18:07] further implements multitasking, working with memory, setting various restrictions, and so on.
[18:13] We will find out what all this means in a few minutes.
[18:16] Next, when we run a program, the operating system allocates space for it,
[18:21] loads it into RAM, such as a hard drive, and then transfers control to it.
[18:27] What does transfer control mean?
[18:29] This means telling the processor where in memory it needs to execute the next command.
[18:36] Here the Instruction Pointer register is used, which stores a pointer, that is, the address to the next instruction in memory that needs to be executed.
[18:46] After the processor has received data from memory at this address, which was in the Instruction Pointer, it updates the value in this register to point to the next instruction in memory.
[18:57] That is, it determines the size of the received instruction and adds it to the current value in the Instruction Pointer.
[19:03] Thus, the pointer is moved forward exactly one instruction.
[19:09] The addresses at which the processor accesses memory are set by programs during their execution.
[19:15] But if they could access any location in memory, this would cause a bunch of security problems.
[19:21] Therefore, the address that the program sets and the real address of the cell in memory can be very different.
[19:28] This system is called the address translation mechanism.
[19:31] To understand how it works, you should first understand the processor operating modes.
[19:37] The processor can operate in several modes.
[19:40] The first mode is called real address mode.
[19:43] This is a 16-bit mode that the processor enters immediately after turning on the computer.
[19:49] It is called so because the address generated by the programs is real and does not require any additional transformations.
[19:57] The second mode is called protected.
[19:59] This is a 32-bit mode that can only be entered from real addresses mode.
[20:05] Secure means that data protection is provided,
[20:09] operating system from application programs and data from these programs from each other,
[20:13] by separating applications into different privilege levels.
[20:18] After the operating system takes control,
[20:21] it puts the processor into protected mode by setting a special system register flag,
[20:25] sets permission and conditions for other programs, defines handle and interrupt tables.
[20:32] Thus, the operating system becomes a full-fledged master of the computer.
[20:37] All application programs running on a computer are like children in a sandbox,
[20:42] which are limited by the capabilities that the operating system itself provides them.
[20:47] The processor monitors all this order, not allowing overriding the operating system conditions,
[20:53] access prohibited memory areas, execute prohibited commands, and so on.
[20:58] This is achieved through privilege levels, which we'll talk about in a couple of minutes.
[21:02] If the protection conditions are violated, an exception is generated,
[21:06] and control is transferred to the operating system so that it can take action.
[21:11] The last mode in which most modern processors operate is 64-bit mode.
[21:17] You can switch to it only from protected mode and it also protects programs from each other.
[21:24] However, the official documentation from Intel and AMD has a slightly different classification of operating modes, which complicates understanding, so I have identified three main ones.
[21:34] According to their classification, there are only two modes.
[21:37] This is a 32-bit mode that includes the real address mode and the protected mode itself.
[21:43] For AMD it is called Legacy Mod for Intel iA32.
[21:47] And the 64-bit mode, which also includes two submodes.
[21:51] Itself 64-bit and compatibility mode.
[21:55] For AMD it is called Long Mod for Intel iA32i.
[22:00] Compatibility mode provides support for 32 and 16-bit code.
[22:06] The privilege level, which was mentioned a little earlier,
[22:09] is access to CPU resource usage.
[22:13] There are no privileges in real address mode, because only one program can be executed in it at a time, so there is no one to protect the data from.
[22:21] In other modes there are 4 levels of privileges from 0 to 3.
[22:25] Zero level, otherwise privileged.
[22:28] This level provides full access to the processor and is where the operating system runs.
[22:35] First level, less privileged.
[22:37] Prohibitions set at level zero will apply to level one.
[22:41] Further, everything is by analogy, that is, the second level has even fewer privileges and the prohibitions established at the zero and first levels will apply to the second.
[22:51] Level 3 is also called user level; it has the lowest priority and is subordinate to all higher levels.
[22:59] All application programs run on it and they cannot access data that was defined for other layers.
[23:06] In practice, the first and second levels are rarely used in operating systems.
[23:12] Basically only two levels are used.
[23:14] This is zero privileged and third user.
[23:18] Thus, programs and data are limited within their privilege levels,
[23:23] where access to many commands, control registers, memory areas, and so on is strictly blocked.
[23:31] Knowing the operating modes of the processor, you can move on to the addressing device.
[23:34] all RAM is divided into conditional segments - these are separate sections of memory for a specific
[23:41] size and their size depends on the processor mode in which it operates the address of a specific cell
[23:48] memory that programs expose is presented in a special format: the address of the beginning of the segment plus
[23:54] offset in this segment; this type of address is called logical in real mode
[24:00] addresses all memory is divided into segments of 64 kilobytes in size, in it the segment address and offset
[24:07] are 16-bit numbers that are the actual segment addresses and offsets
[24:13] in memory this logical address is converted to a 20-bit physical address of the memory cell
[24:18] which will be set to the address bus, that is, the segment is taken and shifted to the left by 4 to it
[24:25] the offset is added and the physical address is obtained - the maximum number of addresses that
[24:30] we can address in this mode is 2 to the 20th power which is equal to one megabyte
[24:36] physical memory in protected mode, all memory is divided into segments from 0 to 4 gigabytes operating
[24:44] system creates the illusion that each program has at its disposal all available address
[24:50] space in this mode activates the virtual address translation mechanism
[24:55] physically, that is, programs begin to work in the virtual address space about which
[25:00] they themselves don’t realize they continue to form exactly the same addresses as
[25:05] I previously assume that they are accessing real addresses in memory and the logical address of the set
[25:11] 16 16
[25:28] handle. This descriptor specifies the starting address of the segment, the privilege level,
[25:33] its dimensions and so on. They are located in special descriptor tables. From handle
[25:39] the segment address is extracted, the offset is added to it and thus the logical address
[25:44] is converted to virtual, provided that the address translation mechanism is enabled otherwise
[25:49] case this address will be physically if there is a virtual address then it should be
[25:56] virtual memory this structure is called page memory organization all
[26:02] address space is divided into pages, these are contiguous areas of memory and their size too
[26:09] depend on the processor mode and the address translation mode; each page is described by the structure
[26:16] which are combined specifically by the country table, each page table is also described separately
[26:21] structure and are not combined into a directory of pages and with each memory access a virtual address
[26:28] is divided into three parts, this is the index of the elements of the page directory from which it is retrieved
[26:33] physical address of the page table index in this page table from which physical
[26:39] page address and offset in this page then, using the address translation mechanism, occurs
[26:46] converts a virtual address to a 32-bit physical address and therefore maximally
[26:52] can be addressed to 2 to the 32nd power or 4 gigabytes of memory 64-bit mode is an extension
[27:01] 32-bit architecture under 64-bit therefore the general concept working in protected mode remains
[27:08] and here, however, there are some significant changes, for example almost completely
[27:14] segmentation is disabled, it would be logical to assume that in this mode you can
[27:18] addresses up to 2 64 bytes of memory but is actually only accessible up to 2 52
[27:26] bytes of physical memory and up to 2 in 48 bytes of virtual memory, these limitations are due to
[27:33] limitation of the processor architecture itself and the operating system exhaled information
[27:40] there was quite a lot about addresses, so let’s summarize everything that was said during the execution of the program; it needs
[27:47] access memory areas to receive data from there, write them, call others
[27:52] procedures and so on, for this it forms logical addresses to memory for which it should
[27:58] occurs this reversal depending on the operating mode of the processor, this logical address is either
[28:04] the physical one is immediately converted or the virtual one is converted, after which the virtual one is converted
[28:10] physical, after that it is set to the bus address and the ok processor is called
[28:18] is constantly busy executing instructions, hence the question arises of how an external device
[28:23] manages to interact with the processor, for example by entering something from the keyboard, we need to
[28:28] the processor processed the request by receiving some data from the user right at the time of program execution
[28:34] without any delays in this case, external devices transmit through the interrupt controller
[28:41] processor and interrupt signal when interrupting there is a signal to the processor to interrupt
[28:46] execution of the current program and transferred control to a special function about the work q interrupt function
[28:53] handlers are ordinary programs that are constantly in memory
[28:57] and can be called at any time, having received a signal, the processor generates an interrupt by sending
[29:03] control the handler of this very interruption, the current program is interrupted but it must
[29:09] be continued after the handler has completed its work, so the state of the current one is saved first
[29:16] program which is characterized by registers with the address of the next instruction and so on then
[29:21] That is, everything that can be changed during the operation of the handler.
[29:25] After its completion, the handler transfers control to the interrupted program.
[29:30] Restores its last saved state.
[29:33] And she continues working from the place where she was interrupted.
[29:38] The interrupt is also located in a special interrupt descriptor table.
[29:42] These handles have a privilege level that determines the program's privilege level,
[29:47] which can take advantage of this interrupt.
[29:50] There are three main types of interrupts. These are software, hardware and exceptions.
[29:56] Let's start from the end. An exception is generated by the processor itself when a program tries to violate
[30:01] protection limitation or when errors occur during its execution. Thanks to such interruptions
[30:08] operating system can protect its data from user programs, which is what we are talking about
[30:14] spoke a little earlier. Hardware interrupts are generated by the interrupt controller, it
[30:19] It acts as a link between external devices and the processor.
[30:23] Interrupts are processed according to priorities, which avoids collisions,
[30:27] which appear when signals are received from several sources at once.
[30:32] Software interrupts can be generated by the int command programmer himself.
[30:35] This feature is available, for example, in the MS-DOS operating system in real address mode.
[30:42] Its operant just means the number from the interrupt descriptor in the descriptor table.
[30:47] In the Windows operating system, programs cannot call an interrupt directly.
[30:52] Instead, system functions have appeared that the axis itself provides for connecting application programs with external devices.
[31:00] Thus, interrupts allow you to switch the execution of one program to another.
[31:05] The multitasking mechanism is based on this approach.
[31:08] That is, the simultaneous illusory operation of all programs on the computer is achieved by constantly switching them.
[31:15] This mechanism is implemented programmatically by operating systems and it works in 32 and 64 bit modes, respectively.
[31:24] All this time we talked about programs as integral units executed by the processor, so as not to create confusion in the head.
[31:32] In fact, a program is too huge a set of instructions to talk about it as some kind of integral unit.
[31:39] Therefore, when implementing operating systems, all programs are divided into processes, processes are divided into threads or tasks.
[31:47] And already a task is an independent sequence of commands that are executed in its environment.
[31:53] A large number of these threads are not executed simultaneously, as we already understood.
[31:57] They quickly switch, replace each other, and because of this, the illusion is created that all running programs on the computer are working in synchronous mode.
[32:07] Before changing a task, its state is saved in a specially allocated memory area, as was done at the time of interruption.
[32:15] After which the next task is launched, having previously restored its state in which it was interrupted earlier.
[32:23] In addition to multitasking, multiprocessing is now used everywhere.
[32:28] Each processor has multiple cores, and servers have multiple processors.
[32:33] One way or another, there are three main types of multiprocessor systems.
[32:37] This is when the motherboard has multiple processor sockets, when the processor has multiple cores, and when the processor has virtual cores.
[32:47] We will not consider their interaction now, since this is a rather complex topic that will blow the minds of fragile minds.
[32:55] Okay, conclusion of the day.
[32:56] With the release of new processors and with the development of technology, the operating model of processors and operating systems will constantly change.
[33:04] So what I told you is the general concept of how it works in principle.
[33:10] Understanding such things, at least at the theoretical level, gives you an idea of ​​the machine you are working with, for which you are writing code.
[33:18] The layers of abstraction need to be pulled apart at least sometimes and look at what’s underneath the hood.
[33:23] If you watched this video to the end, then in half an hour you learned more about the computer than some programmers who spend a whole year studying the next framework in the hope of finding enlightenment.
[33:35] If all this seems complicated to you, that's okay.
[33:38] Growth begins where complexity begins, where lightness begins, where degradation begins.
[33:45] Like for development.
[33:46] Good luck.
```

## All frames

_Total: 80. Hero frames flagged with star._

* `/tmp/watch-klx0yrn8/frames/frame_0001.jpg` (t=00:00)
  `/tmp/watch-klx0yrn8/frames/frame_0002.jpg` (t=00:25)
  `/tmp/watch-klx0yrn8/frames/frame_0003.jpg` (t=00:51)
  `/tmp/watch-klx0yrn8/frames/frame_0004.jpg` (t=01:16)
  `/tmp/watch-klx0yrn8/frames/frame_0005.jpg` (t=01:41)
  `/tmp/watch-klx0yrn8/frames/frame_0006.jpg` (t=02:07)
  `/tmp/watch-klx0yrn8/frames/frame_0007.jpg` (t=02:32)
  `/tmp/watch-klx0yrn8/frames/frame_0008.jpg` (t=02:57)
  `/tmp/watch-klx0yrn8/frames/frame_0009.jpg` (t=03:23)
  `/tmp/watch-klx0yrn8/frames/frame_0010.jpg` (t=03:48)
  `/tmp/watch-klx0yrn8/frames/frame_0011.jpg` (t=04:13)
  `/tmp/watch-klx0yrn8/frames/frame_0012.jpg` (t=04:39)
  `/tmp/watch-klx0yrn8/frames/frame_0013.jpg` (t=05:04)
  `/tmp/watch-klx0yrn8/frames/frame_0014.jpg` (t=05:29)
  `/tmp/watch-klx0yrn8/frames/frame_0015.jpg` (t=05:55)
  `/tmp/watch-klx0yrn8/frames/frame_0016.jpg` (t=06:20)
* `/tmp/watch-klx0yrn8/frames/frame_0017.jpg` (t=06:45)
  `/tmp/watch-klx0yrn8/frames/frame_0018.jpg` (t=07:11)
  `/tmp/watch-klx0yrn8/frames/frame_0019.jpg` (t=07:36)
  `/tmp/watch-klx0yrn8/frames/frame_0020.jpg` (t=08:01)
  `/tmp/watch-klx0yrn8/frames/frame_0021.jpg` (t=08:27)
  `/tmp/watch-klx0yrn8/frames/frame_0022.jpg` (t=08:52)
  `/tmp/watch-klx0yrn8/frames/frame_0023.jpg` (t=09:17)
  `/tmp/watch-klx0yrn8/frames/frame_0024.jpg` (t=09:43)
  `/tmp/watch-klx0yrn8/frames/frame_0025.jpg` (t=10:08)
  `/tmp/watch-klx0yrn8/frames/frame_0026.jpg` (t=10:33)
  `/tmp/watch-klx0yrn8/frames/frame_0027.jpg` (t=10:59)
  `/tmp/watch-klx0yrn8/frames/frame_0028.jpg` (t=11:24)
  `/tmp/watch-klx0yrn8/frames/frame_0029.jpg` (t=11:49)
  `/tmp/watch-klx0yrn8/frames/frame_0030.jpg` (t=12:15)
  `/tmp/watch-klx0yrn8/frames/frame_0031.jpg` (t=12:40)
  `/tmp/watch-klx0yrn8/frames/frame_0032.jpg` (t=13:05)
* `/tmp/watch-klx0yrn8/frames/frame_0033.jpg` (t=13:31)
  `/tmp/watch-klx0yrn8/frames/frame_0034.jpg` (t=13:56)
  `/tmp/watch-klx0yrn8/frames/frame_0035.jpg` (t=14:22)
  `/tmp/watch-klx0yrn8/frames/frame_0036.jpg` (t=14:47)
  `/tmp/watch-klx0yrn8/frames/frame_0037.jpg` (t=15:12)
  `/tmp/watch-klx0yrn8/frames/frame_0038.jpg` (t=15:38)
  `/tmp/watch-klx0yrn8/frames/frame_0039.jpg` (t=16:03)
  `/tmp/watch-klx0yrn8/frames/frame_0040.jpg` (t=16:28)
  `/tmp/watch-klx0yrn8/frames/frame_0041.jpg` (t=16:54)
  `/tmp/watch-klx0yrn8/frames/frame_0042.jpg` (t=17:19)
  `/tmp/watch-klx0yrn8/frames/frame_0043.jpg` (t=17:44)
  `/tmp/watch-klx0yrn8/frames/frame_0044.jpg` (t=18:10)
  `/tmp/watch-klx0yrn8/frames/frame_0045.jpg` (t=18:35)
  `/tmp/watch-klx0yrn8/frames/frame_0046.jpg` (t=19:00)
  `/tmp/watch-klx0yrn8/frames/frame_0047.jpg` (t=19:26)
  `/tmp/watch-klx0yrn8/frames/frame_0048.jpg` (t=19:51)
* `/tmp/watch-klx0yrn8/frames/frame_0049.jpg` (t=20:16)
  `/tmp/watch-klx0yrn8/frames/frame_0050.jpg` (t=20:42)
  `/tmp/watch-klx0yrn8/frames/frame_0051.jpg` (t=21:07)
  `/tmp/watch-klx0yrn8/frames/frame_0052.jpg` (t=21:32)
  `/tmp/watch-klx0yrn8/frames/frame_0053.jpg` (t=21:58)
  `/tmp/watch-klx0yrn8/frames/frame_0054.jpg` (t=22:23)
  `/tmp/watch-klx0yrn8/frames/frame_0055.jpg` (t=22:48)
  `/tmp/watch-klx0yrn8/frames/frame_0056.jpg` (t=23:14)
  `/tmp/watch-klx0yrn8/frames/frame_0057.jpg` (t=23:39)
  `/tmp/watch-klx0yrn8/frames/frame_0058.jpg` (t=24:04)
  `/tmp/watch-klx0yrn8/frames/frame_0059.jpg` (t=24:30)
  `/tmp/watch-klx0yrn8/frames/frame_0060.jpg` (t=24:55)
  `/tmp/watch-klx0yrn8/frames/frame_0061.jpg` (t=25:20)
  `/tmp/watch-klx0yrn8/frames/frame_0062.jpg` (t=25:46)
  `/tmp/watch-klx0yrn8/frames/frame_0063.jpg` (t=26:11)
  `/tmp/watch-klx0yrn8/frames/frame_0064.jpg` (t=26:36)
* `/tmp/watch-klx0yrn8/frames/frame_0065.jpg` (t=27:02)
  `/tmp/watch-klx0yrn8/frames/frame_0066.jpg` (t=27:27)
  `/tmp/watch-klx0yrn8/frames/frame_0067.jpg` (t=27:52)
  `/tmp/watch-klx0yrn8/frames/frame_0068.jpg` (t=28:18)
  `/tmp/watch-klx0yrn8/frames/frame_0069.jpg` (t=28:43)
  `/tmp/watch-klx0yrn8/frames/frame_0070.jpg` (t=29:08)
  `/tmp/watch-klx0yrn8/frames/frame_0071.jpg` (t=29:34)
  `/tmp/watch-klx0yrn8/frames/frame_0072.jpg` (t=29:59)
  `/tmp/watch-klx0yrn8/frames/frame_0073.jpg` (t=30:24)
  `/tmp/watch-klx0yrn8/frames/frame_0074.jpg` (t=30:50)
  `/tmp/watch-klx0yrn8/frames/frame_0075.jpg` (t=31:15)
  `/tmp/watch-klx0yrn8/frames/frame_0076.jpg` (t=31:40)
  `/tmp/watch-klx0yrn8/frames/frame_0077.jpg` (t=32:06)
  `/tmp/watch-klx0yrn8/frames/frame_0078.jpg` (t=32:31)
  `/tmp/watch-klx0yrn8/frames/frame_0079.jpg` (t=32:56)
  `/tmp/watch-klx0yrn8/frames/frame_0080.jpg` (t=33:22)
