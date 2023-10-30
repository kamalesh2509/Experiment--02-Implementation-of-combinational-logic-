# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

# Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'
## Logic Diagram
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
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
![230769540-cb5375ff-4941-43f7-be27-9fb60767ce8d](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/6c3e4cbf-caa6-4d6a-acf9-988d31c473f9)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
