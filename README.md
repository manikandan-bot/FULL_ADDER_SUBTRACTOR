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
![Screenshot 2024-11-16 103056](https://github.com/user-attachments/assets/044b18ff-43cf-42d9-994d-8b81d302acf4)



**Program:**
```
 Developed by:T.Manikandan/* RegisterNumber:24901040
*/ */ module unit22(sum,cout,a,b,cin); output sum; output cout;
 input a; input b; input cin;
 wire s1,c1,c2;
 xor (s1,a,b); and(c1,a,b); xor(sum,s1,cin); and(c2,s1,cin); or(cout,c2,c1);
 endmodule
 module unit23 (df,bo,a,b,bin); output df; output bo; input a; input b; input bin; wire
 w1,w2,w3; assign w1=a^b; assign w2=(~a&b); assign w3=(~w1&bin); assign
 df=w1^bin; assign bo=w2|w3; endmodule
```
**RTL Schematic**
![Screenshot 2024-11-16 102152](https://github.com/user-attachments/assets/c9dcf97b-2a61-4ae1-8340-85ba6078746e)
![Screenshot 2024-11-16 102239](https://github.com/user-attachments/assets/e8924fed-fee8-4292-b2ff-8127ebd23001)


**Output Timing Waveform**
![Screenshot 2024-11-16 102832](https://github.com/user-attachments/assets/0e08aaeb-2f20-4285-92b5-1ac0161e57ee)
![Screenshot 2024-11-16 103356](https://github.com/user-attachments/assets/2a45dc66-f311-4a48-9d34-ce6394a8344f)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



