# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule

FULL SUBTRACTOR:
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule

**RTL Schematic**
FULL ADDER:
<img width="1535" height="771" alt="Screenshot 2026-03-12 104218" src="https://github.com/user-attachments/assets/026ceefd-db2b-4743-b851-03a367576e56" />
FULL SUBRACTOR:
<img width="1593" height="850" alt="Screenshot 2026-03-12 104311" src="https://github.com/user-attachments/assets/101aaeca-9f99-493d-af06-f2947c6472fa" />

**Output Timing Waveform**
FULL ADDER:
<img width="1399" height="782" alt="Screenshot 2026-03-12 104339" src="https://github.com/user-attachments/assets/0a2d414d-e8a9-457e-a7c5-d47d8f0b93a2" />
FULL SUBRACTOR:
<img width="1395" height="787" alt="Screenshot 2026-03-12 104402" src="https://github.com/user-attachments/assets/87bd2a58-f2dd-40d7-adac-80703a4bc841" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



