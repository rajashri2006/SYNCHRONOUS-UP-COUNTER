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
1. Understand the Counter Behavior
Inputs:

clk: Clock signal.
reset: Resets the counter to 0.
Output:

count: 4-bit binary value representing the current count.
Behavior:

On the rising edge of the clock:
If reset = 1, the counter resets to 0.
If reset = 0, the counter increments by 1.
After reaching 1111 (15 in decimal), it wraps around to 0000.



**PROGRAM**


Developed by:Rajashri I RegisterNumber:24900207

![DE ex11 code](https://github.com/user-attachments/assets/3eca743b-3319-43c9-a5bd-6d1094e16b2c)


**RTL LOGIC UP COUNTER**

![DE ex11 diagram](https://github.com/user-attachments/assets/d856640e-0da5-42c7-8285-46e74f983c59)


**TIMING DIAGRAM FOR IP COUNTER**

![DE ex11 waveform](https://github.com/user-attachments/assets/d372efa8-51c5-4bf1-a4f3-a5fe8ce14f6c)


**TRUTH TABLE**

![4 bit counter](https://github.com/user-attachments/assets/e6ee4fde-bc6d-47db-9323-ee7c85742fcf)


**RESULTS**

The implementation of 4 bit synchronous up counter and validate functionality.

