# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/f3b47187-6f0f-490c-8704-f2973cb2b276" />


---

## PROGRAM
```asm
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

```
PROGRAM:
<img width="1920" height="1080" alt="Screenshot 2025-09-22 211424" src="https://github.com/user-attachments/assets/77798fb9-ecc2-4303-8d68-1d82644b4ce5" />

OUTPUT:
<img width="552" height="473" alt="Screenshot 2025-09-22 211453" src="https://github.com/user-attachments/assets/d6701ec1-a613-4f28-9fd8-eed2b2485457" />

---
MANUAL CALCULATIONS:
![WhatsApp Image 2025-09-22 at 21 19 16_a30e1bce](https://github.com/user-attachments/assets/4a3961b0-f5a3-471c-a941-081db0867dd5)


---

RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---


