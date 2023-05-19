# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit...

# Implementation-of-Half-Adder-and-Full-Adder-circuit:

### AIM:

To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:

Hardware – PCs, Cyclone II ,

USB flasher,

Software – Quartus prime.

### Theory:

Adders are digital circuits that carry out addition of numbers.

### Half Adder:

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder:

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER :


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER :

### Procedure:

1)Connect the supply (+5V) to the circuit.

2)Switch ON the main switch.

3)If the output is 1, then the led glows.

### Program:

```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Silambarasan K
RegisterNumber:  212221230101
```
HALF ADDER:
```
module HalfAdder(A,B,C,S);
input A,B;
output S,C;
xor(S,A,B);
and(C,A,B);
endmodule
```
FULL ADDER:
```
module FullAdder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor(d,a,b);
xor(s,d,ci);
and(e,ci,d);
and(f,a,b);
or(co,e,f);
endmodule
```



### Output:

### Half adder:

### Logic symbol:

![out1](https://user-images.githubusercontent.com/93427534/233117477-bf3bf502-1b6a-41d5-905a-e2301f896f2f.png)

### RTL realization:

![out2](https://user-images.githubusercontent.com/93427534/233117497-5259c316-325d-42c1-b0ea-56f4b51d4d12.png)

### Truthtable:

![out3](https://user-images.githubusercontent.com/93427534/233117512-ec94cbf4-555d-4f46-9921-39e4070b38bb.png)

### TIMING DIAGRAM:

![out4](https://user-images.githubusercontent.com/93427534/233117541-619e450b-03dc-482a-8dbc-37233a3c23c7.png)

### Full adder:

### Logic symbol:

![img1](https://user-images.githubusercontent.com/93427534/233117593-2196c2cf-8202-4127-b94f-97c12057f662.png)

### RTL realization:

![img2](https://user-images.githubusercontent.com/93427534/233117610-98689ad5-6026-407c-b0e5-fc3e89db0438.png)

### Truthtable:

![img3](https://user-images.githubusercontent.com/93427534/233117642-a8215791-107f-4a7c-b749-e2d1e7f0334b.png)

### TIMING DIAGRAM:

![img4](https://user-images.githubusercontent.com/93427534/233117672-0c888c03-eaab-4d8c-bd3c-0ddfef7ede2c.png)

### Result:

Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
