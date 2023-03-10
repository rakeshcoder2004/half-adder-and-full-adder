# half-adder-and-full-adder

Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit
Implementation-of-Half-Adder-and-Full-Adder-circuit
AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime Theory Adders are digital circuits that carry out addition of numbers.

Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

image

Figure -01 HALF ADDER
image

Figure -02 FULL ADDER
Procedure
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows.

Program:

module half_adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
module full_adder(x,y,z,s,c);
input x,y,z;
output s,c;
wire x1,x3,x4;
xor(x1,x,y);
xor(s,x1,z);
and(x3,x,y);
and(x4,x,y);
or(c,x3,x4);
endmodule
Output:
RTL :
half_adder_RTL_diagram Full_adder_RTL_Diagram

TIMING DIAGRAM :
half_adder_timing_diagram Full_adder_timing_diagram

TRUTH TABLE
Result:
Thus the output of half_adder and full_adder experiment successfully achieved.
