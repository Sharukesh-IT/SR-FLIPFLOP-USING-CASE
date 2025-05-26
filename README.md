# SR-FLIPFLOP-USING-CASE

**AIM:**

To implement  SR flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

SR Flip-Flop SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/0f710028-ad52-4d3e-9276-8714cf023a25)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dabfc4f4-87e3-4cbc-9472-f89ee1b5ed30)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/dd90d16c-aec5-4290-a586-e2346b1e9eb5)

 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/naavaneetha/SR-FLIPFLOP-USING-CASE/assets/154305477/473efad6-d70b-4ca7-aeb7-898bbfca319f)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

**Procedure**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
Developed by:MAHASRI D
RegisterNumber:24901210
*/

**PROGRAM**
module SRflipflop(S,R,clk,Q,Qbar);
 input S,R,clk; 
 output reg Q;
 output reg Qbar;
initial Q=0;
 initial Qbar=1;
 always @(posedge clk)
 begin Q=S|((~R)&Q);
 Qbar=R|((~S) &
(Qbar)); end endmodule

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2025-05-26 170716](https://github.com/user-attachments/assets/66295ff9-e68e-4048-bcaf-0bb15a01f3d8)

**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2025-05-26 170729](https://github.com/user-attachments/assets/410ad549-d4a9-4aac-b8be-7b114642251b)

**RESULTS**
SR flipflop using verilog and validating their functionality using their functional tables are verified.
