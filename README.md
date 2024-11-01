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









