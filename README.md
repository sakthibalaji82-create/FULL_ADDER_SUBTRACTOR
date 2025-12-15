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
<img width="869" height="570" alt="image" src="https://github.com/user-attachments/assets/02bf5959-b03a-445b-92b7-c252486726d1" />

<img width="1001" height="777" alt="image" src="https://github.com/user-attachments/assets/263e176b-255b-4d2a-99ee-8f7e74739e9a" />

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

module full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule

module full_subtractor(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
assign diff=(a^b^c);
assign borrow=(~a&c)|(~a&b)|(b&c);
endmodule

**RTL Schematic**

FULL ADDER
<img width="1036" height="572" alt="image" src="https://github.com/user-attachments/assets/97cd025f-d8d3-4b7e-b630-5c939fdecbf0" />
FULL SUBTRACTOR
<img width="1044" height="530" alt="image" src="https://github.com/user-attachments/assets/0509a2fc-ed5b-41a7-bf85-1998ce71dd78" />

**Output Timing Waveform**
FULL ADDER
<img width="1039" height="325" alt="image" src="https://github.com/user-attachments/assets/18040932-204a-4485-bc44-8fc2ace447cc" />
FULL SUBTRACTOR
<img width="1040" height="296" alt="image" src="https://github.com/user-attachments/assets/3556e780-1989-4ced-aaaf-7081695072da" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



