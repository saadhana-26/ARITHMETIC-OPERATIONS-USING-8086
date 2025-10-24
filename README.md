# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM
To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.
---
## APPARATUS REQUIRED
* Personal Computer with MASM Softwar
---
## 1. ADDITION
#### Algorithm
1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.
## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />

#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200                     |78
1201                      |88
1202                      |23
1203                      |02
1204                      |9C
1205                      |8A    |
#### Manual Calculations
<img width="544" height="569" alt="image" src="https://github.com/user-attachments/assets/b4436208-0201-4e14-87f1-1ca870ea75e1" />
---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="621" height="425" alt="image" src="https://github.com/user-attachments/assets/1a52e5d2-fa72-465c-b6c2-c903871a38b4" />

## 2. SUBTRACTION
#### Algorithm
1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.
## FLOWCHART
<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />
#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|1200                     |12
1201                      |34
1202                      |12
1203                      |34
1204                      |00
1205                      |00                        |
#### Manual Calculations
(Add your calculation here)
<img width="763" height="498" alt="image" src="https://github.com/user-attachments/assets/6dd726a1-2093-4535-8181-7a35401e7024" />
---
## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="427" alt="image" src="https://github.com/user-attachments/assets/f9963563-b9b8-4439-a54d-9f09ca6a3f55" />

## 3. MULTIPLICATION
#### Algorithm
1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.
##FLOWCHART
<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />
#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|2000                     |04
2001                      |00
2002                      |02
2003                      |00
2004                      |08
2005|                      00  |\
#### Manual Calculations
(Add your calculation here)
<img width="750" height="476" alt="image" src="https://github.com/user-attachments/assets/c8fa9b41-40f0-4e99-8136-93375173bb24" />
---
## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="652" height="442" alt="image" src="https://github.com/user-attachments/assets/66ae064d-a934-4172-87c5-226022fb5b7f" />

## 4. DIVISION
#### Algorithm
1. Load memory location of operands.
2. Perform division.
3. Store result.
   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />
#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|2000                     |69
2001                      |24
2002                      |34
2003                      |12
2004                      |02
2005                      |00  
2006                      |01
|2007                     |00                        |
#### Manual Calculations
(Add your calculation here)
<img width="792" height="584" alt="image" src="https://github.com/user-attachments/assets/4c28efcf-3b4e-4bf7-86f9-04680690ba10" />
---
## OUTPUT FROM MASM SOFTWARE
<img width="639" height="433" alt="image" src="https://github.com/user-attachments/assets/66a90cc8-46a4-466e-9be9-bb398292a619" />
## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

