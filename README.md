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
|                         |                          |

#### Manual Calculations

![addasm](https://github.com/user-attachments/assets/834dd67f-5a03-447d-857f-926499876ee8)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/eb141a95-e574-4f45-aaf7-bd7d5e1f622b" />
<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/9e5413aa-80c4-4303-ac98-c79e0182a676" />


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
|                         |                          |

#### Manual Calculations

![subasm](https://github.com/user-attachments/assets/ecf28e19-9d6b-45c0-8d81-4c276c9d8550)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/dd65e6d4-700a-4083-a5e7-2ef85795da0c" />
<img width="640" height="480" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/4b9ac7aa-f261-4787-b590-c35fd1d5be9b" />


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

![mulasm](https://github.com/user-attachments/assets/445aa40d-2c6b-4fc8-8d47-c92df09b327a)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/aa57f423-11a0-4229-b58f-13951c5d5f3f" />
<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/ee739d1c-66c0-4746-9fa5-8a28502f7ac8" />


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

![divasm](https://github.com/user-attachments/assets/47825915-053d-475d-84f2-848cacd5d155)


---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/4dd9db22-956c-465c-8525-381ee228e113" />

![div masm](https://github.com/user-attachments/assets/94829837-65ee-4281-846a-3895f0f7cedd)

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
