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


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200              |          01              |
|       1200              |          13              |

#### Manual Calculations

<img width="1480" height="1022" alt="WhatsApp Image 2026-10-15 at 10 49 26 AM" src="https://github.com/user-attachments/assets/ed04c76e-be09-4d0e-944b-aeecda3c206b" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/22f76efc-bdcf-4c64-8040-3284ad97cce5" />

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
|          1200           |          10              |
|          1200           |          11              |
#### Manual Calculations

<img width="1600" height="1119" alt="WhatsApp Image 2026-10-15 at 10 48 43 AM" src="https://github.com/user-attachments/assets/8607ae8b-a3c6-4056-91fd-2dc80c2da49d" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/7a1b26e5-3e97-4c36-8368-3e40d4c71b57" />

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
|          1200           |          42              |
|          1200           |          81              |
#### Manual Calculations

<img width="1512" height="1502" alt="WhatsApp Image 2026-10-15 at 10 49 43 AM" src="https://github.com/user-attachments/assets/d2265095-85b6-4dd2-98fe-b74c267df5ef" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/afc1109f-13e5-4e55-9a8f-0d694511b049" />

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
|         1200            |         01               |
|         1200            |         00               |
#### Manual Calculations
<img width="1600" height="1474" alt="WhatsApp Image 2026-10-15 at 10 49 09 AM" src="https://github.com/user-attachments/assets/e976d618-35e7-49af-ad89-2a47212a64a9" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="642" height="433" alt="image" src="https://github.com/user-attachments/assets/0104d5ca-160f-4e21-bfd2-496909676477" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

