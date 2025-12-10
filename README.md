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
FOR FULL ADDER
<img width="443" height="391" alt="Screenshot 2025-12-10 140158" src="https://github.com/user-attachments/assets/810efc13-824e-4629-bd0a-b155e11a24b6" />
FOR FULL SUBTRACTROR
<img width="449" height="407" alt="Screenshot 2025-12-10 140246" src="https://github.com/user-attachments/assets/02e9e6e4-30c4-418d-a725-454a888cb580" />

**Procedure**

Write the detailed procedure here

**Program:**
```
module Full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

```
```
module Full_subtract (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:SADHANA R 
RegisterNumber:25017643
*/

**RTL Schematic**
FOR FULLL ADDER
<img width="1920" height="1080" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/6f651423-322c-41c1-b158-ee1946701ac3" />
FOR FULL SUBTRACTOR
<img width="1920" height="1080" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/b816d287-a99e-448a-9627-bab415e50b87" />


**Output Timing Waveform**
FOR FULL ADEER
<img width="1920" height="1080" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/b3490526-7858-4dd1-8d66-bd085db7989a" />
FOR FULL SUBTRACTOR
<img width="1920" height="1080" alt="Screenshot (47)" src="https://github.com/user-attachments/assets/d7fe9523-f310-46e7-a95c-d03e25aa9b78" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



