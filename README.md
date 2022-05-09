# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
 
 
 
 


## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.




## Program:
/*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: Aavula Tharun
RegisterNumber: 212221240003 
*/

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

module norcombination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule

## Output:

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

## Truthtable

![1 1111](https://user-images.githubusercontent.com/93427201/167445261-5965508e-9245-418d-a565-857c77c9ba64.png)


##  RTL realization
![1 22222](https://user-images.githubusercontent.com/93427201/167445296-ce8e8d43-b08c-41a0-8848-0ff17ee3fa41.png)


## Timing diagram 
![1 3333333333333](https://user-images.githubusercontent.com/93427201/167445321-eae964d4-c0ed-44a1-9754-c4a3f2ee776c.png)


F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## Truthtable
![1 3333](https://user-images.githubusercontent.com/93427201/167445353-ffab0b3f-0300-46ec-b3b0-a66f09870dd3.png)


##  RTL realization
![1 444444](https://user-images.githubusercontent.com/93427201/167445368-f2cd1b62-a61e-4f82-a90b-e354d978401b.png)


## Timing diagram 

![1 55555](https://user-images.githubusercontent.com/93427201/167445378-ede5dc3c-24bb-4e6b-bd9a-487c14b841ac.png)



## Result:
 Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
