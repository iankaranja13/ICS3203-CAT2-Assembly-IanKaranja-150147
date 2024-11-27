# ICS3203-CAT2-Assembly-IanKaranja-150147

# Assembly Programming Tasks

This project consists of several assembly programming tasks demonstrating the use of control flow, array manipulation, modular programming, and data monitoring. The tasks were implemented using **NASM** (Netwide Assembler) for x86 architecture and can be compiled and run on both **32-bit** and **64-bit** systems.

## Prerequisites

To run and compile the assembly code, you will need:

- **NASM** (Assembler for x86 architecture).
- **Linux-based environment** for compiling and running the code.
- **LD** (Linker) for linking object files into executables.

### Compile and Run Instructions

For **64-bit** systems:

1. Assemble the code:
    ```bash
    nasm -f elf64 <filename>.asm -o <filename>.o
    ```

2. Link the object file:
    ```bash
    ld <filename>.o -o <filename>
    ```

3. Run the executable:
    ```bash
    ./<filename>
    ```

For **32-bit** systems, use the following commands:

1. Assemble the code:
    ```bash
    nasm -f elf32 <filename>.asm -o <filename>.o
    ```

2. Link the object file:
    ```bash
    ld <filename>.o -o <filename>
    ```

3. Run the executable:
    ```bash
    ./<filename>
    ```

Replace `<filename>` with the specific task file (e.g., `task1`, `task2`, etc.).

---

## Task 1: Control Flow and Conditional Logic

### Overview
This program classifies a number as "POSITIVE," "NEGATIVE," or "ZERO" based on user input. It demonstrates the use of conditional and unconditional jumps to control program flow effectively.

### Challenges
- **Jump Instructions:** Understanding when to use `jmp` (unconditional) versus conditional jumps like `je` or `jl` was critical.
- **Branching Logic:** Handling the three cases (positive, negative, zero) while ensuring program stability required careful flow planning.

### Insights
- **Conditional jumps** simplify complex logic by branching directly based on comparison results.
- **Modularizing logic** into clear blocks improves readability and debugging efficiency.

---

## Task 2: Array Manipulation with Looping and Reversal

### Overview
This program accepts an array of integers as input and reverses the array in place. It outputs the reversed array using a loop to swap elements without using additional memory.

### Challenges
- **Memory Manipulation:** Swapping elements in place required precise memory addressing.
- **Bounds Checking:** Ensuring the loop correctly iterates only half the array length was key to preventing segmentation faults.
- **Indexing Complexity:** Managing pointers for both the start and end of the array required extra attention to avoid overlaps.

### Insights
- Using **registers for pointer arithmetic** minimizes memory operations and improves efficiency.
- **Dividing the array length** by 2 to limit iterations was an efficient approach to prevent redundant swaps.

---

## Task 3: Modular Program with Subroutines for Factorial Calculation

### Overview
This program calculates the factorial of a user-input number using a modular subroutine. The subroutine uses the stack to preserve registers and employs multiplication in a loop to compute the factorial.

### Challenges
- **Register Management:** Preserving and restoring registers using the stack was critical to ensure program stability.
- **Input Conversion:** Handling ASCII input and converting it to an integer required careful validation to avoid invalid computations.
- **Overflow Risks:** Factorial values grow rapidly, requiring careful testing for inputs near the upper bound of integer storage.

### Insights
- **Subroutines** make the code reusable and modular, improving maintainability.
- **Managing the stack effectively** ensures that the program does not disrupt registers used elsewhere.

---

## Task 4: Data Monitoring and Control Using Port-Based Simulation

### Overview
This program simulates a water level sensor monitoring system. Based on the sensor value, it performs the following actions:
- Turns on a "motor" when the water level is low.
- Stops the motor when the water level is moderate.
- Triggers an "alarm" when the water level is too high.

### Challenges
- **Simulating Ports:** Using memory locations to represent input/output ports required creative mapping.
- **Logic:** Implementing efficient branching to handle the three conditions (low, moderate, high) while maintaining clarity.
- **Memory Addressing:** Manipulating specific memory locations to reflect sensor and motor states required careful planning.

### Insights
- **Simulations** provide a clear understanding of real-world port-based systems without requiring physical hardware.
- **Modular design** and clear branching logic simplify debugging and extend functionality.

---

## About

This project demonstrates key concepts in **assembly programming**, such as **control flow**, **data manipulation**, and **modular subroutines**. The tasks showcase how assembly language can be used to efficiently control hardware devices, manage memory, and perform mathematical computations.

---

## License

MIT License

---

## Resources

- **NASM Documentation:** [https://www.nasm.us/doc/](https://www.nasm.us/doc/)
- **Linking in Linux with LD:** [https://www.gnu.org/software/binutils/manual/](https://www.gnu.org/software/binutils/manual/)
- **Assembly Programming Tutorials:** [https://www.tutorialspoint.com/assembly_programming/index.htm](https://www.tutorialspoint.com/assembly_programming/index.htm)

---

Feel free to update this template with your own details and expand on any sections that may need more specific information about your project. Let me know if you need any changes!

