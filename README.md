# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Rathish kumar C
RegisterNumber: 212222100043
*/
### HALF ADDER
```
module half_adder(a, b, s, c);
input a, b;
output s, c;
xor(s, a, b);
and(c, a, b);
endmodule
```
### FULL ADDER
```
module full_adder(a,b, ci, s, co);
input a,b, ci;
output s, co;
wire x,y,z;
xor (x,a,b);
xor (s,x,ci);
and (y,x,ci);
and (z,a,b);
or (co,y,z);
endmodule
Logic symbol & Truthtable
RTL realization
```

### Output:
### RTL
### HALF ADDER:
![PIC1](https://user-images.githubusercontent.com/120539823/230784091-71ed6877-44da-4162-9870-fb70fc1a8323.png)

### FULL ADDER:
![PIC2](https://user-images.githubusercontent.com/120539823/230784105-fec61967-bb0d-400e-a19d-d45f02566223.png)

### TIMING DIAGRAM

### HALF ADDER:
![TTT](https://user-images.githubusercontent.com/120539823/230783707-e32984e6-292d-4c53-8ec7-3d0afd0bfee1.png)
### FULL ADDER:
![TT2](https://user-images.githubusercontent.com/120539823/230783721-70d67379-20ed-4d6e-9dd8-5d06fb75f93e.png)


### TRUTH TABLE 

### HALF ADDER:
![TR 1](https://user-images.githubusercontent.com/120539823/230783868-099e584f-539e-427e-9cc7-6d6fe8f5a93c.png)

### FULL ADDER:
![TR2](https://user-images.githubusercontent.com/120539823/230783871-dd537e09-c342-4cd6-86f6-79f91cd300db.png)

### Result:

Thus implementation of half adder and full adder circuit are verified

