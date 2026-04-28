# **x86-64 Register Compendium**

This is a conceptual reference for the general-purpose and special-purpose registers in x86-64 assembly, including what they are typically used for.

---

## **🧠 General-Purpose Registers (64-bit)**

### **%rax — Accumulator**

* Used for: return values from functions  
* Used in: arithmetic operations (implicit in some instructions like mul/div)

### **%rbx — Base Register**

* Used for: general storage  
* Callee-saved (must be preserved across function calls)

### **%rcx — Counter Register**

* Used for: loop counters  
* Used in: shift/rotate instructions

### **%rdx — Data Register**

* Used with %rax in multiplication/division  
* Holds remainder in division

---

### **%rsi — Source Index**

* Used for: source operand in memory operations  
* Argument passing (2nd argument)

### **%rdi — Destination Index**

* Used for: destination operand in memory operations  
* Argument passing (1st argument)

---

### **%rbp — Base Pointer (Frame Pointer)**

* Used for: referencing local variables and function parameters  
* Points to base of current stack frame

### **%rsp — Stack Pointer**

* Points to top of stack  
* Changes with push/pop/call/ret

---

### **%r8 – %r15 — Extended Registers**

* Additional general-purpose registers  
* Used for: extra arguments and temporary storage

Argument passing order (System V ABI):

1. %rdi  
2. %rsi  
3. %rdx  
4. %rcx  
5. %r8  
6. %r9

---

## **🔄 Caller-Saved vs Callee-Saved**

### **Caller-Saved (volatile)**

* %rax, %rcx, %rdx, %rsi, %rdi, %r8–%r11  
* Caller must save if needed

### **Callee-Saved (non-volatile)**

* %rbx, %rbp, %r12–%r15  
* Callee must restore before returning

---

## **🧮 Subregisters (Smaller Views)**

Each 64-bit register can be accessed in smaller sizes:

Example: %rax

* %rax (64-bit)  
* %eax (32-bit)  
* %ax (16-bit)  
* %al (low 8-bit)  
* %ah (high 8-bit)

Same pattern applies to others (%rbx → %ebx → %bx → %bl, etc.)

---

## **📍 Instruction Pointer**

### **%rip — Instruction Pointer**

* Holds address of next instruction  
* Automatically updated by CPU  
* Modified by jumps, calls, and returns

---

## **🚩 Flags Register**

### **%rflags (or %eflags)**

* Stores condition flags used for branching

Common flags:

* ZF (Zero Flag) → result \== 0  
* SF (Sign Flag) → result negative  
* OF (Overflow Flag) → signed overflow  
* CF (Carry Flag) → unsigned overflow

Used by:

* cmp, test  
* conditional jumps (je, jne, jl, etc.)

---

## **🧠 Mental Model Summary**

* %rsp → "where the stack is"  
* %rbp → "start of this function"  
* %rax → "return value"  
* %rdi/%rsi/... → "function arguments"  
* %rip → "what runs next"

---

## **⚡ Quick Reference Table**

| Register | Purpose |
| ----- | ----- |
| %rax | Return value / accumulator |
| %rbx | Callee-saved general |
| %rcx | Loop counter |
| %rdx | Arithmetic helper |
| %rsi | 2nd argument |
| %rdi | 1st argument |
| %rbp | Frame pointer |
| %rsp | Stack pointer |
| %r8–%r9 | Extra arguments |
| %r10–%r11 | Temporaries |
| %r12–%r15 | Callee-saved |
| %rip | Instruction pointer |
| %rflags | Condition flags |

