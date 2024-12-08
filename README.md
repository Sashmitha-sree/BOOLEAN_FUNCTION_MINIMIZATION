# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
module de2(a,b,c,d,w,x,y,z,f1,f2);

input a,b,c,d,w,x,y,z;

output f1,f2;

wire m,n,o,p,q,r,s,t,u,k1,k2,k3,k4,k5,k6,k7,k8,k9;

not(m,a);

not(n,b);

not(o,c);

not(p,d);

and(q,m,n,o,p);

and(r,a,o,p);

and(s,n,c,p);

and(t,m,b,c,d);

and(u,b,o,d);

or(f1,q,r,s,t,u);

not(k1,w);

not(k2,x);

not(k3,y);

not(k4,z);

and(k5,x,k3,z);

and(k6,k2,k3,z);

and(k7,k1,x,y);

and(k8,w,k2,y);

and(k9,w,x,y);

or(f2,k5,k6,k7,k8,k9);

endmodule

```


**RTL realization**

![Screenshot 2024-12-08 193358](https://github.com/user-attachments/assets/27783a36-0498-425f-8349-8860a4ca0a74)


**Logic symbol & Truthtable:**

![Screenshot 2024-12-08 201716](https://github.com/user-attachments/assets/e68e9c77-9e4d-4109-bfa7-204f20f624e2)


**Timing Diagram**
![Screenshot 2024-12-08 201634](https://github.com/user-attachments/assets/d6a022bc-3760-4970-b65b-864a83079a59)



**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

