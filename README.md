#### NAME:RAJKUMAR G
#### REGISTER NUMBER:23003498
#### Experiment 02  Implementation-of-combinational-logic
### AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
### EQUIPMENT REQUIRED:
 Hardware PC Cyclone II, USB flasher Software - Quartus prime 
### Theory:
 A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
### Procedure:
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:*
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6.Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output waveform
### Program:
```
module ex_02(a,b,c,d,f1);
input a,b,c,d;
output f1;
wire x1,x2,x3,x4,x5;
assign x1=(~a)&(~b)&(~c)&(~d);
assign x2=(a) &(~c)&(~d);
assign x3=(~b)& (c) &(~d);
assign x4=(~a)& (b) & (c) & (d);
assign x5=(b) & (~c)&(d);
assign f1=x1|x2|x3|x4|x5;
endmodule
```
### RTL REALIZATION:

![Screenshot 2023-11-20 153654](https://github.com/2005Mukesh/Experiment--02-Implementation-of-combinational-logic-/assets/138849308/b1272672-7ecc-49cd-8b69-b364cbded089)

### TRUTH TABLE:
![image](https://github.com/2005Mukesh/Experiment--02-Implementation-of-combinational-logic-/assets/138849308/a4c0061d-e8e2-476e-b5ca-54c67bf5b1f7)

### TIMING DIAGRAM:
![image](https://github.com/2005Mukesh/Experiment--02-Implementation-of-combinational-logic-/assets/138849308/9cc1bbff-7c60-4bb9-a1e3-fe6024870489)

### Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
