# VSD-Squadron-Internship
A Github repo to keep the progress of my learnings and to complete various tasks assigned to me in the VSD Squadron internship using the VSDSquadron Mini board under Kunal Ghosh sir.

<details>
  <summary>Task 1</summary>
  <br>
    1. Create a GitHub repo.<br>
    2. Install the RISC-V toolchain using VDI.<br>
    3. Refer to the videos, perform the instructions, and play around. 
  <br>

  <br>

  ### Commands for GCC (O0):

  <br>
      1. To check if home directory:
  <br>
    
    cd

  <br>
    2. To open a new C file in leafpad:

  <br>

    leafpad sum1ton.c &
  
  <br>
    3. To compile the code using GCC.

  <br>

    gcc sum1ton.c
  
  <br>
    4. To run the file.

  <br>

    ./a.out
  
  <br>

  <img src="./Media/Cbased.jpeg" width="800" alt="Description of image">

  <br> 
  
  <br>
  
  ### Commands for RISCV (O1):

  <br>
    1. To create an object file from the C file based on the RISC-V character set (O1).
    
  <br>
    
    riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

  <br>

  <img src="./Media/RiscBasedO1.jpeg" width="800" alt="Description of image">

  <br>

  <br>
    2. To create an object file from the C file based on the RISC-V character set (Ofast).
    
  <br>
    
    riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o sum1ton.o sum1ton.c

  <br>

  <img src="./Media/RiscBasedO2.jpeg" width="800" alt="Description of image">

  <br>

  <br>
    3. To view the object file.
    
  <br>
    
    riscv64-unknown-elf-objdump -d sum1ton.o

  <br>
    4. To view specific lines from the object file.
    
  <br>
    
    riscv64-unknown-elf-objdump -d sum1ton.o | less

  <br>
  
</details>
