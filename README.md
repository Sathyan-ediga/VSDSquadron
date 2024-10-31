# VSDSquadron
## Task 1 -
To complete the task, start by creating a GitHub repository to store your work.Create a GitHub repository, download a virtual machine manager, and install the RISC-V toolchain using the provided VDI. Follow the lab videos, write a C program to calculate the sum up to *n*, and compile it with both the `gcc` compiler and the RISC-V simulator.

<h1>To compile the C program:</h1>
Install leafpad GTK and text editor.
<l></l>

```
sudo apt install leafpad
```
Create a new C file using leafpad editor.
```
leafpad sum1ton.c
```
![Image Alt](https://github.com/Sathyan-ediga/VSDSquadron/blob/b21ab2a365d4fd93cbd357a12811d7458fc3f949/1.png)
<h1>Writing C code, its compilation and output</h1>
<h2>1) write a C program  to count the numbers from 1 to n using leafpad editor</h2>

```
 leafpad sum1ton.c
 ```

To get the output.
 ```
 ./a.out
 ```
![Image Alt](https://github.com/Sathyan-ediga/VSDSquadron/blob/main/2.png)

<h2>2) To comppile and dissemble the program using RISCV GCC Compiler</h2>

To see the program.

 ```
cat sum1ton.c
 ```
![Image Alt](https://github.com/Sathyan-ediga/VSDSquadron/blob/main/3.png)

The compiler optimizes code based on the information it has about the program. When multiple files are compiled together into a single output file, the compiler can leverage information from all files to enhance optimization for each one.

Enabling optimization flags prompts the compiler to improve code performance and/or reduce code size, though this may increase compilation time and impact debugging capabilities.

The command used to compile using the RISC-V compiler is it creates the objdump file

 ```
riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.0 sum1ton.c
 ```
![Image Alt](https://github.com/Sathyan-ediga/VSDSquadron/blob/main/4.png)

<h2>3) Running the C code using RISC-V compiler and then generating the assembly code using objdump</h2>
   
Use the command riscv64-unknown-elf-objdump -d sum1ton.o will generate the assembly code

 ```
riscv64-unknown-elf-objdump -d sum1ton.o 
 ```
![Image Alt](https://github.com/Sathyan-ediga/VSDSquadron/blob/main/Screenshot%202024-10-31%20195949.png)
 
