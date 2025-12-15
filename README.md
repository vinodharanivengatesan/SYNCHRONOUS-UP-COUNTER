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
**UP COUNTER**

1. Open Quartus Prime and create a new project for the 4-bit synchronous up counter.
2. Write the Verilog HDL code using four JK flip-flops with a common clock input.
3. Connect J and K of the LSB flip-flop to logic 1 so it toggles on every clock pulse.
4. Configure the remaining flip-flops so they toggle only when all lower-order Q outputs are high.
5. Compile the design and check for errors.
6. Simulate the circuit and observe the count sequence using the timing diagram.
7. Verify the output values with the truth table to confirm correct up-counting operation.

**DOWN COUNTER**

1. Open Quartus Prime and create a new new project for the down counter.
2. Create a Verilog HDL file and define the module with clock and reset inputs and a multi-bit output.
3. Write the always block triggered on the positive edge of the clock.
4. Apply reset logic to initialize the counter output to its maximum value.
5. On every clock pulse, decrement the counter value by one when reset is inactive.
6. Compile the design and correct any compilation errors.
7. Simulate the circuit using the Simulation Waveform Editor.
8. Observe the output counting sequence in the timing diagram.
9. Verify the results using the truth table to confirm correct down-counting operation.   

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: RegisterNumber:
25015399

**RTL LOGIC COUNTER**
UP COUNTER:
![UP LOGIC](https://github.com/user-attachments/assets/64dcd6e4-6ca1-4b59-9365-b33d3dd61a84)


DOWN COUNTER:
![LOGIC DOWN](https://github.com/user-attachments/assets/dc86f055-27eb-4610-9083-598d3c61c572)



**TIMING DIAGRAM FOR COUNTER**
UP COUNTER:
![T UP](https://github.com/user-attachments/assets/14897e89-a9f1-4841-b75d-43d0739f3288)

DOWN COUNTER:
![down td](https://github.com/user-attachments/assets/bd04d932-1f25-404a-a63a-2d5215f3ce05)




**TRUTH TABLE**
UP COUNTER:
![UP TT](https://github.com/user-attachments/assets/b8e3314e-c270-489e-8e6b-69a68bb13ab4)

DOWN COUNTER:
![down tt](https://github.com/user-attachments/assets/44b441e2-e140-43ea-a379-60319d3a2620)




**RESULTS**
The 4-bit synchronous up counter was successfully implemented and simulated in Quartus Prime. The counter increments its output from 0000 to 1111 on each clock pulse without ripple delay, confirming correct synchronous operation.
