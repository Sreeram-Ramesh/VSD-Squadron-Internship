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

<details>
<summary>Task 2</summary>
  
  <br>
    1. Run SPIKE simulation and observation with -O1 and -Ofast.<br>
    2. Write a simple C application and compile it with RISC-V gcc / SPIKE.<br>
    
  <br>

  ### Commands to compile using RISCV:

  <br>
    1. To run the SPIKE simulation.

  <br>

      spike pk sum1ton.o

  <br>

  <img src="./Media/RiscBasedSPIKE.jpg" width="800" alt="Description of image">

  <br>

  <br>
    2. To debug sections of object code.

  <br>

    spike -d pk sum1ton.o

  <br>
    3. To run the Program Counter until we want to run the programs manually.

  <br>
  
    : until pc 0 100b0

  <br>

  <br>

  <img src="./Media/SpikeDebug1.jpg" width="800" alt="Description of image">

  <br>

  <br>

  <img src="./Media/SpikeDebug2.jpg" width="800" alt="Description of image">

  <br>

  <br>
    4. To find the contents of a register.

  <br>

    : reg 0 a0

  <br>

  <br>

  <img src="./Media/SpikeA2Contents.jpg" width="800" alt="Description of image">

  <br>

  <br>
    Press 'Enter' to run the next instructions.

  <br>

  <br>

  <img src="./Media/SpikeA2Ins.jpg" width="800" alt="Description of image">

  <br>

  <br>
    lui - Load Upper Immediate [31:12]

  <br>

  <br>
  
  <img src="./Media/SpikeSPContents.jpg" width="800" alt="Description of image">

  <br>

  <br>
    addi - Add Immediate, -16 in dec which is 10 in hexa, basically 10 sub from the stack pointer.
    
  <br>

  <br>

  ### Binary to Decimal Conversion C Application

  <br>
    Source Code:
    
  <br>

  <br>

  <img src="./Media/MyApp1.jpg" width="800" alt="Description of image">

  <br>

  <br>

  ### Compiling using GCC and Executing.

  <br>

  <br>

  <img src="./Media/MyApp2.jpg" width="800" alt="Description of image">

  <br>

  <br>

  ### Compiling and executing using RISC V.

  <br>
  
  #### SPIKE Simulation:

  <br>
    Using -O1 Execution.

  <br>

    riscv64-unknown-elf-gcc -O1 -mabi=lp64 -march=rv64i -o bintodec.o bintodec.c

  <br>

  <br>

  <img src="./Media/MyAppSpikeO.jpg" width="800" alt="Description of image">

  <br>

  <br>

  <br>
    Using -Ofast Execution.

  <br>
    
    riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o bintodec.o bintodec.c

  <br>

  <br>

  <img src="./Media/MyAppSpikeOfast.jpg" width="800" alt="Description of image">

  <br>

  <br>
  
</details>
