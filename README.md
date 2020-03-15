# macro-with-multiple-parameter
Developed a working of Macro expansion for an IBM 360 / 370 assembler. The main motive is to create macro expansion with multiple arguments and create Macro Name Table and Macro Definition Table.

Aim: Defining a macro with multiple arguments, expansion of macro calls & generating expanded source
code.

Instructions:
1) Write a ALP using few instructions & Macro calls with multiple arguments.
2) Define domain/body of the Macro with arguments
3) Write a program which will replace each Macro call with its domain along with proper
arguments & performs expansion of the Macro.
4) Show the input source code with Macro call & output the expanded source code
5) Also output the following statistics:
- Number of instructions in input source code (excluding Macro calls)
- Number of Macro calls
- Number of instructions defined in the Macro call
- Actual argument during each Macro call
- Total number of instructions in the expanded source code.

Input 1: Input Source code with Macro calls
```
MOV R
ABHISHEK 30, 40, 50
DCR R
AND R
ABHISHEK 33, 44, 55
MUL 88
HALT
```
Input 2: Macro definition
```
MACRO
ABHISHEK &ARG1, &ARG2, &ARG3
ADD & ARG1
SUB &ARG2
OR &ARG3
MEND
```

Output source code after Macro expansion:
```
MOV R
ADD 30
SUB 40
OR 50
DCR R
AND R
ADD 33
SUB 44
OR 55
MUL 88
HALT
```

Statistical output:
```
Number of instructions in input source code (excluding Macro calls) = 5
Number of Macro calls = 2
Number of instructions defined in the Macro call = 3
Actual argument during first Macro call “ABHISHEK” = 30, 40, 50
Actual argument during second Macro call “ABHISHEK” = 33, 44, 55
Total number of instructions in the expanded source code = 11
```
