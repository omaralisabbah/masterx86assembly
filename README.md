🧭 Full Roadmap for Learning x86 Assembly Language
1. Foundations (Prerequisites)

Before learning x86 assembly, make sure you understand:

✅ 1.1 Computer Architecture Basics

What is a CPU?

ALU, registers, control unit

Memory hierarchy (RAM, cache, disk)

How instructions execute (fetch-decode-execute cycle)

Endianness (little vs. big)

✅ 1.2 Number Systems

Binary, Hexadecimal

Two’s complement

Bitwise operations (AND, OR, XOR, shifts)

✅ 1.3 Operating System Basics

Processes, system calls

User vs Kernel mode

Stack & heap

Milestone: You should understand how data moves through a CPU.
2. Environment Setup

Choose which environment you will learn:

Option A — Linux (recommended)

Tools: nasm, ld, gdb

Editor: VSCode or Vim

Install NASM:
sudo apt install nasm

Option B — Windows

MASM (Microsoft Assembler) OR

WinASM / Visual Studio MASM

Option C — Cross-Platform

Use Intel SDE or qemu

Online assemblers: Godbolt (Compiler Explorer)

Milestone: You can assemble, link, and run a simple “Hello World”.
3. x86 Architecture Essentials
3.1 Registers

Learn 32-bit first (x86), then 64-bit (x86-64).

32-bit registers

General purpose: EAX, EBX, ECX, EDX

Pointer & index: ESI, EDI, EBP, ESP

EIP instruction pointer

EFLAGS flags

64-bit registers (if using x86-64)

RAX, RBX, … R15

RIP

RFLAGS

3.2 Memory

Addressing modes (direct, indirect, scaled index)

Stack layout & calling conventions

Alignment & segmentation

Milestone: You can read and predict what a short piece of assembly code does.
4. Assembly Language Syntax

Learn Intel syntax first (more readable), optionally AT&T later.

4.1 Basic Instructions

Data Movement: mov, lea, push, pop

Arithmetic: add, sub, mul, div, inc, dec

Logic: and, or, xor, not, shl, shr

Control flow: jmp, cmp, je, jne, jg, jl

Stack instructions: call, ret

4.2 Directives

NASM: section .text, global _start, db, dw, etc.
MASM: .data, .code

Milestone: Write a program that takes console input, processes it, and prints output.
5. System Calls & OS Interaction
5.1 Linux (x86 / x86-64) Syscalls

Using int 0x80 (32-bit) or syscall (64-bit):

Examples:

write

read

open, close

mmap

5.2 Windows Syscalls / WinAPI

Using call to WinAPI functions

Kernel32.dll (e.g., CreateFileA)

Stdcall calling convention

Milestone: You can write assembly programs that interface with the OS filesystem and process input/output.
6. Functions & Calling Conventions

Learn calling conventions because they are essential for mixing C and assembly.

6.1 x86 32-bit

cdecl

stdcall

fastcall

6.2 x86-64

System V AMD64 ABI (Linux, macOS)

Microsoft x64 calling convention

Know:

Parameter passing (registers/stack)

Return values

Stack frame (prologue & epilogue)

Milestone: Write assembly functions callable from C, and call C functions from assembly.
7. Advanced Topics
7.1 Floating Point & Multimedia

x87 FPU instructions

SIMD: SSE, SSE2–SSE4

AVX (if 64-bit)

7.2 Optimization

Loop unrolling

Instruction pipelining

Cache-aware programming

Aligning data

7.3 Memory & Interrupts

BIOS interrupts (real mode)

Hardware interaction

Inline assembly in C/C++

7.4 Reverse Engineering

Use tools: Ghidra, IDA, Radare2

Understand compiler-generated assembly

Milestone: Analyze an executable and reconstruct high-level logic.
8. Specialization Paths

Choose how you want to use x86 assembly:

Path A — Systems Programming

OS development

Bootloaders

Drivers

Learning real mode, protected mode, paging

Projects:

Build your own bootloader

Write a tiny operating system kernel

Path B — Reverse Engineering / Security

Malware analysis

Writing shellcode

Anti-debugging techniques

Projects:

Crack a simple binary

Write custom shellcode

Path C — High-Performance Optimization

SIMD-heavy code

Scientific computing

Game engine optimization

Projects:

Optimize matrix multiplication

Write a high-speed string library

9. Final Mastery Level

To be an expert:

Read Intel® 64 and IA-32 Manuals (Vol 1–3)

Study compiler assembly output from Clang/GCC/MSVC

Write hybrid C/ASM code

Build a complete x86 emulator/interpreter

Understand the microarchitecture (pipeline stages, uops, reorder buffer)

10. Recommended Resources
Beginner-Friendly

“Programming From the Ground Up”

“Intel x86 Assembly Language and Architecture”

“PC Assembly Language” by Paul Carter

Intermediate

Intel & AMD official manuals

“Reverse Engineering for Beginners” by Dennis Yurichev

Advanced

Agner Fog’s optimization manuals

AMD64 ABI documentation
