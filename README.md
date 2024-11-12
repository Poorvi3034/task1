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

***
***
***
 ## TASK 5 
 ## MINI PROJECT

 ##  Burgler Alarm
In today’s world of IoT devices, CCTV cameras are widely used for surveillance, but they come with challenges such as complex installation, reliance on internet connectivity, high memory consumption, and privacy concerns in private areas. To address this, there’s a need for a simpler, more efficient security solution.

The Advanced Easy to Use Burglar Alarm uses an ultrasonic radar sensor to detect movement and alerts users with a passive buzzer when trespassing occurs. Unlike laser-based systems, this device is easy to install and requires minimal setup, just needing placement perpendicular to a solid surface. It features an auto-adjust function that measures distance and sets a detection threshold, with the device working on just 5V DC power.

## Components Required

VSD Squadron Mini developement board
Male USB C Cable
HC-SR04 Ultrasonic Sensor
Bread Board
Male to Male; Male to Female jumper cable
Red LED
Passive Buzzer
220 Ohm Resistor
Toggle Switch



## Circuit Diagram


![WhatsApp Image 2024-11-12 at 1 58 14 PM](https://github.com/user-attachments/assets/bd2b8812-44a6-41d0-96f7-27532f9118d2)

HC-SR04 Ultrasonic Sensor:

VCC connects to 5V on the VSD Squadron Mini.
Trig connects to PD3 on the VSD Squadron Mini.
Echo connects to PD2 on the VSD Squadron Mini.
Gnd connects to Gnd on the VSD Squadron Mini.
LED with Resistor:

The positive leg (+) of the LED connects to PD4 on the VSD Squadron Mini.
The negative leg (–) of the LED connects through a 220Ω resistor to Gnd.
Buzzer:

Pin 1 of the buzzer connects to PC7 on the VSD Squadron Mini.
Pin 2 of the buzzer connects to Gnd.
Button Switch:

Pin 1 of the button connects to 5V.
Pin 2 of the button connects to PC3 on the VSD Squadron Mini.

## code

#include "debug.h"

uint16_t distance;
uint16_t press;

void Input_Capture_Init(uint16_t arr, uint32_t psc)
{
    GPIO_InitTypeDef        GPIO_InitStructure = {0};
    TIM_ICInitTypeDef       TIM_ICInitStructure = {0};
    TIM_TimeBaseInitTypeDef TIM_TimeBaseInitStructure = {0};
    NVIC_InitTypeDef        NVIC_InitStructure = {0};

    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD | RCC_APB2Periph_GPIOC | RCC_APB2Periph_TIM1, ENABLE);

    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_2;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPD;
    GPIO_Init(GPIOD, &GPIO_InitStructure);
    GPIO_ResetBits(GPIOD, GPIO_Pin_2);
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_3;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPD;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_3 | GPIO_Pin_4;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOD, &GPIO_InitStructure);

    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_7;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    TIM_TimeBaseInitStructure.TIM_Period = arr;
    TIM_TimeBaseInitStructure.TIM_Prescaler = psc;
    TIM_TimeBaseInitStructure.TIM_ClockDivision = TIM_CKD_DIV1;
    TIM_TimeBaseInitStructure.TIM_CounterMode = TIM_CounterMode_Up;
    TIM_TimeBaseInitStructure.TIM_RepetitionCounter = 0x00;
    TIM_TimeBaseInit(TIM1, &TIM_TimeBaseInitStructure);
     TIM_ICInitStructure.TIM_Channel = TIM_Channel_1;
    TIM_ICInitStructure.TIM_ICPrescaler = TIM_ICPSC_DIV1;
    TIM_ICInitStructure.TIM_ICFilter = 0x00;
    TIM_ICInitStructure.TIM_ICPolarity = TIM_ICPolarity_Rising;
    TIM_ICInitStructure.TIM_ICSelection = TIM_ICSelection_DirectTI;

    TIM_PWMIConfig(TIM1, &TIM_ICInitStructure);

    NVIC_InitStructure.NVIC_IRQChannel = TIM1_CC_IRQn;
    NVIC_InitStructure.NVIC_IRQChannelPreemptionPriority = 0;
    NVIC_InitStructure.NVIC_IRQChannelSubPriority = 1;
    NVIC_InitStructure.NVIC_IRQChannelCmd = ENABLE;
    NVIC_Init(&NVIC_InitStructure);

    TIM_ITConfig(TIM1, TIM_IT_CC1 | TIM_IT_CC2, ENABLE);

    TIM_SelectInputTrigger(TIM1, TIM_TS_TI1FP1);
    TIM_SelectSlaveMode(TIM1, TIM_SlaveMode_Reset);
    TIM_SelectMasterSlaveMode(TIM1, TIM_MasterSlaveMode_Enable);
    TIM_Cmd(TIM1, ENABLE);
}

