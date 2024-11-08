## VSDSquadron-Research-Internship-2024

The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.

***

## Installation
oracle virtual machine
![image](https://github.com/user-attachments/assets/83714547-fc42-42ff-9e83-9a4f94d53d9c)

gedit editor
![image](https://github.com/user-attachments/assets/09e08fa2-d4be-48f1-90d2-081729d068ee)

***

## steps

1. open gedit editor and write c code to find the sum of n number
![image](https://github.com/user-attachments/assets/4f4a3266-f931-4954-9a72-cd3d83662f5e)

2.compile the above code using gcc and get the required output
![image](https://github.com/user-attachments/assets/e9cdacf7-cb34-4fa8-a0a4-059ee4b5a700)

3. compile and run the same code using the risc-v simulator and search for main using a command:"riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main"

![image](https://github.com/user-attachments/assets/e1fc99d2-6e55-4ef7-9006-9db96f3d27f1)

4. changing it from o1 to ofast and search for main use of commands: "riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main"


![image](https://github.com/user-attachments/assets/79c3a328-ba28-4208-ad67-14c8fb1b9ad1)

***
***
***

## TASK 2 

## A. SPIKE simulation and observation with -o1 and -ofast 

## STEPS
1. The C code of TASK 1

![image](https://github.com/user-attachments/assets/e9cdacf7-cb34-4fa8-a0a4-059ee4b5a700)

2. -ofast output using riscv simulator

![Screenshot 2024-10-24 094029](https://github.com/user-attachments/assets/99830a20-f888-4628-aab8-9294084c29b1)

3. confirm the same using SPIKE

![Screenshot 2024-10-27 194935](https://github.com/user-attachments/assets/73c0a1f2-9e4f-44c1-837f-258f2e067abd)

***
***

## B. write a simple c program for any simple application and risc-v GCC/ SPIKE

## STEPS 
 I chose a simple C program that prints all the prime number from 1 to 100
 it loops from 2 to 100. The inner loop checks for the factors of the current number . If any number between 2 and the square root of the current nyumber divides it evenly, its not prime number.

![Screenshot 2024-10-28 195644](https://github.com/user-attachments/assets/f1083b48-3f9c-4953-bcb0-ada28fa59015)

compile using GCC


![Screenshot 2024-10-28 201122](https://github.com/user-attachments/assets/688cb76f-15ee-48ca-a599-078662903d12)

Compile using riscv

![image](https://github.com/user-attachments/assets/95ddf564-885d-431a-a9ba-e4c4b141bf86)


![Screenshot 2024-10-28 203203](https://github.com/user-attachments/assets/c5697747-c7e5-4e4c-bb64-7376047a4257)


compile using SPIKE

![Screenshot 2024-10-28 213910](https://github.com/user-attachments/assets/de09b867-a337-4fa5-a16e-09ffbf1d0ce0)

![Screenshot 2024-10-28 213938](https://github.com/user-attachments/assets/3553fbc6-b68d-4cb4-851b-4c1bb87cd8d8)

***
***
***

## TASK 3
***
## RISC-V Instruction Types (R,I,S,B,U,J):

 In RISC-V architecture, instructions are classified into different instruction types based on their format and usage. There are six main instruction types: R-type, I-type, S-type, B-type, U-type, and J-type. Each type has a different purpose and layout in the instruction format.  
 
## 1. R-type (Register)
Purpose: Used for operations that involve registers, such as arithmetic or logic operations between two registers.

opcode: Operation code (6 bits)

rd: Destination register (5 bits)

rs1: First source register (5 bits)

rs2: Second source register (5 bits)

funct3: Function code (3 bits)

funct7: Additional function code (7 bits)

***

## 2. I-type (Immediate)
Purpose: Used for operations involving an immediate value (constant) and a register.

opcode: Operation code (7 bits)

rd: Destination register (5 bits)

rs1: Source register (5 bits)

imm: Immediate value (12 bits)

***


## 3. S-type (Store)
Purpose: Used for store operations, where data is stored from a register to memory.

opcode: Operation code (7 bits)

rs1: Base register (5 bits)

rs2: Source register (5 bits)

funct3: Function code (3 bits)

imm: Immediate value (12 bits, split into two parts)

***


## 4.B-type (Branch)
Purpose: Used for branch operations, which control program flow based on conditions (e.g., branch if equal, branch if less than).

opcode: Operation code (7 bits)

rs1: First register (5 bits)

rs2: Second register (5 bits)

funct3: Function code (3 bits)

imm: Immediate value (12 bits, split into multiple fields)

***

## 5. U-type (Upper Immediate)
Purpose: Used for instructions that operate on an immediate value, especially for setting a large immediate value in the upper 20 bits.

opcode: Operation code (7 bits)

rd: Destination register (5 bits)

imm: Immediate value (20 bits)

***

## 6. J-type (Jump)
   
Purpose: Used for jump operations, which are typically used to perform unconditional jumps (like a function call or returning from a function).

opcode: Operation code (7 bits)

rd: Destination register (5 bits, typically used for the return address in some instructions)

imm: Immediate value (20 bits, split into multiple fields)

 ***
 ***



## 15 Unique Instructions and Their 32-bit Machine Code                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    
![image](https://github.com/user-attachments/assets/86bca67e-d5a3-49b2-b253-b3f5d952c9d9)

***
***
***
## TASK 4
## Use this RISC-V core verilog netlist and testbench for functional simulation experiment and upload waveform
***NOTE:** Since the designing of RISCV Architecture and writing it's testbench is not the part of this Research Internship, so we will use the Verilog Code and Testbench of RISCV that has already been designed. The reference GitHub repository is : [iiitb_rv32i] https://github.com/vinayrayapati/rv32i/blob/main/iiitb_rv32i.v
## steps 
1. create a directory

   
2. create a files using 'touch' command

![Screenshot 2024-11-08 225143](https://github.com/user-attachments/assets/050cf959-2992-42cd-94c3-886a35735609) 


3. Copy the code from the reference github repo and paste it in your verilog and testbench files.
   
![Screenshot 2024-11-08 233152](https://github.com/user-attachments/assets/3727fa4f-a0f1-462f-9816-85b9594372eb) 

![Screenshot 2024-11-08 233329](https://github.com/user-attachments/assets/6fc30d5f-6dc9-4c35-841a-0dde951d0455) 


4. enter the simulation command for verilog code and for waveform in GTKWave
   
$ iverilog -o task_rv32i task_rv32i.v task_rv32i_tb.v 

$ ./task_rv32i

$ gtkwave task_rv32i.vcd


5. the GTKWave will be opened and output waveform of various instructions that we have covered in TASK -2
![Screenshot 2024-11-08 232819](https://github.com/user-attachments/assets/8e8c5ec9-66af-424f-a235-ff08596f2963)
 







                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             









