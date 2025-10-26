### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**

1.Start the ModelSim/Vivado software and Create a new project and add a Verilog file.

2.Write the dataflow code for 8-to-3 encoder using continuous assignment statements (assign).

3.Compile the code and check for errors.

4.Write a testbench to apply all 8 input combinations.

5.Simulate the design and observe output waveform. Verify the truth table and save results.

**PROGRAM**

Program for Encoder 8 To 3 in Dataflow Modelling and verify its truth table in quartus using Verilog programming.

module encoder_8_to_3_dataflow (

    input [7:0] I,
    
    output [2:0] Y
    
    );

    // Continuous assignments for the outputs based on the input logic
    
    assign Y[0] = I[1] | I[3] | I[5] | I[7];
    
    assign Y[1] = I[2] | I[3] | I[6] | I[7];
    
    assign Y[2] = I[4] | I[5] | I[6] | I[7];
    
    endmodule
    
**RTL LOGIC FOR Encoder 8 To 3 in Dataflow Modelling**

<img width="1902" height="913" alt="image" src="https://github.com/user-attachments/assets/d2d131a1-15f6-4662-a4aa-eb552639d03b" />

**TIMING DIGRAMS FOR Encoder 8 To 3 in Dataflow Modelling**

**RESULTS**

The 8-to-3 encoder is successfully implemented using dataflow modeling, and the simulated output verifies the correct binary code generation for each valid input.




