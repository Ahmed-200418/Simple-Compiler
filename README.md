# 🛠️ OLL Compiler
A simple compiler for a custom stack-based language with the `.oll` extension.  
This compiler parses `.oll` source code, converts it into x86-64 NASM assembly, assembles it using NASM, links it with GCC, and then runs the resulting executable.

---

## 📄 Language Overview

The `.oll` language supports the following instructions:

| Instruction           | Description                                      |
|-----------------------|--------------------------------------------------|
| `PUSH <num>`          | Push a number onto the stack                     |
| `POP`                 | Pop the top value from the stack                 |
| `ADD`                 | Add the top two values on the stack              |
| `SUB`                 | Subtract the top value from the one below it     |
| `PRINT "<string>"`    | Print a string literal                           |
| `READ`                | Read an integer input from the user              |
| `JUMP.EQ.0 <label>`   | Jump if top of stack is equal to 0               |
| `JUMP.GT.0 <label>`   | Jump if top of stack is greater than 0           |
| `HALT`                | Terminate the program                            |
| `<label>:`            | Define a label (can be used as a jump target)    |

---

## 🚀 Getting Started

### ✅ Requirements

To run this project, make sure you have the following installed:

- **Python 3**
- **NASM** (Netwide Assembler)
- **GCC** (for linking the assembly code)

## ▶️ How to Compile and Run

1. Write your program in a file ending with `.oll` (e.g. `example.oll`) and you can find samples in the project files
2. Run the compiler script using:

```bash
python compiler.py example.oll
