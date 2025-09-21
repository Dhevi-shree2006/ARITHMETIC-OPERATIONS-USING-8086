# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

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

## DIRECT ADDITION

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
| 1200                    |    12                    |
| 1201                    |    34                    |
| 1202                    |    12                    |
| 1203                    |    34                    |
| 1204                    |    24                    |
| 1205                    |    68                    |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 02 06_faca4408](https://github.com/user-attachments/assets/5e626d11-1c3f-435b-98b9-702dd727d54c)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="650" height="336" alt="addScreenshot 2025-08-29 085255" src="https://github.com/user-attachments/assets/933db6b5-5f97-4b4e-a3d9-c52889296577" />

##INDIRECT ADDITION

###PROGRAM
```asm
CODE SEGMENT
ASSUME CS: CODE, DS:CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1: MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```
#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |                      
| 1200                    |    78                    |
| 1201                    |    88                    |
| 1202                    |    23                    |
| 1203                    |    02                    |
| 1204                    |    9C                    |
| 1205                    |    8A                    |
#### Manual Calculations

<img width="686" height="525" alt="image" src="https://github.com/user-attachments/assets/a35a2421-4b4b-4505-90b1-8df14bdaa689" />

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="621" height="425" alt="inaddScreenshot 2025-09-17 142922" src="https://github.com/user-attachments/assets/7fb9d97b-4c65-46b2-b4ea-3ea9504a439e" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />

## DIRECT SUBTRACTION

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
| 1200                    |    12                    |
| 1201                    |    34                    |
| 1202                    |    12                    |
| 1203                    |    34                    |
| 1204                    |    00                    |
| 1205                    |    00                    |

#### Manual Calculations

(Add your calculation here)
<img width="930" height="408" alt="image" src="https://github.com/user-attachments/assets/6ca71e79-1e78-4b15-998d-df4de93f6213" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-17 at 14 23 52_6f89e1bc](https://github.com/user-attachments/assets/efe5932a-d876-42cd-a40c-13ce09a0f76d)

## INDIRECT SUBTRACTION

### PROGRAM
```
CODE SEGMENT
ASSUME CS: CODE,DS:CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX, BX
JNC DOWN
INC CL
DOWN: MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200                    |    12                    |
| 1201                    |    34                    |
| 1202                    |    12                    |
| 1203                    |    34                    |
| 1204                    |    00                    |
| 1205                    |    00                    |
#### Manual Calculations

(Add your calculation here)
![WhatsApp Image 2025-09-21 at 23 21 17_1182d2a4](https://github.com/user-attachments/assets/ccc516b8-e936-4c91-b892-fcb95e21cde4)


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="427" alt="insubScreenshot 2025-09-12 084822" src="https://github.com/user-attachments/assets/ed2de494-43c7-4567-8730-2b6d522cdfcf" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)
<img width="1151" height="626" alt="image" src="https://github.com/user-attachments/assets/9e1484b8-f847-4265-a7e8-6172f11671c0" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="637" height="424" alt="mulScreenshot 2025-09-17 142337" src="https://github.com/user-attachments/assets/07386bb7-fd91-4fa1-92a0-c530bdd984ae" />


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
|                         |                          |

#### Manual Calculations

(Add your calculation here)
<img width="1160" height="560" alt="image" src="https://github.com/user-attachments/assets/9897ab9d-b1dd-4890-9998-9c18a7b3d2e1" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="628" height="427" alt="Screenshot 2025-09-21 223000" src="https://github.com/user-attachments/assets/2ec97a09-7f3e-4a27-8d83-4352d78d009b" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

