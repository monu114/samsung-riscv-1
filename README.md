# Samsung-RISCV
The program is centered around the RISC-V architecture and leverages open-source tools to provide hands-on learning in VLSI chip design and RISC-V concepts. The internship is guided by the esteemed instructor, Mr. Kunal Ghosh.

## Profile Overview

Name: G S Monish Yadav

College: Vidyavardhaka College of Engineering

Email ID: monishyadav@zohomail.in

GitHub Profile: monu112004

LinkedIn Profile: www.linkedin.com/in/g-s-monish-yadav-23262b266

<details>
<summary><b>Task 1:</b> Task 1: Review lab videos on C programming and RISC-V architecture. Perform the task of compiling C code using both the GCC compiler and the RISC-V compiler, demonstrating an understanding of the compilation process for each.simulator</summary>   
<br>

## C and RISC-V Based Labs

This repository demonstrates the processes involved in compiling C programs and generating assembly code using both a standard GCC compiler and a RISC-V GCC compiler. It includes comprehensive steps and explanations to guide users through each stage of the compilation and debugging workflow.

## C Language-Based Lab

### Steps to Compile a .c File on Your Machine:

1. Open the bash terminal and navigate to the directory where you want to create your file.
2. Use the following command to create and edit a new .c file:
   ```sh
   gedit sum_1ton.c
![3](https://github.com/user-attachments/assets/0e762cb5-cbdf-495e-aaec-0dea9aae3aa1)

### Steps to Compile a .c File on Your Machine:
 ```sh
 gcc sum_1ton.c
 ./a.out
 # Compilation and execution complete.
 ```
![2](https://github.com/user-attachments/assets/5712cf49-d372-467e-9ace-425a3741b7b4)
## RISC-V Based Lab

### Steps to Compile Using RISC-V GCC Compiler:
1. Ensure the RISC-V GCC compiler is installed and accessible on your system.
2. Verify the .c file contents using the cat command:
``` sh
cat sum_1ton.c
```
3. Compile the C program for RISC-V architecture using:
``` sh
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
```
4. Disassemble the object file to view its assembly code using:
``` sh
riscv64-unknown-elf-objdump -d sum_1ton.o
```
5. Use /main in the terminal to locate the main function in the assembly output.
![4](https://github.com/user-attachments/assets/abbb078b-bee3-452d-9e04-0f0d61ba42bf)
### Explanation of Key Commands and Options: 
1. -mabi=lp64: Specifies the Application Binary Interface (ABI) for 64-bit integers, pointers, and long data types, suitable for 64-bit RISC-V architecture.

2. -march=rv64i: Indicates the 64-bit RISC-V base integer instruction set architecture.

3. -O1: Enables basic optimization for better performance without significantly increasing compilation time.

4. riscv64-unknown-elf-objdump: A tool for disassembling RISC-V binaries to examine the code structure and debug it effectively.
</details>

<details>   
<summary><b>Task 2:</b> Task is to refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler simulator</summary>   
<br>
   
#  RISC-V ISA Simulation with SPIKE and Proxy Kernel (pk)
This repository provides instructions for setting up and using SPIKE, a RISC-V ISA simulator, along with the Proxy Kernel (pk) for program execution. Follow the steps below to install the necessary tools, run simulations, and debug RISC-V programs effectively.

##  What is SPIKE?
SPIKE is an open-source RISC-V ISA simulator written in C++. It emulates a RISC-V core and cache system, enabling developers to test RISC-V programs without hardware. SPIKE supports running standalone programs as well as operating systems like Linux

## Testing the SPIKE Simulator
To validate the setup, compile and execute a sample program (sum_1ton.c) using both the GCC and RISC-V compilers.
### Using GCC Compiler:
``` sh
gcc product.c  
./a.out
```
![VirtualBox_vsdworkshop_13_01_2025_20_43_22](https://github.com/user-attachments/assets/e20f695b-6839-42d1-9f3f-7835fb7b8d7f)

### Using RISC-V Compiler:
``` sh
spike pk product.o
```
## Analyzing the Assembly Code
### Objdump Analysis:
Generate the assembly code with the following command:
``` sh
riscv64-unknown-elf-objdump -d sum_1ton.o | less
```
![VirtualBox_vsdworkshop_13_01_2025_20_43_47](https://github.com/user-attachments/assets/04a7db80-2d33-42ed-bafd-77a29c09d413)

### Debugging with SPIKE:
1. Open the debugger using the command:
``` sh
spike -d pk product.o
```
2. Perform debugging operations in the terminal.
   
## Optimization Levels
Snapshots of RISC-V objdump at different optimization levels (-O1 and -Ofast) provide insights into how compiler optimizations affect the generated assembly code. Use these options during compilation to analyze the differences:

-O1 Optimization

-Ofast Optimization

![VirtualBox_vsdworkshop_13_01_2025_20_42_05](https://github.com/user-attachments/assets/68908728-8b0a-405b-8b9c-19f3cc09741b) 

