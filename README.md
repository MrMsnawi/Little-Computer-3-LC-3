# Little Computer 3 (LC-3) Virtual Machine

![Status](https://img.shields.io/badge/Status-Work_in_Progress-yellow) ![Language](https://img.shields.io/badge/Language-C++-blue) ![Focus](https://img.shields.io/badge/Focus-System_Internals-red)

## 📖 Overview
This project is a software implementation of the **LC-3 (Little Computer 3)** architecture, written in C++. 

The goal of this project is to simulate a complete computer system—including memory management, register states, and instruction execution—entirely in software. By building the "hardware" via code, I am exploring the fundamental concepts of how computers process binary instructions, a critical first step towards mastering **Reverse Engineering** and **Kernel Exploitation**.

## 🧠 Architecture Concepts
The LC-3 is a simplified Von Neumann architecture widely used for teaching system internals. This VM simulates the following hardware components:

### 1. Memory Storage
*   Simulates **65,536 memory locations** (16-bit address space).
*   Implements the logic for storing instructions and data in a linear array, mimicking physical RAM.

### 2. The CPU (Central Processing Unit)
*   **Registers:** Implementation of 10 hardware registers (8 General Purpose, 1 Program Counter, 1 Condition Flag).
*   **The Loop:** A custom implementation of the **Fetch-Decode-Execute** cycle that drives all computing.
*   **Opcodes:** Handling of the LC-3 instruction set (ADD, AND, NOT, BR, JMP, etc.) through bitwise manipulation.

### 3. Trap Routines (System Calls)
*   Simulation of hardware interrupts and I/O operations.
*   Interacts with the host terminal to handle keyboard input (GETC) and screen output (PUTS), mimicking how an OS kernel handles drivers.

## 🛠️ Project Roadmap
This project is currently under active development.

- [x] **Project Skeleton:** Memory and Register structures defined.
- [ ] **Instruction Parsing:** Logic to decode 16-bit binary opcodes.
- [ ] **Execution Engine:** Implementation of arithmetic and control flow instructions.
- [ ] **I/O Handling:** Input buffering and terminal output.
- [ ] **Integration Test:** Running the game **"2048"** (compiled for LC-3) inside this VM.

## 🎯 Why this Project?
As an aspiring **Reverse Engineer**, understanding the abstraction layers of a computer is vital. This project forces me to deal with:
*   **Bitwise Operators:** Manually extracting opcode bits and flags (`<<`, `>>`, `&`, `|`).
*   **Endianness:** Handling Big-Endian to Little-Endian conversion.
*   **Control Flow:** Understanding how `if` statements and function calls work at the assembly level.

## 🚀 Building & Running
*Instructions will be added as the project nears completion.*

---

*"What I cannot create, I do not understand." — Richard Feynman*
