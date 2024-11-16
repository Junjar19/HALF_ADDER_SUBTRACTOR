# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![Screenshot 2024-11-12 133633](https://github.com/user-attachments/assets/726ee04a-69a9-45d5-af86-2af51f44438c)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B
![Screenshot 2024-11-16 211227](https://github.com/user-attachments/assets/35ed72fb-9dca-41b1-9abf-ad0629fa1315)


Figure -02 HALF Subtractor

**Truthtable**

a	b	sum (a ^ b)	carry (a & b)
0	0	0	0
0	1	1	0
1	0	1	0
1	1	0	1
![image](https://github.com/user-attachments/assets/3fd38d6b-39a9-4ae3-88c3-aa5dff3f63a0)


a	b	difference (a ⊕ b)	borrow (~a & b)
0	0	0	0
0	1	1	1
1	0	1	0
1	1	0	0
![image](https://github.com/user-attachments/assets/6ece45db-babb-4e61-80f7-ba49ba80d539)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

i)HALF ADDER

module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum= (a ^ b);
assign carry= ( a & b);
endmodule


ii)HALF SUBTRACTOR

module hs(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a ^ b);
assign borrow= ( ~a & b);
endmodule



/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:Junjar U
RegisterNumber:24008873

*RTL Schematic**
*![Screenshot 2024-11-12 133910](https://github.com/user-attachments/assets/4eda8653-f2a0-42ba-83a0-7faaad4a74a5)

![Screenshot 2024-11-16 211421](https://github.com/user-attachments/assets/f91ddac9-5d6e-4027-9106-d91dab3784eb)


**Output/TIMING Waveform**

**Result:**
Thus the given half adder and half subtractor functions are implemented and their operators are verified using Verilog programming.
