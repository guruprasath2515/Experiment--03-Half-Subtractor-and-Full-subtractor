# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program
HALF SUB
````
module halfsub(a,b,differ,borrow);
input a,b;
output differ,borrow;
xor(differ,a,b);
assign borrow = ~a & b;
endmodule
````
FULL SUB
````
module fullsub(a,b,c,borrow,differ);
input a,b,c;
output borrow,differ;
xor(differ,a,b,c);
assign borrow = (~a)&c | (~a)&b | (b&c);
endmodule
````
HALF SUB TRUTH TABLE

![WhatsApp Image 2024-01-02 at 14 22 36_6698c9d8](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/e93b15fc-586b-484f-b99b-023ef141ae79)

FULL SUB TRUTH TABLE

![WhatsApp Image 2024-01-02 at 14 23 10_3b0ba0a2](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/b14ec254-7b96-4b96-b3f7-712c59021eee)
RTL VIEWER
HALF SUB
![WhatsApp Image 2024-01-02 at 14 24 07_da421f2f](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/c2413e13-9fe3-45e5-a41f-c3d450f887e5)

FULL SUB

![WhatsApp Image 2024-01-02 at 14 25 25_e4ba737b](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/5b2fb17c-43db-4803-a322-8574e2bf2db5)
WAVEFORM
HALF SUB

![WhatsApp Image 2024-01-02 at 14 26 17_34f07714](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/6a378a59-5a3a-4661-acae-99436d358289)
FULL SUB

![WhatsApp Image 2024-01-02 at 14 26 55_48f6b3ae](https://github.com/guruprasath2515/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/155418874/69c39ef5-d776-4217-869b-9abeda917c35)


## Output:

## Truthtable



##  RTL realization


## Timing diagram 

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
