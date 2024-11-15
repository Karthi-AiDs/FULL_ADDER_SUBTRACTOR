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
Full Adder

![5b721d66-fc8d-48df-badc-226348be44df](https://github.com/user-attachments/assets/ad9cd7de-c9bc-41e4-bbff-5c027cbf08f7)


Full Subtractor

![image](https://github.com/user-attachments/assets/7b992c8e-1a9e-4f4b-bdfd-d3ce96feefeb)




**Procedure**


1).Type the program in Quartus software.

2).Compile and run the program.

3).Generate the RTL schematic and save the logic diagram.

4).Create nodes for inputs and outputs to generate the timing diagram.

5).For different input combinations generate the timing diagram

**Program:**

Full Adder

```

module fulladder(sum, cout, a, b, cin); output sum;
output cout;
input a;
input b;
input cin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
endmodule

```

Full Subtractor

```

module fullsub(df,bo,a,b,bin);
output df;
output bo;
input a;
input b; input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

```
 
Developed by: KARTHIKEYAN D

RegisterNumber: 24000848


**RTL Schematic**

Full Adder

![Screenshot 2024-11-15 132224](https://github.com/user-attachments/assets/f1d9273d-1963-4e1a-bdd0-e0fdfbe60659)

Full Subtractor

![Screenshot 2024-11-15 133419](https://github.com/user-attachments/assets/1ec0cb10-02a6-481c-9149-b5b1a9222f13)


**Output Timing Waveform**

Full Adder

![image](https://github.com/user-attachments/assets/a4afc530-a2c3-44a7-b913-ec806ce84a11)


Full Subtractor

![image](https://github.com/user-attachments/assets/69bb6859-f588-4a98-b96c-ac15193c4cee)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



