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

/*
 1.Type the program in Quartus software.
 2.Compile and run the program.
 3.Generate the RTL schematic and save the logic diagram.
 4.Create nodes for inputs and outputs to generate the timing diagram.
 5.For different input combinations generate the timing diagram.
*/

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
```
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
if(!rstn)
  out<=0;
else
  out <= out+1;
end
endmodule
```
Developed by: Dhanvant Kumar V
RegisterNumber: 24005057
*/

**RTL LOGIC UP COUNTER**
![exp11](https://github.com/user-attachments/assets/484939c5-050f-4d95-be8e-a03ed6f9a26c)

**TIMING DIAGRAM FOR IP COUNTER**
![waveform screenshot](https://github.com/user-attachments/assets/abf4651f-6fbf-4e6f-ac48-d9b34c5c7e4a)

**TRUTH TABLE**
![4 bit synchoronous turth table](https://github.com/user-attachments/assets/604af79b-9475-4bd5-9abd-670fd7d2b340)

**RESULTS**
Thus 4 bit synchronous up counter is implemented and it's functionality is validated in Quartus using Verilog Programming.
