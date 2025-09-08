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
MOV SI,1200H
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
| 1200: 31                | 1204: 62                 |
| 1201: 12                | 1205: 24                 |
| 1202: 31                | 1206: 00                 |
| 1203: 12                | 1207: C4                 |
#### Manual Calculations
![add manual](https://github.com/user-attachments/assets/5293cb12-9fcd-4a1b-98c7-422be8da0bf5)


## OUTPUT IMAGE FROM MASM SOFTWARE
![AYESHA add1 1](https://github.com/user-attachments/assets/8c920187-4435-4822-a311-be36a4bfe03c)
![AYESHA add1](https://github.com/user-attachments/assets/a31f0663-7d45-4d69-ab85-2594555f29e6)


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
MOV SI,1200H
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
|  1200: 31               |  1204:   00              |
|  1201: 12               |  1205:   00              |
|  1202: 31               |  1206:   00              |
|  1203: 12               |  1207:   C4              |
#### Manual Calculations
![sub manual](https://github.com/user-attachments/assets/c7113350-2236-4acf-9dab-0df74b6b0143)

## OUTPUT SCREEN FROM MASM SOFTWARE
![AYESHA sub2 1](https://github.com/user-attachments/assets/3e30b04e-3896-499a-bba2-5c0ecb1d53bf)
![AYESHA sub2](https://github.com/user-attachments/assets/f28cb65d-e3e0-43ac-85d1-daf832bc9e0c)

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
MOV SI,1200H
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
|  1200: 31               | 1204: 61                 |
|  1201: 12               | 1205: ED                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: C4                 |
### Manual Calculations
![mul manual](https://github.com/user-attachments/assets/9ec17078-13f5-4cfb-a2a7-20e1633de80c)



## OUTPUT SCREEN FROM MASM SOFTWARE
![AYESHA mul 3 1](https://github.com/user-attachments/assets/eddf2cd9-7544-4709-baa9-f3a24e9598a6)
![AYESHA mul3](https://github.com/user-attachments/assets/bafa2c8b-d4d6-41ae-93f6-28054459f84d)

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
MOV SI,1200H
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
|  1200: 31               | 1204: 01                 |
|  1201: 12               | 1205: 00                 |
|  1202: 31               | 1206: 00                 |
|  1203: 12               | 1207: 00                 |

#### Manual Calculations
![div manual](https://github.com/user-attachments/assets/c9833800-f54b-4c16-8d02-be4460bc8991)



## OUTPUT FROM MASM SOFTWARE
![AYESHA div4 1](https://github.com/user-attachments/assets/e572d239-3d44-4b12-bb4f-c217ebcfc666)
![AYESHA div4](https://github.com/user-attachments/assets/c7bc9758-f16e-43a3-9b62-4c1d21c44558)






## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
