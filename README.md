# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

 a b cin sum carry 0 0 0 0 0 0 0 1 1 0 0 1 0 1 0 0 1 1 0 1 1 0 0 1 0 1 0 1 0 1 1 1 0 0 1 1 1 1 1 1 

 ![Screenshot 2024-12-03 143410](https://github.com/user-attachments/assets/744537c4-6cdd-44bd-9fcc-d08c80f86fe8)

 a b bin difference borrow 0 0 0 0 0 0 0 1 1 1 0 1 0 1 1 0 1 1 0 1 1 0 0 1 0 1 0 1 0 0 1 10 0 0 1 1 1 1 1

 ![Screenshot 2024-12-03 143516](https://github.com/user-attachments/assets/b0a56d99-3606-4b62-8ad8-b9c70438c298)


**Procedure**

 1. Type the program in Quartus software.

 2. Compile and run the program.
 
 3. Generate the RTL schematic and save the logic diagram.
 
 4. Create nodes for inputs and outputs to generate the timing diagram.
 
 5. For different input combinations generate the timing diagram

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Full adder
```
 module fa(a,b,cin,sum,carry);
 
 input a,b,cin;
 
 output sum,carry;
 
 assign sum=( (a ^ b)^cin);
 
 assign carry= ( (a & b)| ( cin &(a ^ b )));
 
 endmodule
```
 Full subtractor
```
 module fs(a,b,bin,difference,borrow);
 
 input a,b,bin;
 
 output difference,borrow;
 
 assign difference= ( (a ^ b)^bin);
 
 assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
 
 endmodule
```
 
Developed by: R.karthik padmanaban
RegisterNumber:24001743

**RTL Schematic**

![WhatsApp Image 2024-12-03 at 13 27 49_046d7555](https://github.com/user-attachments/assets/29379be5-0bb5-4678-8f43-91649d65fa56)

![WhatsApp Image 2024-12-03 at 13 27 49_70ed80be](https://github.com/user-attachments/assets/c6bd7607-411b-4db9-b9f9-3378dcfb39d9)


**Output Timing Waveform**

![Screenshot 2024-12-09 194106](https://github.com/user-attachments/assets/c97307ae-10c6-4107-937c-3c72bc15aff7)

![Screenshot 2024-12-09 194200](https://github.com/user-attachments/assets/5ddda646-eb3f-4a01-a58b-483d42f5b875)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



