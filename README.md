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

![image](https://github.com/anupjanmane18/samsung-riscv/blob/main/task2/spike_O1_objdump_for_sum1ton.png)

* In the above picture registor a0 earlier has value 21000 in hex decimal.
* After running the registor a0 became 21180 in hexa decimal.
* * Because there has +384 in decimal,so after calculation it gives the above value 

**Spike_Ofast_objdump**

* Here also goes the same we compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-Ofast_format** using SPIKE simulator



![image](https://github.com/anupjanmane18/samsung-riscv/blob/main/task2/spike_Ofast_objdump_for_sum1ton.png)

* In the above picture registor sp earlier has value 3ffffffb50 in hex decimal.
* After running the registor a0 became 3ffffffb40 in hexa decimal.
* Because there has -16 in decimal,so after calculation it gives the above value.

### Area of a Circle (C program):

**Here i have used radius as 5**

![image](https://github.com/vaibhavibirajdar07/samsung-risc-v/blob/main/C_code_for_area_of_circle.png)

**riscv_objdump_O1_format**

* we have obtained the required main part to compare the execution in assembly language as shown below :

![image](https://github.com/vaibhavibirajdar07/samsung-risc-v/blob/main/Objdump_using%20-O1_format_for_area_of_circle.png)

**riscv_objdump_Ofast_format**

* we have obtained the required main part to compare the execution in assembly language as shown below :

![image](https://github.com/vaibhavibirajdar07/samsung-risc-v/blob/main/Objdump_using%20-Ofast_format_for_area_of_circle.png)


### Testing the SPIKE Simulator for new c program i.e mult1ton.c
**spike_O1_objdump**

* Here we are compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-O1_format** using SPIKE simulator

![image](https://github.com/vaibhavibirajdar07/samsung-risc-v/blob/main/spike_O1_objdump_for_area_of_circle.png)



**Spike_Ofast_objdump**

* Here also goes the same we compare both of the compiler that must display the same output on the terminal.
* after that we are gona debug the sum1ton.c of **-Ofast_format** using SPIKE simulator



![image](https://github.com/vaibhavibirajdar07/samsung-risc-v/blob/main/spike_Ofast_objdump_for_area_of_circle.png)




### End of 2nd task
</details>

------------------------------------------------------------------------------------------------------------------
