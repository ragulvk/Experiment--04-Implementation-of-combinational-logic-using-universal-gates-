# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:

 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime

## THEORY:

A universal gate is a logic gate which can implement any Boolean function without the need to use any other type of logic gate. The NOR gate and NAND gate are universal gates. This means that you can create any logical Boolean expression using only NOR gates or only NAND gates. In practice, this is advantageous since NOR and NAND gates are economical and easier to fabricate than other logic gates. Similarly, an OR gate is typically realised as a NOR gate followed by an inverter.
 
# Procedure:

## STEP 1:
Create a project with required entities.

## STEP 2:
Create a module along with respective file name.

## STEP 3:

Run the respective programs for the given boolean equations.

## STEP 4:

Run the module and get the respective RTL outputs.

## STEP 5:

Create university program(VWF) for getting timing diagram.

## STEP 6:

Give the respective inputs for timing diagram and obtain the results.

## STEP 7:

Write the detailed procedure here 


# Program:
```
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.

Developed by: Monisha T
RegisterNumber:  212221240029

```

##  F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
```

module Combination(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule
```
##  F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
```
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

```

# Output:

## F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate

### Truthtable:

![output1](https://user-images.githubusercontent.com/93427240/167295830-a3fc6753-a276-4f5f-b88c-5261cc6d54bf.png)


###  RTL realization:

![output2](https://user-images.githubusercontent.com/93427240/167295837-ebf48940-7666-4e8e-a9ed-95cb364635ff.png)

### Timing diagram 

![output3](https://user-images.githubusercontent.com/93427240/167295842-0b08354c-9d15-4fcc-b87d-3c4e9ad200f3.png)


## F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

### Truthtable:

![output4](https://user-images.githubusercontent.com/93427240/167295980-4765834c-7d9a-4757-ac9c-9b9a54c39897.png)


###  RTL realization:

![output5](https://user-images.githubusercontent.com/93427240/167295988-62a2ce85-5c56-479a-8df4-227bdd6ac28b.png)

### Timing diagram 

![output6](https://user-images.githubusercontent.com/93427240/167295991-1f7d7011-4b6b-4458-b45b-e73762259edf.png)


## Result:

Thus implementation of logic functions using NAND and NOR gates is done and its operation is verified in Quartus using Verilog programming.
 
