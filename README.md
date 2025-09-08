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
| 1200: 12                | 1204: 24                 |
| 1201: 34                | 1205: 68                 |
| 1202: 12                | 1206: 00                 |
| 1203: 34                |                          |
------------------------------------------------------

#### Manual Calculations

![addasm](https://github.com/user-attachments/assets/834dd67f-5a03-447d-857f-926499876ee8)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/22380dbb-b747-4879-a644-409a3febd7aa" />

<img width="640" height="480" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/5a34a80d-d33e-4b20-8b51-e1979ba9a65a" />



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
code segment
assume cs:code,ds:code
org 1000h
mov si,1200h
mov ax,[si]
mov bx,[si+02h]
mov cl,00h
mov ax,bx
jnc l1
inc cl
l1:mov[si+04h],ax
mov [si+06h],cl
mov ah,4ch
int 21h
code ends
end
```
#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200: 12                | 1204: 00                 |
| 1201: 34                | 1205: 00                 |
| 1202: 12                | 1206: 00                 |
| 1203: 34                |                          |
------------------------------------------------------


#### Manual Calculations

![subasm](https://github.com/user-attachments/assets/ecf28e19-9d6b-45c0-8d81-4c276c9d8550)


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/96993129-923b-40fb-b796-c6d8179a6143" />

<img width="640" height="480" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/0bc0e75c-5d11-47b1-8adf-cea5503f9a8f" />



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
| 1200: 12                | 1204: 44                 |
| 1201: 34                | 1205: 51                 |
| 1202: 12                | 1206: 97                 |
| 1203: 34                |                          |
------------------------------------------------------
#### Manual Calculations

(Add your calculation here)

![mulasm](https://github.com/user-attachments/assets/445aa40d-2c6b-4fc8-8d47-c92df09b327a)


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-09-07 at 22 18 40 (1)](https://github.com/user-attachments/assets/49dec03a-dd6f-4ab8-966b-dcd43554acf0)
![WhatsApp Image 2025-09-07 at 22 18 30](https://github.com/user-attachments/assets/ffdef407-d9f8-4d20-9765-109bd6a0ab3f)


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
| 1200: 12                | 1204: 01                 |
| 1201: 34                | 1205: 00                 |
| 1202: 12                | 1206: 00                 |
| 1203: 34                |                          |
------------------------------------------------------
#### Manual Calculations

![divasm](https://github.com/user-attachments/assets/47825915-053d-475d-84f2-848cacd5d155)


---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-09-07 at 22 27 10 (1)](https://github.com/user-attachments/assets/b065c35e-824b-455d-a3a5-0c198a2d4f18)
![WhatsApp Image 2025-09-07 at 22 27 10 (2)](https://github.com/user-attachments/assets/22ecf79d-c53e-4ed7-8a20-e0ec38b24621)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
