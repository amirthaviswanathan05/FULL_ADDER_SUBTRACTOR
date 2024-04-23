# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

# AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# Full Adder and Full Subtractor

## Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

## Figure -1 FULL ADDER

## Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## Truthtable:
### FULL-ADDER :
![319499226-fe8a893e-7da2-49a7-b5f0-1fc2e4a1976f](https://github.com/amirthaviswanathan05/FULL_ADDER_SUBTRACTOR/assets/149035397/b73708d8-ce3f-40da-b040-99d233112615)

### FULL-SUBTRACTOR: 
![319499373-532faf89-78bb-4299-b8ca-9a967622141a](https://github.com/amirthaviswanathan05/FULL_ADDER_SUBTRACTOR/assets/149035397/02ffec74-0350-464a-b40b-cd0a0ed4c714)


## Procedure:

STEP-1 Open Quartus Prime software.

STEP-2 Create a new project and select the target FPGA device.

STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

STEP-4 Add the HDL file to the project and compile the design.

STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.

Write the detailed procedure here

# Program:

```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```

# RTL Schematic:
 ![319499633-776457b8-69fb-4627-87a1-4c58b479b2c9](https://github.com/amirthaviswanathan05/FULL_ADDER_SUBTRACTOR/assets/149035397/b96c91fd-7229-4032-a423-fff3456402c8)



# Output Timing Waveform:
![319499766-db43bff2-a490-4df7-8099-e8dfba237afa](https://github.com/amirthaviswanathan05/FULL_ADDER_SUBTRACTOR/assets/149035397/7a0bd143-b720-44cd-a354-dd3ee537888a)



# Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



