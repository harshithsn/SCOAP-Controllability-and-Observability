# SCOAP-Controllability-and-Observability
This project is based on Digital VLSI Testing and Testability. The netlist is given as input, the code performs SCOAP  Controllability and Observability of circuit.

# Prerequisite for this project
1) Create a netlist by naming all wires with numbers (increasing order 1,2,3,.....), starting from input to output. example is shown below
2) Save the netlist in .txt format and edit netlist file name in code. (Don't give extra spacing at end of netlist).

# Example (4:1 MUX netlist is used for simulation)
```
NAND 5 2 3
AND 13 6 7
AND 14 8 9
AND 15 10 11
AND 16 4 12
OR 20 13 14
OR 22 15 16
NAND 23 18 19
AND 24 20 23
AND 25 21 22
OR 26 24 25
INPUT 1 7 9 11 12 17
OUTPUT 26
FANOUT 17 18 19 21
FANOUT 5 6 10
FANOUT 1 2 3 8 4 
```

![mux-01](https://user-images.githubusercontent.com/63975346/140762141-6ed6b118-ce2d-4609-ae6a-2e8b598c3c0f.png)

The code contain many variable and functions which are used in fault collapsing and fault simulation. Each cell in code contain description of variabels and function. 

# SCOAP Controllability
Controllability means difficulty of setting internal circuit lines to 0 or 1 by setting primary circuit inputs.

![CC0](https://user-images.githubusercontent.com/63975346/140855245-7cbadb33-5f61-44d1-86e6-06a4b9ba75d3.PNG)

SCOAP Controllability In above figure CC1_5 means Combinational Controllability of 1 at node 5. And CC0_5 means Combinational Controllability of 0 at node 5.

# SCOAP Observability

Observability means difficulty of observing internal circuit lines by observing primary outputs.

![Observe](https://user-images.githubusercontent.com/63975346/140855778-29d649c2-d3d9-4183-a5c6-4ef327a6cc17.PNG)

SCOAP Observability In above figure CO_5 means Combinational Observability of node 5. And CO_2 means Combinational Observability of node 2.

# Manual Calculation of SCOAP Controllability  and Observability

![SCOAP-01](https://user-images.githubusercontent.com/63975346/140856015-57eaa5c0-ae93-4fed-8df2-4d5b622e47b2.png)

In above figure at node 10 the values are (3,2) 13.  
The values inside brackets represent Combinational Controllability. Here 3 is Combinational Controllability of 0 at node 10, similarly 2 is Combinational Controllability of 1 at node 10. 13 represents Combinational Observability of node 10

# THANK YOU
