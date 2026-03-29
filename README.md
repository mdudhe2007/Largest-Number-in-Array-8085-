### 📦 Largest Number in Array using 8085 Assembly

### 🧾 Overview

This project implements a simple yet fundamental algorithm in 8085 Assembly Language to find the largest number in an array stored in memory.
It demonstrates:

Looping using registers
Memory traversal using HL pair
Comparison using CMP instruction
Conditional branching
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### ⚙️ Algorithm

Initialize HL with starting address of array
Load first element into accumulator (A)
Compare with next element
If current element is greater → update A
Repeat until all elements are checked
Store result in memory
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 🧠 Assembly Code
LXI H, 1000H     ; HL points to start of array
MVI C, 04H       ; Number of elements

MOV A, M         ; Load first element into A (assume max)

LOOP: INX H      ; Move to next element
CMP M            ; Compare A with current memory

JNC SKIP         ; If A >= M, skip update
MOV A, M         ; Else update max value

SKIP: DCR C      ; Decrement counter
JNZ LOOP         ; Repeat until done

STA 2000H        ; Store largest number at 2000H
HLT
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 📊 Example

Input (Memory):

Address	Value
1000H	25
1001H	40
1002H	10
1003H	60

Output:
Address	Value
2000H	60 ✅
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 🖥️ Simulation

Run the program using:
GNUSim8085
Any compatible 8085 simulator
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 🎥 Demo
<p align="center"> <img src="video.gif" /> </p>
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 📁 Project Structure
Largest-Number-8085/<br>
│<br>
├── code.asm<br>
├── README.md<br>
└── demo.mp4<br>
    <hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">
    
### 🚀 Key Concepts Covered
Register pair (HL) addressing
Loop control using counter register
Conditional jumps (JNC, JNZ)
Memory read/write operations
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### ✨ Future Improvements
Find smallest number
Find both min & max in one pass
Extend to 16-bit numbers
Combine with sorting algorithm
<hr style="border: none; height: 2px; background: linear-gradient(to right, #00c6ff, #0072ff);">

### 📌 Author
DuduBoiii
