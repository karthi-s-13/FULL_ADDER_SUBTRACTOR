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

```Full Adder```

![2-41](https://github.com/user-attachments/assets/38a4f897-b767-496a-ac23-aa6c8c42fbc8)

```Full subtractor```

![full-subtractor-truth-table](https://github.com/user-attachments/assets/eecf3961-d85d-49c1-932c-3a4744101000)



**Procedure**

Write the detailed procedure here

**Program:**
```FULL ADDER```
```
module exp4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
wire sl,cl,c2;
xor(sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,cl);
endmodule
```

```FULL SUBTRACTOR```
```
module exp4sub(df,bo,a,b,bin);
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
```
/* Program to design a Full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: KARTHIKEYAN S RegisterNumber:24900102
*/

**RTL Schematic**

```FULL ADDER```

![Screenshot 2024-11-12 110458](https://github.com/user-attachments/assets/164a6f44-08ac-4d35-a479-46439dfc0ff4)

```FULL SUBTRACTOR```

![Screenshot 2024-11-12 113852](https://github.com/user-attachments/assets/e2483152-4426-4c62-9511-4e50e246a1c2)



**Output Timing Waveform**

```FULL ADDER```

![Screenshot 2024-11-12 111719](https://github.com/user-attachments/assets/a53c2bc3-5bf6-40f1-9ff8-fbcbad3fb7fd)

```FULL SUBTRACTOR```

![Screenshot 2024-11-12 114441](https://github.com/user-attachments/assets/ae218389-b928-48e3-a1e4-fb7bde718646)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



