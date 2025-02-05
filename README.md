# Experiment--04-Half-Subtractor-and-Full-subtractor
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
1.Use module project name(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: JENISHA.J
RegisterNumber:  212222230056

HALF SUBTRACTOR

module HS(a,b,d,bo);
input a,b;
output d,bo;
assign d = (a^b);
assign bo = (~a&b);
endmodule

FULL SUBTRACTOR

module FS(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (A^B^C);
assign Borrow = (~A&(B^C)|(B&C));
endmodule
```

## Output:

## Truthtable
### HALF SUBTRACTOR
![HS truth](https://user-images.githubusercontent.com/119405070/232306868-4d58ce3e-d6b6-4092-b33b-cbcca3b75366.png)


### FULL SUBTRACTOR
![FS truth](https://user-images.githubusercontent.com/119405070/232306887-854d52a6-18f5-4e86-90f0-2bd404b42809.png)


##  RTL realization
### HALF SUBTRACTOR
![HS rtl](https://user-images.githubusercontent.com/119405070/232265081-2bbea4aa-fdb1-49ac-9e31-3e4d4979f3ea.png)
### FULL SUBTRACTOR
![FS rtl](https://user-images.githubusercontent.com/119405070/232265503-c5e3b489-1f0e-40f3-a9a5-3358dcef4b58.png)


## Timing diagram 
### HALF SUBTRACTOR
![HS time](https://user-images.githubusercontent.com/119405070/232265232-86b50a69-1e70-41c6-8438-a96fedc3e71d.png)
### FULL SUBTRACTOR
![FS time](https://github.com/Jenishajustin/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405070/6ab963e7-ac56-44f0-aa94-d2cb678a98ff)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
