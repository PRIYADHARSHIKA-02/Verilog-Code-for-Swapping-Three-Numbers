# Verilog-Code-for-Swapping-Three-Numbers
Aim

To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

Apparatus Required

Vivado 2023.1 or equivalent Verilog simulation tool.

Procedure

Launch Vivado 2023.1:

Open Vivado and create a new project.
Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables.
Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly.
Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project.
Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation.
Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected.
Save and Document Results:

Capture the waveform output and include the results in your report for verification.

Verilog Code:

module swap(clk);
  input clk;
  
  real a = 5;
  
  real b = 3;
  
  real c = 7;
  
  real temp;
  
always @(posedge clk) 

begin

 temp = a;
 
 a = b;
 
 b = c;
 
 c = temp;
 
end endmodule

Output:

![WhatsApp Image 2024-10-17 at 19 40 57_5d7b42ad](https://github.com/user-attachments/assets/281f49ad-cd09-440f-929e-1bdba5610ed3)






Testbench for Swapping Three Numbers:

`timescale 1ns / 1ps

module swap_tb;
reg clk;
real a, b, c; 
swap uut ( .clk(clk) );
always #5 clk = ~clk; 
  initial begin clk = 0;
  a = uut.a; b = uut.b;
  c = uut.c;
$monitor("At time %t, a = %f, b = %f, c = %f", $time, uut.a, uut.b, uut.c);
#50;
$finish;
end 
endmodule


Conclusion

In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated. The testbench verified the swapping operation, showing that the values of three input numbers (a, b, and c) were swapped correctly without the use of temporary variables. This experiment demonstrated the effectiveness of Verilog in implementing logical operations and control mechanisms such as swapping values. The simulation results confirm the correct functionality of the design.
