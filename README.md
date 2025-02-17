## Experiment 1
### Design 1: Simulation of CS Amplifier
### Aim
Simulate the DC analysis, Transient, and AC analysis of a CS amplifier circuit using LTSpice.
### Circuit
![circuit 1](https://github.com/user-attachments/assets/44a7e682-3fae-4dc6-9815-6c28d79776a9)


### Procedure

1. Design the CS amplifier circuit.
2. Naming the NMOS as CMOSN.
3. DC Analysis:Apply the DC voltage of  V<sub>DD</sub> = 1.8 V and V<sub>GS</sub> = 0.9 V . In LTSpice, go to the Simulate option and select Edit Simulation Command.Click on DC Analysis, then press OK.Click on Run in the tab menu to obtain the DC operating point V<sub>out</sub> .Set the Length as constant and determine the Width such that I<sub>D</sub> = 56.8 uA .

4. Transient Analysis:Modify the  V<sub>GS</sub> voltage source to a sine wave input with:
     - DC level= 0.9 V 
     - Amplitude= 50 mV 
     - Frequency= 1 kHz 
     
     In LTSpice, go to Edit Simulation Command, select Transient Analysis. Set the Stop Time as 5ms, then click OK.

5. AC Analysis:In Edit Simulation Command, select AC Analysis.Set the Type of Sweep to Decade.Set Points per Decade to 10.Set the Frequency Range from 0.1 Hz to 1 THz.Click OK. Determine the gain and frequency response of the circuit.

### Calculation

Power Calculation
 P = 100 uW

Drain Equation
V<sub>DD</sub> = V<sub>DS</sub> + I<sub>D</sub>*R<sub>D</sub> 

 P = I*V

Given: I<sub>D</sub> = 55.5 uA, V<sub>DD</sub> = 1.8 V 

Thus V<sub>DS</sub> = V<sub>out</sub> 

R<sub>d</sub>=32.4 Kohm ,but used 8 Kohm

Length= 4 nm

Width=6.6 um(Found by keeping the Length constant).

V<sub>DS</sub>=0.66 V

Q point is (0.66 V,55.55 uA)

## Results:
1.**DC Analysis:**

 ![dc](https://github.com/user-attachments/assets/48efa094-3533-4283-9fc7-3ee53466c092)

drain current I<sub>d</sub>=56.55 uA
V<sub>out</sub>=0.66 V \
Width=6.6 um for length=4 um\

2.**Transient Analysis:**
![TA](https://github.com/user-attachments/assets/b5333f0b-1dfa-4d1f-bdc5-a6a994a8bcd7)



There is 180 degree phase shift between input and output 

3.**AC Analysis:**
![TA](https://github.com/user-attachments/assets/1ae3fe4a-f8d8-4889-a12f-2f64a8a073e6)


Gain=22 dB

## Inference:
1. The drain current is directly impacted by the MOSFET's width.
2. The quantity of drain current can be directly controlled by altering the MOSFET's size.
3. A phase shift of 3.180 degrees between the input and output waveforms
4. The CS amplifier's gain is higher, at 22 dB.(For example, the output signal is 22 times greater than the input signal.)


### Design 2: Simulation of CMOS Amplifier
### Aim
Simulate the DC analysis, Transient, and AC analysis of a CMOS amplifier circuit using LTSpice.
### Circuit
![C2](https://github.com/user-attachments/assets/bd356386-2553-4786-a5f3-6d590d61fde9)


### Procedure

1. Design the CMOS amplifier circuit.
2. Naming the NMOS as CMOSN and PMOS as CMOSP.
3. Apply the DC voltage of  V<sub>DD</sub> = 1.8 V
4. DC sweep Analysis: Go to the edit simulation command and select the DC sweep option and choose:
 -Source name= V<sub>in</sub>.
 -type of Sweep= Linear.
 -start value=0,
 -stop value =V<sub>DD</sub>=1.8 V.
 -increment=0.1.

find the V<sub>in</sub> from the vtc curve  
5. DC Analysis:put the appropriate V<sub>in</sub> value. go to the Simulate option and select Edit Simulation Command.Click on DC Analysis, then press OK.Click on Run in the tab menu to obtain the DC operating point V<sub>out</sub> .Set the Length as constant and determine the Width such that I<sub>D</sub> = 49.25 uA .

6. Transient Analysis:Modify the  V<sub>in</sub> voltage source to a sine wave input with:
     - DC level= 0.9 V 
     - Amplitude= 50 mV 
     - Frequency= 1 kHz 
     
     In LTSpice, go to Edit Simulation Command, select Transient Analysis. Set the Stop Time as 5ms, then click OK.
7. AC Analysis:In Edit Simulation Command, select AC Analysis.Set the Type of Sweep to Decade.Set Points per Decade to 10.Set the Frequency Range from 0.1 Hz to 1 THz.Click OK. Determine the gain and frequency response of the circuit.

### Calculation

 I<sub>D</sub> = 49.29 uA, V<sub>DD</sub> = 1.8 V 

Length M1= 4um\
Width=6.6 um(found by keeping the Length of M1 constant)\
Length M2= 4 um\
Width=6.6 um(found by keeping the Length of M2 constant)\

## Results:
1.**DC Sweep Analysis:**

![dc sweep](https://github.com/user-attachments/assets/14fb7f23-609a-4218-9296-f125e71e31b4)


 the value of the V<sub>in</sub> is selected as 0.8V as it is present in the middle of the saturation region of the VTC Curve.\
2.**DC Analysis:**

![dc r](https://github.com/user-attachments/assets/f734e60b-5b2d-45ca-adfe-801007348a78)


drain current I<sub>d</sub>=49.25 uA
V<sub>out</sub>=1.52 V \
Length M1= 4 um,Width= 6.6 um for M1.\
Length M2= 4 um,Width=6.6 um for M2.\


3.**Transient Analysis:**

![ta b](https://github.com/user-attachments/assets/4975a2b2-1416-4cc3-ac96-0ca8fa277a04)


There is 180 degree phase shift between input and output 

4.**AC Analysis:**

![ac ana](https://github.com/user-attachments/assets/3a0e16e4-4f23-4786-85da-8b0c6c00b9a0)


Gain=0.8 dB

## Inference:
1. The drain current is directly impacted by the MOSFET's width.
2. There is minimal change in the drain current when adjusting the width of PMOS due to altering the MOSFET's M1 dimensions (i.e., I<sub>d</sub> is not significantly affected).-M2-The drain current drastically changes when the NMOS width is changed.
3. An increase in width results in a larger gain and a phase shift of 4.180 degrees between the input and output waveforms.
5. The gain of the CMOS amplifier is 0.8 dB.(For example, the output signal significantly exceeds the input signal by 0.8 times.)
