# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Logic Diagram (using nand gate) and (using nor gate):
![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/2dae18d5-93f4-445c-920b-d1242fa4e707)


![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/8dd47ec5-8d45-43ed-8e40-e3aa52917a58)

## Procedure
*Create a project with required entities.
*Create a module along with respective file name.
*Run the respective programs for the given boolean equations.
*Run the module and get the respective RTL outputs.
*Create university program(VWF) for getting timing diagram.
*Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: SURESH S
RegisterNumber: 23008233
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```
## OUTPUT:
## RTL realization of NAND AND NOR gates:
![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/e0a108dc-f10a-43f0-ae09-bed316ac093d)

## Truthtable of NAND gate:
![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/5aa9115a-a910-4d51-bbc5-4bc8b25530d6)

## Truthtable of NOR gate:
![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/47178b1a-3294-498a-8310-fb21c067403e)

## Timing Diagram:
![image](https://github.com/Suresh-2006/Experiment--02-Implementation-of-combinational-logic-/assets/149347611/4ff715a4-088f-4a7d-afc4-3949791481ca)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
