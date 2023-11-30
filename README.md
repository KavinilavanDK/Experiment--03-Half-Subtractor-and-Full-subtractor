# Name: Kavinilavan DK
# Roll No: 23014025
# Experiment 04: Implementation of half subtractor and full subtractor circuit
# AIM
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.
#  Equipments Required
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor and Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

# Procedure
Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.

# Program:
## Half Subtractor
module halfsubtractor(input x,y,output b,d);

assign d=x^y;

assign b=~x&y;

endmodule
## Full Subtractor
module fullsubtractor(input x,y,z, output d,b);

assign d=x^y^z;

assign b=~x&(y^z)|y&z;

endmodule



#  RTL realization
## Half Subtractor


![full sub rtl](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/6a5b2c88-fcb4-4bd7-9419-f9eea6d5105c)

## Full Subtractor


![image](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/59a0488f-1816-4834-b61a-ba6dc7058c7b)


# Truthtable
## Half Subtractor

![image](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/3f3b169a-cf6d-4084-9125-def7cfcc14cf)
## Full Subtractor
![image](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/cb2fb4a8-f421-4e08-a33e-ac086fc17de9)


# Timing diagram 
## Half Subtractor

![image](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/1426f790-d5fb-4ef5-9c03-b090383bcf41)

## Full Subtractor

![image](https://github.com/KavinilavanDK/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870429/01e4b98d-62c5-4042-b027-38fc0b3864cd)



# Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
