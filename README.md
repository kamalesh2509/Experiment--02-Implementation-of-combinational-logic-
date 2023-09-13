# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 

## Logic Diagram
## Procedure
## Program:
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: kamalesh E 
RegisterNumber: 212222100019 

```
Using NAND Operation:

module combine1(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

Using NOR Operation:

module combine2(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
assign F = ~S;
endmodule
```

## RTL realization
NAND:
![230769436-c66e52b5-0619-419b-88ee-225823a510f9](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/d835c462-9707-4b6d-8960-344b27ce58e6)

NOR:

![230769443-30bfc11d-1dee-424c-b9da-28f8a00c1d03](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/81b5f1ec-c0c5-41b6-bcf4-1f2573096c18)


## Output:
NAND:
![230769461-03c4f869-4c34-46be-9101-aea1df9917dd](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/570d888f-7b1b-49bd-841c-26158d105464)

NOR:
![230769509-f01614dd-0c56-45ed-8a77-32e426f798d7](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/205260d2-20d7-42c9-a831-5389811a75fc)

## Timing Diagram
NAND:
![230769530-0b13b1d2-6b8c-48c1-a0c5-5c4b6d65a795](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/9a0df440-d193-4ca4-ab5f-253cd42c32e1)
NOR:
![Uploading 230769540-cb5375ff-4941-43f7-be27-9fb60767ce8d.png…]()

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
