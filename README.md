# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Raja.R
RegisterNumber: 212222100041
# HALF SUBTRACTOR:
module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule


# FULL SUBTRACTOR:
module fullsub(a,b,c,diff,borrow);
input a,b,c;
output borrow,diff;
wire an,q,r,s,t,cn,u;
not(an,a);
not(cn,c);
xor(q,a,b);
xor(diff,q,c);
and(s,a,b);
and(t,q,cn);
or(borrow,s,t);
endmodule


## Output:
##  RTL realization
# Half subtractor
![1](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/23a4a3ec-6e78-40ed-b8cb-ce1cdab19297)
# Full subtractor
![2](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/507c30f1-5338-4ee4-80b0-7209bd8427ea)


## Truthtable
# Half subtractor
![HALF SUB](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/77daec72-d992-4942-b012-f15597481a65)
# Full subractor
![FULL SUB](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/d276aecb-3abb-4a08-958f-7dfbf8658527)







## Timing diagram
# Half subtractor
![3](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/e3ed11d0-93b4-420a-a921-ddf52c2f7842)
# Full subtractor
![4](https://github.com/Raja8334/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/120719634/7f44677e-851a-466a-b92f-8c72583930b4)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
