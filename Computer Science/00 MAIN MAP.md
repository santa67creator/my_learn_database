# 🗺️ 00 MAIN MAP

> [!abstract] Main map
> All the structure in one place: from the basics of a computer to how the processor works. Go from top to bottom through the levels, within each level the notes are in reading order.

---

## 🟢 Level 1: BEGIN

> [!tip] Start here
> If you are a beginner and want to understand how a computer works, read all the PDFs from [[ICT MAIN PAGE]] first.

| Note | What about |
|---------|-------|
| [[ICT MAIN PAGE]] | 6 lectures on ICT (PDF): computer, OS, HCI, databases, networks, internet |

---

## 🟡 Level 2: memory – [[MEMORY CHAPTER]]

> [!info] What's inside
> How a computer stores data: RAM, byte order, data types and how programming languages work with memory.

### 💽 Memory and RAM

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[Memory]] | what is memory: registers, cache, RAM, HDD/SSD |
| 2 | [[RAM]] | cells, bits and bytes, how addressing works |
| 3 | [[RAM Size]] | what does memory size depend on: why does a 32-bit system see only 4 GB |
| 4 | [[RAM Addressing]] | byte and word addressing |

### 💾 [[MEMORY CORE]]

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[Big-Endian and Little-Endian]] | memory byte order |
| 2 | [[Memory Alignment]] | **where exactly** to place data in memory |
| 3 | [[Various Data Types]] | types determine content and amount of space |
| 4 | [[Storing Negative Integers (Two’s Complement)]] | how works negative numbers in pc |

### 🧩 [[Language Structure]]

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[Primitive Data Types]] | **primitive types**, copied by value |
| 2 | [[Reference Data Types and Arrays]] | arrays and reference types |
| 3 | [[Unused Memory]] | how to move and remove garbage in memory |

---

## 🔴 Level 3: how the processor works - [[CPU CORE]]

> [!info] What's inside
> What is a processor, what architectures and registers it has, how it executes commands and in what modes it operates.

### ⚙️ Processor

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[CPU CORE]] | what is a processor (CPU), the problem of translation and backward compatibility |
| 2 | [[x86 vs ARM vs AVR]] | x86 for PCs and servers, ARM for phones, AVR for microcontrollers |
| 3 | [[Bitness and Word Size]] | machine word and bit depth (16 / 32 / 64 bits) |

### 🗃️ Registers

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[REGISTERS]] | small memory cells on the processor itself, the fastest memory |
| 2 | [[Why Byte Addressing Is Faster]] | why byte addressing is faster than verbal addressing |
| 3 | [[General-Purpose Registers]] | general purpose registers, they are used by the programmer |
| 4 | [[Special-Purpose Registers]] | segment, stack (BP, SP), FLAGS |
| 5 | [[Register Overflow]] | what happens if the number does not fit into the register |

### 🚦 Teams and modes

| # | Note | What about |
|:-:|---------|-------|
| 1 | [[Opcodes]] | a command is a number of several bytes, by which the processor understands what to do |
| 2 | [[Program Counter]] | what happens after switching on: BIOS, loading the first sector |
| 3 | [[Processor Operating Modes]] | address translation and processor operating modes |
| 4 | [[Protected Mode]] | empty note for now |