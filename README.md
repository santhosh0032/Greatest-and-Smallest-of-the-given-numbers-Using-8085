# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H
MOV C,A
LXI H, 4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JNC NEXT
MOV A, M
NEXT: INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```


## Output:
<img width="1905" height="1021" alt="image" src="https://github.com/user-attachments/assets/6c7b1d6c-af91-449a-b9a7-599763ccbbc1" />
<img width="1895" height="995" alt="image" src="https://github.com/user-attachments/assets/7960a195-647c-453b-b0d0-0db076fd3638" />




## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H
MOV C,A
LXI H, 4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JC NEXT
MOV A, M
NEXT: INX H
DCR C
JNZ LOOP
STA 4301H
HLT
```

## Output:

<img width="1897" height="994" alt="image" src="https://github.com/user-attachments/assets/00c16893-4035-41c8-b6c1-0e054241a149" />

<img width="1874" height="1047" alt="Screenshot 2025-09-12 160601" src="https://github.com/user-attachments/assets/5facf9a1-25e6-4bd9-aab9-cdcae26889c0" />








## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
