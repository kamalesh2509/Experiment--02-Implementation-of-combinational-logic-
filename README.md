# Experiment--02-Implementation-of-combinational-logic

## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

Using AND gate: An AND gate is a fundamental digital logic gate that performs a logical conjunction on its input signals. It produces an output signal only when all of its input signals are high (logic level 1). If any of the input signals is low (logic level 0), the output of the AND gate remains low.

using NOT gate: A NOT gate, also known as an inverter, is a basic digital logic gate that performs the operation of negation on its input signal. In other words, it produces the opposite (complementary) output to its input. If the input is high (logic level 1), the output will be low (logic level 0), and if the input is low, the output will be high.

using OR gate: An OR gate is a fundamental digital logic gate that performs a logical disjunction on its input signals. It produces an output signal when at least one of its input signals is high (logic level 1). The output remains low only if all input signals are low (logic level 0).

## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Developed by:E.Kamalesh
RegisterNumber:212222100019
module DE2(a,b,c,d,f1);
input a,b,c,d;
output f1;
wire x1,x2,x3,x4,x5;
assign x1=(~a)&(~b)&(~c)&(~d);
assign x2=(a)&(~c)&(~d);
assign x3=(~b)&(c)&(~d);
assign x4=(~a)&(b)&(c)&(d);
assign x5=(b)&(~c)&(d);
assign f1=x1|x2|x3|x4|x5;
endmodule
```
## RTL:

![263434590-5ab2c60f-4580-4390-8c83-3c47e830b49c](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/0cf41176-23e9-4b2c-b947-c27e04f5f4b7)
## Truth table
![263434612-b280551a-f504-449b-8050-3c61de9a5b15](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/89925971-758e-477a-87d8-cdcf8831b5f8)
## Output waveform
![263435625-b4739a63-7d76-4783-9926-cea462a51185](https://github.com/kamalesh2509/Experiment--02-Implementation-of-combinational-logic-/assets/120444689/80822640-8fe5-4a1f-ae88-a73272f13fc1)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
