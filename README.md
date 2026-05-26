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
<img width="500" height="700" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


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
|      1200 : 12          |        1204 : 24         |
|      1201 : 34          |        1205 : 68         |  
|      1202 : 12          |        1206 : 00         |
|      1203 : 34          |                          |  

#### Manual Calculations

![WhatsApp Image 2026-02-06 at 1 10 31 PM](https://github.com/user-attachments/assets/d29ad7a9-80dd-4f58-8062-47d13d7566fe)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="655" height="447" alt="add" src="https://github.com/user-attachments/assets/6f02951c-9bf9-4c77-9365-f9f0ef77f31b" />

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
mov AX,1234h
mov BX,1234h
sub AX,BX
jnc down
inc CL
down:mov SI,1200h
mov [sI],AX
mov [SI+2],CL
mov ah,4ch
int 21H
code ends
end
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200 : 12          |        1204 : 00         |
|      1201 : 34          |        1205 : 00         |  
|      1202 : 12          |                          |
|      1203 : 34          |                          |  

#### Manual Calculations

![WhatsApp Image 2026-02-06 at 1 10 31 PM (1)](https://github.com/user-attachments/assets/32c20ead-32db-4e05-9870-8d1553363086)

---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="638" height="429" alt="sub" src="https://github.com/user-attachments/assets/e76f46a4-92c5-4f74-a10e-b98fc919f7f0" />

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
code segment
assume cs:code,ds:code
org 1000h
MOV DX,0000H
mov AX,1234h
mov BX,1234h
mul BX
mov si,1200h
mov [si],ax
mov [si+02h],dx
mov ah,4ch
int 21h
code ends
end

```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200 : 12          |        1204 : 90         |
|      1201 : 34          |        1205 : 5A         |  
|      1202 : 12          |        1206 : 4B         |
|      1203 : 34          |        1207 : 01         | 

#### Manual Calculations

![WhatsApp Image 2026-02-06 at 1 10 32 PM](https://github.com/user-attachments/assets/637191e3-4f0c-4584-a880-0a351e22c7ac)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="636" height="431" alt="mul" src="https://github.com/user-attachments/assets/8dd2651e-183f-4b8a-810c-90728a9de976" />

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
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,1234H
DIV BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END

```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200 : 12          |        1204 : 01         |
|      1201 : 34          |        1205 : 00         |  
|      1202 : 12          |        1206 : 00         |
|      1203 : 34          |        1207 : 00         |  

#### Manual Calculations

![WhatsApp Image 2026-02-06 at 1 10 32 PM (1)](https://github.com/user-attachments/assets/7890faf2-47c1-43e8-a720-49af56c2bee4)


---
## OUTPUT FROM MASM SOFTWARE
<img width="636" height="425" alt="div" src="https://github.com/user-attachments/assets/b197ccc6-296d-42b0-872e-b8b19dd5bebc" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

