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
![image](https://github.com/user-attachments/assets/cea8dc7e-e90f-4645-8c5b-6d1bcf77acb7)
![image](https://github.com/user-attachments/assets/c8a1a6fb-d1f6-459c-814c-4ffeafe1308d)
**Procedure**
1.Open the Quartus II
2.create a new project
3.start coding
4.run it then RTL realization will be shown
5.next get the output waveform 
6.get the output and write a result

**Program:**
//full adder
module Exp4_1(sum, cout, a, b, cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets wire sl,cl,c2;
//Instantiate logic gate primitives
xor (sl,a,b);
and(cl,a,b);
xor(sum, sl, cin);
and (c2, sl,cin);
or (cout, c2,cl);
endmodule

module Exp4_2 (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:24900612
J.PAVITRA
*/

**RTL Schematic**
![Exp4_1](https://github.com/user-attachments/assets/36fbd518-151d-47a9-a059-87774e0a9f21)
![Exp4_2](https://github.com/user-attachments/assets/b31caca0-aedd-45e2-aa8e-82ec6242ff0c)

**Output Timing Waveform**
![Exp4_1Waveform](https://github.com/user-attachments/assets/9a794051-dd8b-448a-a2fb-9866bf9730f9)
![Exp4_2Waveform](https://github.com/user-attachments/assets/b891eeba-b9f8-41f7-ba16-67e51f82c54d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



