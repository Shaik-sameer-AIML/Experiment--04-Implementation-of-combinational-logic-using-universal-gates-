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


~~~

## Program:
/*
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: Shaik sameer
RegisterNumber: 212221240051 
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

~~~

## Output:

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

## Truthtable
![1 1111](https://user-images.githubusercontent.com/93427186/167447114-3e91f60f-fa00-4485-a72f-dd34b2d26c76.png)



##  RTL realization
![1 22222](https://user-images.githubusercontent.com/93427186/167447149-a3ae17ab-daf6-4a5a-acd1-a5d9dd785e8d.png)


## Timing diagram 
![1 3333333333333](https://user-images.githubusercontent.com/93427186/167447168-de0c1c2a-8429-4e21-8ed1-fc16d553777e.png)


F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

## Truthtable

![1 3333](https://user-images.githubusercontent.com/93427186/167447345-9228abd0-d620-4918-81ef-3bf1bd3baa53.png)


##  RTL realization

![1 444444](https://user-images.githubusercontent.com/93427186/167447356-c6245664-56ad-4bec-b5bc-68ceb49744d4.png)


## Timing diagram 

![1 55555](https://user-images.githubusercontent.com/93427186/167447375-48a00499-d2a0-4da6-9e6e-f5702e3a33f3.png)




## Result:

Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
 
