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
```
 1.Initialize the shift register to known state (e.g., all zeros).
 2.Input a bit seially into the shift register.
 3.Shift the contents of the register one position to the right.
 4.Output the shifted bit from the last stage of the register.
 5.Repeat steps 2-4 for each bit you want to input and shift.
 ```
 

**PROGRAM**

 
```
Developed by:GOBIKA K 
RegisterNumber:212222050013
```
![code11](https://github.com/Gobikakannan/SYNCHRONOUS-UP-COUNTER/assets/163496346/54aaed01-4d73-4f0a-9433-688d80cff8b5)


**RTL LOGIC UP COUNTER**
![diagram 11](https://github.com/Gobikakannan/SYNCHRONOUS-UP-COUNTER/assets/163496346/a08a3682-05e2-4380-be2b-b4854eb6f9bd)

**TIMING DIAGRAM FOR IP COUNTER**
![output11](https://github.com/Gobikakannan/SYNCHRONOUS-UP-COUNTER/assets/163496346/45456986-dc00-48f0-8a64-47c94f8763b1)

#### TRUTH TABLE:
![table11](https://github.com/Gobikakannan/SYNCHRONOUS-UP-COUNTER/assets/163496346/7462405c-bf39-40c7-80b1-038860ad67f0)

#### RESULTS:
   Hence a 4 bit synchronous up counter is implemented correctly.