uint16_t pressed(void){
    if(GPIO_ReadInputDataBit(GPIOC,GPIO_Pin_3)==1){
        Delay_Ms(500);
        GPIO_WriteBit(GPIOC,GPIO_Pin_7,SET);
        Delay_Ms(100);
        GPIO_WriteBit(GPIOC,GPIO_Pin_7,RESET);
        Delay_Ms(1000);
        press=!press;
    }
    return press;
}

int main(void)
{
    SystemCoreClockUpdate();
    Delay_Init();
    USART_Printf_Init(115200);
    Input_Capture_Init(0xFFFF, 48 - 1);
    uint32_t count=0;
    uint32_t value=0;
    uint16_t avg=0;
    while (pressed())
    {     
        GPIO_WriteBit(GPIOD, GPIO_Pin_3, SET);
        Delay_Us(10); 
        GPIO_WriteBit(GPIOD, GPIO_Pin_3, RESET);
        if(count<=4000){
            count+=1;
            GPIO_WriteBit(GPIOD,GPIO_Pin_4,SET);
            value+=distance;
            Delay_Ms(1);
        }else if(count==4001){
            avg = value/count;
            GPIO_WriteBit(GPIOC,GPIO_Pin_7,SET);
            Delay_Ms(100);
            GPIO_WriteBit(GPIOC,GPIO_Pin_7,RESET);
            Delay_Ms(100);
            GPIO_WriteBit(GPIOC,GPIO_Pin_7,SET);
            Delay_Ms(100);
            GPIO_WriteBit(GPIOC,GPIO_Pin_7,RESET);
            Delay_Ms(100);
            count+=1;
        }else if(count>4001 && count<4050){
            count+=1;
            Delay_Ms(1);
        }else{
            GPIO_WriteBit(GPIOD,GPIO_Pin_4,RESET);
            if(distance<avg-10 || distance>avg+10){
                count=0;
                while(pressed()){
                    GPIO_WriteBit(GPIOC,GPIO_Pin_7,SET);
                    GPIO_WriteBit(GPIOD,GPIO_Pin_4,SET);
                    Delay_Ms(500);
                    GPIO_WriteBit(GPIOC,GPIO_Pin_7,RESET);
                    GPIO_WriteBit(GPIOD,GPIO_Pin_4,RESET);
                    Delay_Ms(500);
                }
            }
        }  
    }
}

void TIM1_CC_IRQHandler(void) __attribute__((interrupt("WCH-Interrupt-fast")));

void TIM1_CC_IRQHandler(void)
{
    if (TIM_GetITStatus(TIM1, TIM_IT_CC1) != RESET)
    {
        TIM_SetCounter(TIM1,0);
    }

    if (TIM_GetITStatus(TIM1, TIM_IT_CC2) != RESET)
    {
        uint32_t duration = TIM_GetCapture1(TIM1);
        distance = duration*0.034/2;
        printf("%d\n",distance);
        
    }

    TIM_ClearITPendingBit(TIM1, TIM_IT_CC1 | TIM_IT_CC2);
}

 

    



   
            





## Key Features
1. Easy Installation: Requires minimal setup; simply place it perpendicular to a solid surface, with 5v DC connection.
2. Auto-Adjust Feature: Automatically calibrates the detection threshold within 10 seconds of being turned on.
3. Adaptable Range: Can be placed between 0.1- 4 meters from the detection surface.
4. Low Power Consumption: Designed to operate efficiently with just 5V DC power which can be provided from a 5V adapter or a Battery bank.
5. Privacy-Friendly: Suitable for use in private rooms without violating privacy.











 







                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             









