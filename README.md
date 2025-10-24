
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

```
**OUTPUT:**
<img width="1918" height="1193" alt="Descending after" src="https://github.com/user-attachments/assets/5efeff4d-142a-49f1-a712-395ed3666d84" />


**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="1919" height="1199" alt="Descending Before" src="https://github.com/user-attachments/assets/3b9f2ce5-4d33-470d-aa5e-0b06e38de71f" />

After execution: D:0x40H:
<img width="1918" height="1193" alt="Descending after" src="https://github.com/user-attachments/assets/7635da45-3496-4a47-99c9-22226c1ef98b" />



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**
<img width="1919" height="1199" alt="Ascending Before" src="https://github.com/user-attachments/assets/da47a999-cd05-46fe-8c34-67031bcfc06c" />

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="1916" height="1191" alt="Ascending After" src="https://github.com/user-attachments/assets/234b9901-59b4-41d5-b1cf-8bfc39a24b82" />


After execution:
D:0x40H:
<img width="1919" height="1199" alt="Ascending Before" src="https://github.com/user-attachments/assets/9bd8d408-2f18-4e51-93b3-fec61a750500" />




**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

