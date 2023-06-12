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

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation. Y= A+B
 

## Logic Diagram
## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively. 

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression. 

4.Use each output to represent one for F1 and the other for F2. 5.End the verilog program using keyword endmodule.

## Program:
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: RATHISH KUMAR C
Register No:212222100043

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module imp(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```
## RTL realization
## Output:
## Logical Diagram:
![logic](https://github.com/pradeepsiva20/Experiment--02-Implementation-of-combinational-logic-/assets/120539823/7910c1b5-59f8-475d-8bd9-c6f9b9dc602b)

## RTL
  For F1:
  
![237874285-33bf1982-c9f4-4e82-a293-ac0348beb82a](https://github.com/pradeepsiva20/Experiment--02-Implementation-of-combinational-logic-/assets/120539823/023d8b44-a950-4ad1-9922-67b636c91a47)

  For F2:
  
![for f2](https://github.com/pradeepsiva20/Experiment--02-Implementation-of-combinational-logic-/assets/120539823/a91f10ff-fbc9-4a25-836f-935925f71369)

## Timing Diagram
  For F1:
  
![timing diagram for f1](https://github.com/pradeepsiva20/Experiment--02-Implementation-of-combinational-logic-/assets/120539823/7142e9d1-a309-46c5-95bd-ab9c27a929ad)

  For F2:
  
![timing diagram for f2](https://github.com/pradeepsiva20/Experiment--02-Implementation-of-combinational-logic-/assets/120539823/297ca42b-86fe-4317-9241-2089dc3d25a6)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
