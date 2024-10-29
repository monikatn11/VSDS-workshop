 # VSDSquadronMini Research Internship - 20th October Cohert
<p>
The program is based on RISC-V architecture and uses open-source tools to teach people about VLSI and RISC-V
</p>

<li>Instructor: Kunal Ghosh</li>
<li> Student Name: Monika T N</li>
<li> College Name:BMS COLLEGE OF ENGINEERING,BENGALURU.</li>
<details>
 <summary>
 <h2> TASK-1 </h2> 
<h2>Installation of RISC-V toolchain using VDI. Uploading the snapshot of complied code and RISC-V Objdmp on GitHub.</h2>
 </summary>
The task 1 includes completion of the following instructions
<br>
<ol>
  <li> Creating GitHub repo. </li>
  <li> Installation of Oracle VirtualBox. </li>
  <li> Installation of RISC-V toolchain using VDI. </li>
  <li> Writing C program to find sum of n numbers. </li>
  <li> Using RISC-V Simulator for compiling and running the code. </li>
  <li> Uploading the snapshots in Github. </li>
</ol>
<h4>
  STEPS:
  <br>
  <OL>
    <li>
      Open ubuntu in VirtualBox.
    </li>
   <img src="task1.png">
      
   <br>
      <li>Home screen of Ubuntu.</li>
      <img src="task1 (3).png">
    <br>
      <li>Write the C program for sum of one to n in newfile and run the code in terminal.</li>
      <img src= "task1 (4).png" > <br>
      <li>Run command riscv64-unknown-elf-objdump -d sum1ton.o </li>
      <img src="task1 (5).png"> <br>
      <li>Search the main.</li>
       <img src="taskk1.jpeg">
        <img src="taskk1 (2).jpeg">
</OL>
</h4>
</details>


<details>
<summary>
 <h2>TASK-2</h2>
</b> <h2>Performing SPIKE Simulation and Debugging a simple C code with Interactive Debugging Mode using Spike</h2>
</summary> 
  
### What is SPIKE in RISCV?
> * A RISC-V ISA is a simulator, enabling the testing and analysis of RISC-V programs without the need for actual hardware.  
> * Spike is a free, open-source C++ simulator for the RISC-V ISA that models a RISC-V core and cache system. It can be used to run programs and a Linux kernel, and can be a starting point for running software on a RISC-V target.  
  
 ### What is pk (Proxy Kernel)?  
> * The RISC-V Proxy Kernel, pk , is a lightweight application execution environment that can host statically-linked RISC-V ELF binaries.  
> * A Proxy Kernel in the RISC-V ecosystem simplifies the interaction between complex hardware and the software running on it, making it easier to manage, test, and develop software and hardware projects.  
 


### Testing the SPIKE Simulator  
The target is to run the ```sum1ton.c``` code using both ```gcc compiler``` and ```riscv compiler```, and both of the compiler must display the same output on the terminal. 

### Debug the task 1 code using SPIKE
<li> To use SPIKE and debug sum 1 to n c program </li><br>
<img src="task2 (2).png">
<img src="task2.png">


### Write a simple C program for any simple application and compile with RISC-V GCC/SPIKE.
<li>Write the C program to find largest number in 3 numbers in newfile and run the code in terminal.</li>
<img src ="task2 (3).png"><br>

<li>And to compile the code using **riscv compiler**, use the following command: </li><br>
<img src="task2 (3.1).png"><br>
<li>Search the main.</li>
       <img src="task2 (4).png">
        <img src="task2 (5).png">
 
</details>

<details>
<summary>
 <h2>TASK-3</h2><br>
</b><h2> RISC-V Instruction types & 32-Bit Instruction code
</summary>

<h3>What is RISC-V?</h3>
<p>RISC-V is an exciting and innovative open-source instruction set architecture (ISA) that enables developers to create custom processors tailored to specific applications. This means that anyone can design and implement their processors without needing to pay for expensive licenses, making RISC-V a popular choice in both academia and industry.</p>


<h2>Instruction Formats in RISC-V</h2>
RISC-V organizes its machine language instructions into six distinct formats, each optimized for different types of operations. Here’s a breakdown of each format:

<h2>R-Type Instructions:</h2>

<p>Used primarily for arithmetic and logical operations.
Structure: Each instruction is 32 bits long and includes:
Opcode (7 bits): Indicates the type of operation.
rd (5 bits): The destination register where the result is stored.
func3 (3 bits): Specifies the operation type (e.g., add, subtract).
rs1 (5 bits): The first source register.
rs2 (5 bits): The second source register.
func7 (7 bits): Provides additional details about the operation.</p>

<h2>I-Type Instructions:</h2>

What It Is: Involves operations that use registers and immediate values (constants).
Structure:
Opcode (7 bits): Identifies the instruction type.
rd (5 bits): The destination register.
func3 (3 bits): Operation type.
rs1 (5 bits): The source register.
imm (12 bits): A signed immediate value (replaces rs2 and func7 from R-Type).

<h2>S-Type Instructions:</h2>

What It Is: Used to store data from registers to memory.
Structure:
Opcode (7 bits): Indicates the operation.
imm (12 bits): Split into two parts for memory address calculation.
rs1 (5 bits): The source register containing the value to be stored.
func3 (3 bits): Defines the type of store operation (byte, half-word, etc.).

<h2>B-Type Instructions:</h2>

What It Is: Used for branching and control flow based on conditions.
Structure:
Opcode (7 bits): Defines the instruction type.
imm (12 bits): Encodes the branch offset.
rs1 (5 bits) and rs2 (5 bits): Source registers used in the branching condition.
func3 (3 bits): Specifies the branch condition.

<h2>U-Type Instructions:</h2>

What It Is: Designed to load immediate values into registers.
Structure:
Opcode (7 bits): Specifies the instruction.
Consists mainly of two instructions: LUI (Load Upper Immediate) and AUIPC (Add Upper Immediate to PC).
Example: lui x15, 0x13579 would load the value into the upper half of register x15.

<h2>J-Type Instructions:</h2>

 Used for jump operations, allowing the program to change its execution flow.
Structure:
Opcode (7 bits): Indicates a jump instruction.
imm (20 bits): The immediate value determining where to jump.
Primarily consists of the JAL (Jump and Link) instruction, often used in loops and function calls.













 
</details>
