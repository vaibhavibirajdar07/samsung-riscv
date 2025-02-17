# samsung-riscv
##  Basic Details

*Name:* Vaibhavi Birajdar  
*College:* KLE Institue of Technology  
*Email ID:* vaibhavibirajdar25@gmail.com  
*GitHub Profile:* [Vaibhavi_Birajdar_Github](https://github.com/vaibhavibirajdar07)  
*LinkedIN Profile:* [Vaibhavi Birajdar](https://www.linkedin.com/in/vaibhavi-birajdar-915650258/)

----------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 1:</b>Task is to  refer to C based and RISCV based lab videos and execute the task of compiling the C code using gcc and riscv compiler</summary><br>



### C Language based LAB
I have successfully run the virtual machine and compiled the tasks.

Initial task is:-

### write a program to compile the sum of first 5 natural numbers in c:

we have written the code sum of 1st 5 numbers in leafpad as shown below.

```
gcc sum_1ton.c

./a.out
```

this code will be run in terminal to get output as 15 for 1st 5 numbers as shown below :


![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/C%20Code%20compiled%20on%20gcc%20Compiler.png)

### RISCV based LAB

1. Using the cat command, the entire C code will be displayed on the terminal.
   
![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/cat%20Command.png)

2. A program is run to obtain risc-v version of the code previously written in c:

  	```
	riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
	```

![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/RISCV_C_CODE_O1.png)


3. As the whole version of above code looks lengthier we have used below code to make it shorter
	
 	```
	riscv64 -unknown-elf-objdump -d sum1ton.o | less
	```
 
& we have obtained the required main part to compare the execution in assembly language as shown below :

	
 
![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/Objdump%20using%20-O1%20format.png)

4. Open the same terminal and run the given command:
 
 	```
	riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum_1ton.o sum_1ton.c
	 ```


![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/RISCV_CODE_Ofast.png)

5. As the whole version of above code looks lengthier as earlier we have used below code to make it shorter
	
 	```
	riscv64 -unknown-elf-objdump -d sum1ton.o | less
	```
 
& we have obtained the required main part to compare the execution in assembly language as shown below :



![image](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%201/Objdump%20using%20-Ofast%20format.png)

### End of 1st task
</details>

------------------------------------------------------------------------------------------------------------------
<details>
<summary><b>Task 2:</b> Performing SPIKE Simulation and Debugging the C code with Interactive Debugging Mode using Spike.
	
I understood the principle and working of the whole program and how various registers like stack pointer and r5 are increasing.
</summary> 


### Testing the SPIKE Simulator for sum1ton.c
**spike_O1_objdump**

* Here we are compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-O1_format** using SPIKE simulator

![spike_O1_objdump_for_sum1ton](https://github.com/user-attachments/assets/7dd97a0f-66ea-4d65-9358-1d86ed5d97d6)


* In the above picture registor a0 earlier has value 21000 in hex decimal.
* After running the registor a0 became 21180 in hexa decimal.
* * Because there has +384 in decimal,so after calculation it gives the above value 

**Spike_Ofast_objdump**

* Here also goes the same we compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-Ofast_format** using SPIKE simulator



![spike_Ofast_objdump_for_sum1ton](https://github.com/user-attachments/assets/9dd161a1-87c4-4966-b8ba-a1156ccd0468)


* In the above picture registor sp earlier has value 3ffffffb50 in hex decimal.
* After running the registor a0 became 3ffffffb40 in hexa decimal.
* Because there has -16 in decimal,so after calculation it gives the above value.

### Area of a Circle (C program):

**Here i have used radius as 5**

![C_code_for_area_of_circle](https://github.com/user-attachments/assets/44008e2b-8b68-4e3d-80ea-c9dcbfda2e75)


**riscv_objdump_O1_format**

* we have obtained the required main part to compare the execution in assembly language as shown below :

![Objdump_using -O1_format_for_area_of_circle](https://github.com/user-attachments/assets/867d7380-a905-45b1-9ec8-8719711d92e6)


**riscv_objdump_Ofast_format**

* we have obtained the required main part to compare the execution in assembly language as shown below :

![Objdump_using -Ofast_format_for_area_of_circle](https://github.com/user-attachments/assets/02104142-0d36-4568-ab24-b0db32ecdda6)



### Testing the SPIKE Simulator for new c program i.e mult1ton.c
**spike_O1_objdump**

* Here we are compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-O1_format** using SPIKE simulator

![spike_O1_objdump_for_area_of_circle](https://github.com/user-attachments/assets/fa2ac77f-b38a-42b8-989c-7d770e92fd8f)




**Spike_Ofast_objdump**

* Here also goes the same we compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-Ofast_format** using SPIKE simulator



![spike_Ofast_objdump_for_area_of_circle](https://github.com/user-attachments/assets/3873cf6d-9bd1-4a00-9d82-e1b28154adc9)





### End of 2nd task
</details>

------------------------------------------------------------------------------------------------------------------

<details>
<summary><b>Task 3:</b> Task is to identify various instruction type of all the given instructions with its exact 32 bits instruction code. </summary>

### INSTRUCTIONS FORMAT IN RISC-V  
 
There are 6 instruction formats in RISC-V:  
1. R-format  
2. I-format  
3. S-format  
4. B-format  
5. U-format  
6. J-format

### 1. R-type Instruction  
* In RV32, each instruction is of size 32 bits.
* In R-type instruction, R stands for register
* This instruction type is used to execute various arithmetic and logical operations.
* The entire 32 bits instruction is divided into 6 fields as shown below.
  
![R_type_instruction](https://github.com/user-attachments/assets/40019a97-4382-4a4d-bac6-5741cbec3a4d)


### 2. I-type Instruction  
* In RV32, each instruction is of size 32 bits.
* In I-type instruction, I stand for immediate which means that operations use Registers and Immediate value
* This instruction type is used in immediate and load operations.
*  The entire 32 bits instruction is divided into 5 fields as shown below.

![I_type_instruction](https://github.com/user-attachments/assets/9f047b6c-85dd-4b55-bb54-b0281ec88d99)


**Example: ADDI rd, rs1, imm**


### 3. S-type Instruction  

* In RV32, each instruction is of size 32 bits.
*  In S-type instruction, S stand for store which means it is store type instruction that helps to store the value of register into the memory.
*  Mainly, this instruction type is used for store operations.
*  The entire 32 bits instruction is divided into 6 fields as shown below.  
  
![S_type_instruction](https://github.com/user-attachments/assets/cfa71fc0-57c0-470a-8ceb-8b85c0dbe278)

**Example: SW rs2, imm(rs1)**


### 4. B-type Instruction  
* In RV32, each instruction is of size 32 bits.
* In B-type instruction, B stand for branching which means it is mainly used for branching based on certain conditions.
*  The entire 32 bits instruction is divided into 8 fields as shown below.  
  
![B_type_instruction](https://github.com/user-attachments/assets/6f63892d-3b45-4f6f-a685-3c3e8e6715fa)


**Example: BEQ rs1, rs2, imm**   
 
  
### 5. U-type Instruction  
* In RV32, each instruction is of size 32 bits.
*  In U-type instruction, U stand for Upper Immediate instructions which means it is simply used to transfer the immediate data into the destination register.
*  The entire 32 bits instruction is divided into 3 fields as shown below.  
  
![U_type_instruction](https://github.com/user-attachments/assets/716b8c11-8251-4519-a881-54840e626616)



**Example: LUI rd, imm**   

  
### 6. J-type Instruction  
* In RV32, each instruction is of size 32 bits.
* In J-type instruction, J stand for jump, which means that this instruction format is used to implement jump type instruction.
*  The entire 32 bits instruction is divided into 6 fields as shown below.  
  
![J_type_instruction](https://github.com/user-attachments/assets/7f1bdd8f-06d0-48ed-a3c7-528b2cda17cd)


**Example: JAL rd, imm**

1. SLLI t0, t0,0x1f

![image](https://github.com/user-attachments/assets/caf27b0e-ce37-48a5-b43f-d278bd3c3c11)

> * In this instruction, SLLI means Shift Left Logical Immediate,
> *hence this instruction belongs to the I-type instruction set.

- **Immediate :** `000000011111` (12-bit immediate value for 0x1f)
- **rs1 = t0 :** `00101`
- **rd = to :** `00110`
- **funct3:** `001`
- **Opcode for SLLI :** `0010011`

**32-bit instruction:** `000000011111|00101|001|00110|0010011`

2. AUIPC a5 0xffff0

![image](https://github.com/user-attachments/assets/dc1b9458-2bce-4ea9-89c1-610b5170cd78)

> * In this instruction AUIPC means Add Upper Immediate to PC Immediate,
> *  hence this instruction belongs to U-type instruction set.

- **Immediate :** 11111111111100000000 (split into imm[31:12] = 111111111111 and imm[11:0] = 000000000000)
- **rd = a5 :** `01111`
- **Opcode for AUIPC :** `0010111`

**32-bit instruction:** `111111111111|01111|0010111`


3. LI a0 0

![image](https://github.com/user-attachments/assets/732699d9-8bdf-48e5-bbce-ff775e79ea57)

**The LI pseudo-instruction means "Load Immediate" and is equivalent to an ADDI (Add Immediate) instruction** 

> * In this instruction LI means Load Immediate,
> * hence this instruction belongs to I-type instruction set

- **Immediate :** `000000000000` (12 bits)
- **rs1 = x0 :** 00000`
- **rd = a0 :** 01010`
- **funct3:** 000`
- **Opcode for ADDI:** `0010011`

**32-bit instruction:** `000000000000|00000|000|01010|0010011`

4. MV a1 a0 


![image](https://github.com/user-attachments/assets/0b0164b6-a416-48d5-8602-74cea98d939f)

**The MV (Move) instruction is a pseudo-instruction in RISC-V, which is equivalent to:
ADD a1, a0, x0**

> * In this instruction MV means  pseudo-instruction,
> *  hence this instruction belongs to S-type instruction set.

- **funct7:** `0000000`
- **rs2 = x0 :** `00000`
- **rs1 = a0 :** `01010`
- **funct3:** `000`
- **rd = a1 :** `01011`
- **Opcode for ADD :** `0110011`

**32-bit instruction:** `0000000|00000|01010|000|01011|0110011`

5. BEQZ a5 101f0 <exit+0x2c>

![image](https://github.com/user-attachments/assets/8e3d4a6a-59fa-4afd-be84-5b38e3c0185b)

**The BEQZ pseudo-instruction means "branch if equal to zero" and is equivalent to:
BEQ a5, x0, offset**



> * In this instruction BWQZ means  pseudo-instruction,short for "branch if equal to zero."
> *  hence this instruction belongs to B-type instruction set.

- **Immediate :** `1000000011100` (split into imm[12] = `1`, imm[10:5] = `000000`, imm[4:1] = `01110`, imm[11] = `0`)
- **rs1 = a5 :** `01111`
- **rs2 = x0 :** `00000`
- **funct3:** `000`
- **Opcode for BEQ:** `1100011`

**32-bit instruction:** `1000000|00000|01111|000|01110|1100011`

6. LW a0 0(sp)

![image](https://github.com/user-attachments/assets/8aa35f2b-bcd2-4619-a3dd-d22d0f706dff)

> * In this instruction, LW means Load Word,
> * hence this instruction belongs to I-type instruction set.

- **Immediate :** `000000000000`
- **rs1 = sp :** `00010`
- **rd = a0 :** `01010`
- **funct3:** `010`
- **Opcode for LW :** `0000011`

**32-bit instruction:** `000000000000|00010|010|01010|0000011`

7. LUI a0 0x21 



![U_type](https://github.com/user-attachments/assets/c27d0aee-79b4-4550-97c4-fb407e604869)


> * In this instruction LUI means Load Upper Immediate,
> *  hence this instruction belongs to U-type instruction set.

- **Immediate = 0x21 :** `0000000000000_00100001`
- **rd = a5:** `01010`
- **Opcode:** `0110111`

**32 bits instruction :** ```0000000000000|00100001|01010|0110111``` 

8. JAL ra 10408 <printf>

![J_type](https://github.com/user-attachments/assets/ed8c976f-f2a3-43cb-8bd0-32c46f7db684)

> * In this instruction JAL means Jump and Link,
> *  hence this instruction belongs to J-type instruction set.

- **Immediate (20 bits)**: `0 1001100000 1 00001010` (split into imm[20] = `0` and imm[10:1] = `1001100000 `imm[11] = `1` and imm[19:12] = `00001010`)
- **rd (ra = x1)**: `00001`
- **Opcode**: `1101111`
		         
**32 bits instruction :** ```0 1001100000 1 00001010|00001|1101111```

9. SD ra 8(sp) 

![S_type](https://github.com/user-attachments/assets/6603a9a5-4804-4ff8-9099-cad8a7440174)


> * In this instruction SD means store doubleword instruction,
> *  hence this instruction belongs to S-type instruction set.  
 
- **Immediate :** `000000010000` (split into imm[11:5] = `0000000` and imm[4:0] = `10000`)
- **rs2 = ra :** `00010`
- **rs1 = sp :** `00100`
- **funct3:** `110`
- **Opcode for SD :** `0100011` 

**32 bits instruction :** ``` 00010|00100|110|10000|100011 ```

10. J 101b0 <atexit> 

![image](https://github.com/user-attachments/assets/d837a001-3588-4ea7-9627-851fb5ff4cc3)

> * In this instruction J means Jump and Link,
> *  hence this instruction belongs to J-type instruction set.

- **Immediate :** `0000010000001101010` (split into imm[20] = `0`, imm[10:1] = `0000000000`, imm[11] = `0`, imm[19:12] = `00000100`)
- **rd = x0 :** `00000`
- **Opcode for J-type (JAL):** `1101111`

**32-bit instruction:** `0000000|0000000000|0|00000100|00000|1101111`



11. SRAI s1 a5 0x3

![image](https://github.com/user-attachments/assets/e1236784-f266-45a2-a05e-67706beeb944)

> * In this instruction SRAI means  Shift Right Arithmetic Immediate.
> *  hence this instruction belongs to I-type instruction set.

- **Immediate :** `000000000011` (split into imm[11:0] = `000000000011`)
- **rs1 = a5 :** `01111`
- **rd = s1 :** `01001`
- **funct3:** `101`
- **Opcode for SRAI :** `0010011`

**32-bit instruction:** `000000000011|01111|101|01001|0010011`

12. BENZ a5,10188 <do global dtors aux+0x4c>
    
![image](https://github.com/user-attachments/assets/31d8c899-4b38-4779-95d8-ed01a5ca0023)

**Assume that BENZ behaves similarly to a branch instruction, but with a custom format. We can treat BENZ like a branch if not zero instruction**

> * In this instruction BENZ means a specific operation (hypothetical or custom instruction), 
> * hence this instruction belongs to a custom instruction type.

- **Immediate :** `0000011010010` (split into imm[12] = `0`, imm[10:5] = `000001`, imm[4:1] = `1010`, imm[11] = `0`)
- **rs1 = a5 :** `01111`
- **rs2 = x0 :** `00000`
- **funct3:** `001`
- **Opcode for custom BENZ:** `1100011`

**32-bit instruction:** `0000001|00000|01111|001|1010|1100011`

13. LBU a5, 1944(gp) # 231a0 <completed.5468>

![image](https://github.com/user-attachments/assets/8f009b1b-1992-45c9-a6ee-aab390d88532)

> * In this instruction LBU means Load Byte Unsigned,
> * hence this instruction belongs to I-type instruction set

- **Immediate :** `11110001000`
- **rs1 = gp :** `00011`
- **rd = a5 :** `01111`
- **funct3:** `100`
- **Opcode for LBU:** `0000011`

**32-bit instruction:** `11110001000|00011|100|01111|0000011`


14 . LD ra 8(sp)

![image](https://github.com/user-attachments/assets/1c0d8506-db98-45da-b412-5e2f1180b59e)
> * In this instruction LD means  load doubleword instruction,
> *  hence this instruction belongs to S-type instruction set.

- **Immediate :** `000000001000` (split into imm[11:5] = `0000000` and imm[4:0] = `01000`)
- **rs1 = sp :** `00010`
- **rd = ra :** `00001`
- **funct3:** `011`
- **Opcode for LD :** `0000011`

**32 bits instruction :** ```0000000|01000|00010|011|00001|0000011```

15. ADDI sp, sp, -16  

![I_type](https://github.com/user-attachments/assets/8ebbb5e4-a5df-4fde-915a-ce4957241968)


> * In this instruction ADDI means Addition, I means Immediate,
> * hence this instruction belongs to I-type instruction set.

- **Opcode for ADDI :** `0010011`  
- **rd = sp :** `00010`  
- **rs1 = sp :** `00010`  
- **imm[11:0] = -16 :** `111111110000`  
- **func3 :** `000`
  
**32 bits instruction :** ```111111110000|00010|000|00010|0010011``` 


### End of 3rd task
</details>

------------------------------------------------------------------------------------------------------------------


<details>
<summary><b>Task 4:</b> Use this RISC-V Core Verilog netlist and testbench for functional simulation experiment. Upload waveform snapshots for the commands on your GitHub. </summary>

Reference GitHub repo is [![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/vinayrayapati/rv32i/blob/main/iiitb_rv32i.v)

## Starting with Functional Simulation
* First I installed the iverilog and gtkwave using following commands:
  ```
  sudo apt-get update
  ```
  ```
  sudo apt-get install iverilog gtkwave
  ```
* Cloning the github repository:
  - make a github repository
  - upload the two filies
  - 1. https://github.com/vaibhavibirajdar07/vaibhavi/blob/main/iiitb_rv32i.v
    2. https://github.com/vaibhavibirajdar07/vaibhavi/blob/main/iiitb_rv32i_tb.v
  -  run the below code in cmd 

  ```
   git clone https://github.com/vaibhavibirajdar07/vaibhavi
   ```

* Chanding the working directory to `vaibhavi` using the following comand:
  ```
   cd vaibhavi
  ```

* To simulate and run the verilog code , entered the following commands in the terminal:
  ```
  iverilog -o vaibhavi iiitb_rv32i.v iiitb_rv32i_tb.v
  ```
  ```
  ./vaibhavi
  ```
* For seeing the output waveform I used the following command:
  ```
  gtkwave iiitb_rv32i.vcd
  ```

* The GTKWave will be opened and following window will be appeared  
  
![image](https://github.com/user-attachments/assets/8ebb8c40-d549-4bd2-9521-92a4200b617c)

### As shown in the figure below, all the instructions in the given verilog file is hard-coded, the designer has hard-coded each instructions based on their own pattern. Hence the 32-bits instruction that we generated in above task will not match with the given instruction.

![image](https://github.com/user-attachments/assets/512edc06-4524-43f7-833f-e3d087869a38)

#### Following are the differences between standard RISCV ISA and the Instruction Set given in the reference repository:  
  
|  **Operation**  |  **Standard RISCV ISA**  |  **Hardcoded ISA**  |  
|  :----:  |  :----:  |  :----:  |  
|  ADD R6, R2, R1  |  32'h00110333  |  32'h02208300  |  
|  SUB R7, R1, R2  |  32'h402083b3  |  32'h02209380  |  
|  AND R8, R1, R3  |  32'h0030f433  |  32'h0230a400  |  
|  OR R9, R2, R5  |  32'h005164b3  |  32'h02513480  |  
|  XOR R10, R1, R4  |  32'h0040c533  |  32'h0240c500  |  
|  SLT R1, R2, R4  |  32'h0045a0b3  |  32'h02415580  |  
|  ADDI R12, R4, 5  |  32'h004120b3  |  32'h00520600  |  
|  BEQ R0, R0, 15  |  32'h00000f63  |  32'h00f00002  |  
|  SW R3, R1, 2  |  32'h0030a123  |  32'h00209181  |  
|  LW R13, R1, 2  |  32'h0020a683  |  32'h00208681  |  
|  SRL R16, R14, R2  |  32'h0030a123  |  32'h00271803  |
|  SLL R15, R1, R2  |  32'h002097b3  |  32'h00208783  |  

### Instruction 1. ADD 

![image](https://github.com/user-attachments/assets/f1b4a40d-b584-4fde-bb48-2132a76a858d)

### Detailed Explanation:
- **Values Stored in Two Different Registers**:
  - The waveform indicates that the values `1` and `2` are stored in registers `r1` and `r2` respectively (`ID_EX_A` and `ID_EX_B`).

- **32-bit Instruction for ADD `R6, R2, R1`**:
  - The instruction `0x02208300` represents the operation `add r6, r1, r2`. This instruction tells the processor to add the values in registers `r1` and `r2` and store the result in register `r6`.

- **Output of ADD Operation**:
  - The ALU performs the addition `1 + 2`, resulting in `3`, which is shown in the `EX_MEM_ALUOUT` signal.

### Instruction 2. SUB

![image](https://github.com/user-attachments/assets/8ae77a86-82ae-4b89-93cc-0e5e060876b7)


### Detailed Explanation:
- **Values Stored in Two Different Registers**:
  - The waveform indicates that the values `1` and `2` are stored in registers `r1` and `r2` respectively (`ID_EX_A` and `ID_EX_B`).

- **32-bit Instruction for SUB `R7, R2, R1`**:
  - The instruction `0x02208380` represents the operation `sub r7, r1, r2`. This instruction tells the processor to add the values in registers `r1` and `r2` and store the result in register `r7`.

- **Output of ADD Operation**:
  - The ALU performs the addition `1 - 2`, resulting in `-1(FFFFFFFF)`, which is shown in the `EX_MEM_ALUOUT` signal.

### Instruction 3. AND

![image](https://github.com/user-attachments/assets/d8438554-d42e-4585-96de-55d731174ad8)


#### Key Points:
1. **Values Stored in Registers**:
   - `ID_EX_A` holds `3`, corresponding to the value in register `R1`.
   - `ID_EX_B` holds `1`, corresponding to the value in register `R3`.

2. **Instruction Fetching**:
   - `EX_MEM_IR` signal shows the value `0x0230A400`, which is the 32-bit instruction for `AND R8, R1, R3`.

3. **ALU Operation**:
   - The output of the ALU operation `EX_MEM_ALUOUT` shows `1`. This is the result of the bitwise AND operation `3 & 1`:
     - `3` in binary is `0011`
     - `1` in binary is `0001`
     - Bitwise AND of `0011 & 0001` results in `0001`, which is `1` in decimal.

4. **Steps in the Processor Pipeline**:
   - **Fetch Stage**: Instruction `AND R8, R1, R3` is fetched.
   - **Decode Stage**: The values of `R1` and `R3` are read into `ID_EX_A` and `ID_EX_B`.
   - **Execute Stage**: The ALU performs the bitwise AND operation, resulting in `1`.
   - **Memory and Write Back Stages**: (Not shown explicitly but understood to follow.)

### Instruction 4. OR 

![image](https://github.com/user-attachments/assets/5282ec13-2fd0-4a2a-9bd0-fa6dd565709a)


**Description:**
- This instruction performs a bitwise OR operation between the values in registers R2 and R5 and stores the result in register R9.

**Details:**
- The values in R2 and R5 are `2` (binary: `0010`) and `5` (binary: `0101`), respectively.
- The bitwise OR operation (`0010 | 0101`) results in `7` (binary: `0111`).


### Instruction 5. XOR

![image](https://github.com/user-attachments/assets/c385fa51-f561-4293-b971-838145925155)


**Description:**
- This instruction performs a bitwise XOR operation between the values in registers R1 and R4 and stores the result in register R10.

**Details:**
- The values in R1 and R4 are `1` (binary: `0001`) and `4` (binary: `0100`), respectively.
- The bitwise XOR operation (`0001 ^ 0100`) results in `5` (binary: `0101`).


### Instruction 6. SLT 

![Screenshot 2025-01-22 224702](https://github.com/user-attachments/assets/683dafb3-af55-409b-949e-89f8655a6296)

1. **Instruction**: `SLT R1, R2, R4`
   - This instruction performs a "Set Less Than" (SLT) operation. It compares the values in registers `R2` and `R4` and sets the destination register `R1` to 1 if the value in `R2` is less than the value in `R4`; otherwise, it sets `R1` to 0.

2. **Waveform Signals**:
   - **EX_MEM_IR[31:0]**: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction `0x202415580`.
   - **ID_EX_A[31:0]**: The value of register `R2`.
   - **ID_EX_B[31:0]**: The value of register `R4`.
   - **EX_MEM_ALUOUT[31:0]**: The output of the Arithmetic Logic Unit (ALU) after performing the SLT operation.

3. **Waveform Details**:
   - **Values in Registers**: The values stored in `R2` and `R4` are 2 and 4, respectively.
   - **SLT Operation**: The SLT operation compares these values. Since 2 < 4, the output is 1, indicating `R2` is less than `R4`.

4. **Annotations**:
   - **Values stored in two different registers**: Highlighting the values of `R2` and `R4`.
   - **Output of SLT will be 1**: Explains that if the value in `R2` is less than `R4`, the result will be 1; otherwise, it will be 0.
   - **32 bits instruction for SLT R1, R2, R4**: Shows the binary representation of the SLT instruction.

### Instruction 7. ADDI 

![image](https://github.com/user-attachments/assets/4317b78c-4289-42af-9d2a-e867f904b3f2)

1. **Instruction**: `ADDI R12, R4, 5`
   - This instruction performs an "Add Immediate" (ADDI) operation. It adds the immediate value 5 to the value in register `R4` and stores the result in register `R12`.

2. **Waveform Signals**:
   - **EX_MEM_IR[31:0]**: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction `0x00520600`.
   - **ID_EX_A[31:0]**: The value of register `R4`.
   - **ID_EX_IMMEDIATE[31:0]**: The immediate value 5.
   - **EX_MEM_ALUOUT[31:0]**: The output of the ALU after performing the ADDI operation.

3. **Waveform Details**:
   - **Values in Registers and Immediate**: The value stored in `R4` is 4, and the immediate value is 5.
   - **ADDI Operation**: The ADDI operation adds these values. The result is 9, which is stored in `R12`.

4. **Annotations**:
   - **Stored value in Register and an Immediate value**: Highlights the values involved in the ADDI operation.
   - **Output of ADDI will be 9**: Explains that the value in `R4` (4) added to the immediate value (5) results in 9.
   - **32 bits instruction for ADDI R12, R4, 5**: Shows the binary representation of the ADDI instruction.

### Instruction 8. BEQ 

![image](https://github.com/user-attachments/assets/fae591e8-7c12-4cd5-8069-feab798b8710)

**Description:**
- The `BEQ` (Branch if Equal) instruction compares the values in registers `R0` and `R0`.
- If the values are equal, it adds the immediate value `15` to the program counter (PC).

**Waveform Analysis:**
- **Initial State:** The program counter (PC) is initially at `10`.
- **Registers:** Both `R0` registers contain the value `0`.
- **Condition:** Since `R0` is equal to `R0`, the condition is true.
- **PC Update:** The instruction adds `15` to the PC.
  - PC = 10(0A in hexa) + 15 = 25(19 in hexa) .
- **Result:** The updated PC value is `25(19 in hexa)`.


### Instruction 9. BNE 

![image](https://github.com/user-attachments/assets/6aa52a22-cf8b-4d19-9433-6bbc8038afd6)

**Description:**
- The `BEQ` (Branch if not Equal) instruction compares the values in registers `R0` and `R0`.
- If the values are not equal, it adds the immediate value `20` to the program counter (PC).

**Waveform Analysis:**
- **Initial State:** The program counter (PC) is initially at `10`.
- **Registers:** Both `R0` registers contain the value `0`.
- **Condition:** Since `R0` is equal to `R0`, the condition is true.
- **PC Update:** The instruction adds `20` to the PC.
  - PC = 26(1A in hexa) + 20 = 46(2E in hexa) .
- **Result:** The updated PC value is `46(2E in hexa)`.

### Instruction 10. SLL

![image](https://github.com/user-attachments/assets/94fd2459-651d-456e-890d-6103cb0b658b)

### End of 4th task
</details>

------------------------------------------------------------------------------------------------------------------
<details>
   <summary><b>Task 5:Overview, Components Required, Operational Workflow, Applications, Circuit Connection, Pinout Diagram and Table for Pin connection required to build the display driver.</summary>

# Digital Object Counter using VSDSquadron Mini

## Overview
This project implements a microcontroller-based system to convert Gray code to binary and display the result on an I2C LCD. The system reads 3-bit binary inputs from GPIO pins, converts them from Gray code to binary using a custom algorithm, and outputs the results on the LCD. The system also supports optional reset functionality through push buttons. The code utilizes direct I2C communication to control the LCD and uses GPIO for input reading. This application is useful in scenarios such as position sensing, encoders, and digital counters where Gray code is commonly used to minimize errors during transitions.

## Components Required
Here is the components list :

Here is the updated table:  

| **S.No** | **Component**              | **Function**                          |  
|---------|--------------------------|--------------------------------------|  
| 1       | VSD Squadron Mini Board  | Microcontroller for processing data  |   
| 2       | I2C LCD Display          | Displays the object count            |  
| 3       | Push Buttons             | Resets the count when pressed        |  
| 4       | Power Supply (5V or Battery) | Provides power to the system         |   

## Operational Workflow:
* The microcontroller reads binary inputs representing Gray code from sensors. It then converts the Gray code to binary using the gray_to_binary function. Finally, the binary values are displayed on the LCD for monitoring or further processing.

## Applications:
* ✔ Gray code to binary conversion is useful in applications like rotary encoders for position sensing, where minimizing errors during bit transitions is critical. It helps decode Gray code outputs into binary for easier interpretation and processing. This is essential in systems like motion control, digital counters, and communication protocols.

## Circuit Connection
## 🔗 Connection Table: Digital Object Counter using VSD Squadron Mini Board  


| **Component**               | **Pin on Component** | **Connected to (VSD Squadron Mini Board)** |
|-----------------------------|---------------------|---------------------------------------------|
| 🟢 **IR Sensor**            | **VCC**             | **5V**                                     |
|                             | **GND**             | **GND**                                    |
|                             | **OUT**             | **PD6 (GPIO_Pin_6)**                       |
| 🟡 **I2C LCD Display (PCF8574)** | **SDA**             | **PC1 (GPIO_Pin_1)**                       |
|                             | **SCL**             | **PC2 (GPIO_Pin_2)**                       |
|                             | **VCC**             | **5V**                                     |
|                             | **GND**             | **GND**                                    |
| 🔴 **Buzzer**               | **Positive (+)**    | **PD5 (GPIO_Pin_5)**                       |
|                             | **Negative (-)**    | **GND**                                    |
| 🔵 **Push Button (Reset)**  | **One Terminal**    | **GND**                                    |
|                             | **Other Terminal**  | **PD1 (GPIO_Pin_1)**                       |



## Pinout Diagram for the project
The following diagram represents the pin configuration for the Digital Object Counter using the VSD Squadron Mini

![block diagram object counter](https://github.com/vaibhavibirajdar07/samsung-riscv/blob/main/task%205/Screenshot%202025-02-17%20223432.png)


### End of 5th task
</details>

------------------------------------------------------------------------------------------------------------------

<details>
   <summary><b>Task 6: Working Code & short video demonstration .</summary>


## Code uploaded on the board
```
#include <ch32v00x.h>
#include <debug.h>
#include <ch32v00x_gpio.h>
#include <stdio.h> // Include for snprintf

// I2C LCD Configuration
#define SDA_PIN GPIO_Pin_1
#define SCL_PIN GPIO_Pin_2
#define LCD_Address 0x27
//#define RESET_BUTTON_PIN GPIO_Pin_1 // Pin for the reset button
//#define COUNT_RESET_BUTTON_PIN GPIO_Pin_0 // Pin for the count reset button

void lcd_send_cmd(unsigned char cmd);
void lcd_send_data(unsigned char data);
void lcd_send_str(unsigned char *str); // Change to char*
void lcd_init(void);
void delay_ms(unsigned int ms);
void GPIO_INIT(void);
void check_reset_button(void);
void check_count_reset_button(uint8_t *g0, uint8_t *g1, uint8_t *g2);

// Function to produce a delay
void delay_ms(unsigned int ms) {
    for (unsigned int i = 0; i < ms; i++) {
        for (unsigned int j = 0; j < 8000; j++) {
            __NOP();
        }
    }
}

// Function to initialize GPIO pins
void GPIO_INIT(void) {
    GPIO_InitTypeDef GPIO_InitStructure;
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD | RCC_APB2Periph_GPIOC, ENABLE);

    // Reset button
    //GPIO_InitStructure.GPIO_Pin = RESET_BUTTON_PIN;
    //GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU; // Input Pull-Up
    //GPIO_Init(GPIOD, &GPIO_InitStructure);

    // Count reset button
    //GPIO_InitStructure.GPIO_Pin = COUNT_RESET_BUTTON_PIN;
    //GPIO_Init(GPIOD, &GPIO_InitStructure);

    // I2C Pins
    GPIO_InitStructure.GPIO_Pin = SDA_PIN | SCL_PIN;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_OD;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOC, &GPIO_InitStructure);

    // Input Pins (b0, b1, b2)
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_4 | GPIO_Pin_5 | GPIO_Pin_6;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU;
    GPIO_Init(GPIOD, &GPIO_InitStructure);
}

// I2C Functions
void i2c_write(unsigned char dat) {
    for (unsigned char i = 0; i < 8; i++) {
        GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
        GPIO_WriteBit(GPIOC, SDA_PIN, (dat & (0x80 >> i)) ? Bit_SET : Bit_RESET);
        GPIO_WriteBit(GPIOC, SCL_PIN, Bit_SET);
    }
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
}

void i2c_start(void) {
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_SET);
    GPIO_WriteBit(GPIOC, SDA_PIN, Bit_SET);
    delay_ms(1);
    GPIO_WriteBit(GPIOC, SDA_PIN, Bit_RESET);
    delay_ms(1);
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
}

void i2c_stop(void) {
    GPIO_WriteBit(GPIOC, SDA_PIN, Bit_RESET);
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
    delay_ms(1);
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_SET);
    delay_ms(1);
    GPIO_WriteBit(GPIOC, SDA_PIN, Bit_SET);
}

int i2c_ACK(void) {
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
    GPIO_WriteBit(GPIOC, SDA_PIN, Bit_SET);
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_SET);
    int ack = GPIO_ReadInputDataBit(GPIOC, SDA_PIN);
    GPIO_WriteBit(GPIOC, SCL_PIN, Bit_RESET);
    return ack; // Return 0 if ACK received, 1 if not
}

// LCD Functions
void lcd_send_cmd(unsigned char cmd) {
    unsigned char cmd_l = (cmd << 4) & 0xf0;
    unsigned char cmd_u = cmd & 0xf0;

    i2c_start();
    i2c_write(LCD_Address << 1);
    if (i2c_ACK()) return; // Check for ACK
    i2c_write(cmd_u | 0x0C);
    i2c_ACK();
    i2c_write(cmd_u | 0x08);
    i2c_ACK();
    delay_ms(1);
    i2c_write(cmd_l | 0x0C);
    i2c_ACK();
    i2c_write(cmd_l | 0x08);
    i2c_ACK();
    delay_ms(1);
    i2c_stop();
}

void lcd_send_data(unsigned char data) {
    unsigned char data_l = (data << 4) & 0xf0;
    unsigned char data_u = data & 0xf0;

    i2c_start();
    i2c_write(LCD_Address << 1);
    if (i2c_ACK()) return; // Check for ACK
    i2c_write(data_u | 0x0D);
    i2c_ACK();
    i2c_write(data_u | 0x09);
    i2c_ACK();
    delay_ms(1);
    i2c_write(data_l | 0x0D);
    i2c_ACK();
    i2c_write(data_l | 0x09);
    i2c_ACK();
    delay_ms(1);
    i2c_stop();
}

void lcd_send_str(unsigned char *str) { // Change to char*
    while (*str) {
        lcd_send_data(*str++);
    }
}

void lcd_init(void) {
    lcd_send_cmd(0x02); // Initialize LCD in 4-bit mode
    lcd_send_cmd(0x28); // 2 lines, 5x7 matrix
    lcd_send_cmd(0x0C); // Display ON, Cursor OFF
    lcd_send_cmd(0x06); // Entry mode set
    lcd_send_cmd(0x01); // Clear display
    delay_ms(20);
}

// Gray to Binary Conversion Function
void gray_to_binary(uint8_t g0, uint8_t g1, uint8_t g2, uint8_t *b0, uint8_t *b1, uint8_t *b2) {
    *b0 = g0^g1 ^ g2;  // Binary[0] = Gray[0] XOR Gray[1] XOR Gray[2]
    *b1 = g1 ^ g2;  // Binary[1] = Gray[1] XOR Gray[2]
    *b2 = g2;  // Binary[2] =  Gray[2]
}

// Function to display Gray to Binary results on LCD
void Display_Gray_to_Binary(uint8_t g0, uint8_t g1, uint8_t g2, uint8_t b0, uint8_t b1, uint8_t b2) {
    lcd_send_cmd(0x80);  // First row, first column
    unsigned char output[16] = "G0 G1 G2B0 B1 B2";
    lcd_send_str(output);

    lcd_send_cmd(0xC0);  // Move to second row
    unsigned char output_str[16]; // Declare the output string
    sprintf((char*)output_str, "%d  %d  %d  %d  %d  %d", g2, g1, g0, b2, b1, b0); // Format the string
    lcd_send_str(output_str);
}

// Function to check the reset button
/*void check_reset_button(void) {
    if (GPIO_ReadInputDataBit(GPIOD, RESET_BUTTON_PIN) == Bit_RESET) { // Reset button pressed
        delay_ms(50); // Simple debounce
        lcd_init(); // Reset the LCD
        lcd_send_cmd(0x80);  // First row, first column
        unsigned char input[16] = "b0 b1 b2 ";
        lcd_send_str(input);
    }
}

// Function to check the count reset button
void check_count_reset_button(uint8_t *g0, uint8_t *g1, uint8_t *g2) {
    if (GPIO_ReadInputDataBit(GPIOD, COUNT_RESET_BUTTON_PIN) == Bit_RESET) { // Count reset button pressed
        delay_ms(50); // Simple debounce
        if (GPIO_ReadInputDataBit(GPIOD, COUNT_RESET_BUTTON_PIN) == Bit_RESET) { // Confirm button press
            *g0 = 0; // Reset g0
            *g1 = 0; // Reset g1
            *g2 = 0; // Reset g2
            Display_Gray_to_Binary(*g0, *g1, *g2, *g0, *g1, *g2); // Update display
            while (GPIO_ReadInputDataBit(GPIOD, COUNT_RESET_BUTTON_PIN) == Bit_RESET); // Wait for button release
        }
    }
}
*/

int main(void) {
    uint8_t b0 = 0, b1 = 0, b2 = 0, g0 = 0, g1 = 0, g2 = 0;

    NVIC_PriorityGroupConfig(NVIC_PriorityGroup_1);
    SystemCoreClockUpdate();
    Delay_Init(); // Assuming this function is defined elsewhere
    GPIO_INIT();
    lcd_init();
    //lcd_send_cmd(0x80);  // First row, first column
    //unsigned char input[16] = "b0 b1 b2";
    //lcd_send_str(input);
    //delay_ms(1000);

    while (1) {
        // Read inputs one by one with delay
        b0 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_4);
        b1 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_5);
        b2 = GPIO_ReadInputDataBit(GPIOD, GPIO_Pin_6);

        // Compute Gray code outputs (gray_to_binary)
        g0 = b0; // Example Gray code input
        g1 = b1;
        g2 = b2;

        // Convert Gray code to Binary
        gray_to_binary(g0, g1, g2, &b0, &b1, &b2);

        // Display Gray code and Binary results
        Display_Gray_to_Binary(g0, g1, g2, b0, b1, b2);

        // Check for reset button press
        //check_reset_button();
        // Check for count reset button press
        //check_count_reset_button(&g0, &g1, &g2);
    }
}

```
# short video demonstration 
Project Simulation Video: https://drive.google.com/file/d/1-8O0cnozs7bqEK5wsWmAnn29WQpkW66o/view?usp=drive_link

### End of 6th task
</details>

------------------------------------------------------------------------------------------------------------------
