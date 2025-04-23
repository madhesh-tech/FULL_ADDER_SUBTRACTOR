# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

```
Developed by: MADHESH I
Reg No: 212224220055
```

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
FULL ADDER
![WhatsApp Image 2024-12-03 at 14 31 47_75d1a1f4](https://github.com/user-attachments/assets/cd3e119d-ef60-4256-9be6-cbe3e8dbe405)
FULL SUBTRACTOR
![WhatsApp Image 2024-12-03 at 14 31 47_ee59b8d3](https://github.com/user-attachments/assets/b16acf62-0499-488c-a6d4-d9114691693c)
**Procedure**

Write the detailed procedure here

**Program:**
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( cin &(a ^ b ));
endmodule


ii)FULL SUBTRACTOR

module fs(a,b,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))); 
endmodule 
```


**RTL Schematic**
FULL ADDER
![Screenshot 2024-12-03 141239](https://github.com/user-attachments/assets/cb64087e-181c-49a1-8fb7-704c56f012ea)
FULL SUBTRACTOR
![Screenshot 2024-12-03 141952](https://github.com/user-attachments/assets/437637d8-d9b7-466c-b4a0-748993d07b38)

**Output Timing Waveform**
FULL ADDER
![Screenshot 2024-12-03 141434](https://github.com/user-attachments/assets/0c15d9e8-751b-4135-ba75-334f93c86aad)
FULL SUBTRACTOR
![Screenshot 2024-12-03 142211](https://github.com/user-attachments/assets/6c9de3f1-af35-4586-9f7d-dd96d7be59e5)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



