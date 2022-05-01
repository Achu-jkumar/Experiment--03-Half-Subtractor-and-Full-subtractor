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

Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y
## Procedure
## Step 1: 
With the help of Quartus 2 software.
## Step 2:
After run the code do the the analysis and simulation.
## Step 3:
Then get the timing diagram by using universal method.



## Program:
```
Developed by:J.Archana priya 
RegisterNumber:  212221230007.

Half subtracter:

module Exp03EEE(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule

Full subtracter:

module Exp00302 (a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
wire p;
assign diff = ((a^b)^c);
not(p,a);
assign borrow =((p&b)|(p&c)|(b&c));
endmodule  



```


## Output:

## Truthtable



##  RTL realization 
![rtl01](./rtl01.png)
![time1](./time1.png)



## Timing diagram 
![rtl02](./rtl02.png)
![time2](./time2.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
