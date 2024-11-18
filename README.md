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
Truthtable

![Screenshot (12)](https://github.com/user-attachments/assets/157d702b-3733-44ba-959d-75af32920a82)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

![Screenshot (15)](https://github.com/user-attachments/assets/e082094b-9d73-4a13-b311-d7774d68d0c8)



**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/ module unit22(sum,cout,a,b,cin);
output sum;
output cout;
 input a;
 input b;
 input cin;
 wire s1,c1,c2;
 xor (s1,a,b);
 and(c1,a,b);
 xor(sum,s1,cin);
 and(c2,s1,cin);
 or(cout,c2,c1);
endmodule

 module unit23 (df,bo,a,b,bin);
 output df;
 output bo;
 input a;
 input b;
 input bin;
 wire w1,w2,w3; assign w1=a^b;
 assign w2=(~a&b);
 assign w3=(~w1&bin);
 assign df=w1^bin;
 assign bo=w2|w3;
 endmodule  

 
**RTL Schematic**


![Screenshot (13)](https://github.com/user-attachments/assets/64300e27-12ec-4543-b060-c4acbfff55fa)
![Screenshot (14)](https://github.com/user-attachments/assets/8d4bbd11-e859-476e-a0c3-00a09147aa3f)

**Output Timing Waveform**
![Screenshot (4)](https://github.com/user-attachments/assets/b8c8d47a-ed86-4b34-86d6-d867fabd26d2)
![Screenshot (5)](https://github.com/user-attachments/assets/0436a50c-d951-49ce-a5ee-7217cf68f673)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



