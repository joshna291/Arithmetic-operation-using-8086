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
|       1200: 12          |        1204: 24          |
|       1201: 34	        |        1205: 68          |
|       1202: 12	        |        1206: 00          |
|       1203: 34	        |        1207: C4          |

#### Manual Calculations


---![WhatsApp Image 2025-09-05 at 21 05 52_e5d56092](https://github.com/user-attachments/assets/e43f64b5-4491-4c54-aa69-426baebff900)



## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="644" height="361" alt="Screenshot 2025-08-25 213055" src="https://github.com/user-attachments/assets/d9e951e0-327a-4e64-9e7c-f4af3e769884" />


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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200: 12         |	   1204: 00            |  
|        1201: 34	        |      1205: 00            |
|        1202: 12         |   	1206: 00            |
|        1203: 34         |   	1207: C4            |

#### Manual Calculations



---![WhatsApp Image 2025-09-05 at 21 05 53_782a76ef](https://github.com/user-attachments/assets/55805570-8eaf-4338-8b6d-bea20b0542d5)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="644" height="430" alt="Screenshot 2025-08-25 214018" src="https://github.com/user-attachments/assets/413cd6fb-2d10-4d06-921c-090b7c946c23" />


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
|        1200: 12	        |        1204: 44          |
|        1201: 34	        |        1205: 51          |
|        1202: 12         |        1206: 97          |
|        1203: 34         |        1207: 0A          |

#### Manual Calculations



---![WhatsApp Image 2025-09-05 at 21 05 55_9222d959](https://github.com/user-attachments/assets/e1384a0e-c428-4499-bc6b-a9dadd8a75b3)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="430" alt="Screenshot 2025-08-25 214338" src="https://github.com/user-attachments/assets/afa7cc40-0d97-4278-96f5-4436b9df5f0a" />


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
|         1200: 12	     |       1204: 01           |
|         1201: 34	     |       1205: 00           |
|         1202: 12	     |       1206: 00           |
|         1203: 34	     |       1207: 00           |

#### Manual Calculations



---![WhatsApp Image 2025-09-05 at 21 05 57_6031b918](https://github.com/user-attachments/assets/d4c4a74c-96a3-4b53-8feb-d6cc2d40ea97)

## OUTPUT FROM MASM SOFTWARE

<img width="646" height="435" alt="Screenshot 2025-08-25 214758" src="https://github.com/user-attachments/assets/f82fed8d-5d22-4dc2-a035-47d15800dbca" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
