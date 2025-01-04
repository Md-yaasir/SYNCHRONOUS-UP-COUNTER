Skip to content
Navigation Menu
Md-yaasir
SYNCHRONOUS-UP-COUNTER

Type / to search
Code
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
Editing README.md in SYNCHRONOUS-UP-COUNTER
BreadcrumbsSYNCHRONOUS-UP-COUNTER
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

2
Line wrap mode

Soft wrap
Editing README.md file contents
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
60
61
62
63
64
65
66
67
68
69
70
71
72
73
74
75
76
77
78
79
80
81
82
83
84
85
86
87
88
89
90
91
92
93
94
95
96
### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**


**4 bit synchronous UP Counter**


If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.



**Procedure**

1.Initialize the shift register to a known state (e.g., all zeros).

2.Input a bit serially into the shift register.

3.Shift the contents of the register one position to the right (or left).

4.Output the shifted bit from the last stage of the register.

5.Repeat steps 2-4 for each bit you want to input and shift.




**PROGRAM**


Developed by:PARANTHAMAN S

RegisterNumber:24900681


```
module ex11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(!rstn)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```


**RTL LOGIC UP COUNTER**


![de10](https://github.com/23002776/SYNCHRONOUS-UP-COUNTER/assets/145742657/66fc43d1-92e2-44d8-aa13-34c31b4f100a)


**TIMING DIAGRAM FOR IP COUNTER**


![de11](https://github.com/23002776/SYNCHRONOUS-UP-COUNTER/assets/145742657/4e8c3b6a-4598-4ed3-b666-6ded1c19437a)



**TRUTH TABLE**


![de12](https://github.com/23002776/SYNCHRONOUS-UP-COUNTER/assets/145742657/865fb0d4-c01e-48fa-9753-c277cc1e6f6a)



**RESULTS**



Hence a 4 bit synchronous up counter is implemented correctly

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
Editing SYNCHRONOUS-UP-COUNTER/README.md at main · Md-yaasir/SYNCHRONOUS-UP-COUNTER
