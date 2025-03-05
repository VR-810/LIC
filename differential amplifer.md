### **"Differential Amplifier"**

The output voltage of a differentiator amplifier, sometimes referred to as a differentiating amplifier or a differentiator circuit, is directly proportional to the time derivative of the input.  In other words, either the RC time constant or the time derivative can be used to adjust the output voltage.
 What is the function of a differential amplifier?
 The differential amplifier's job is to boost the heart signal's amplitude so that it may be transformed into a digital format.  By carefully choosing external resistors to connect between the input and output terminals, the circuit's gain can be changed.

### **question:Vdd=2.5v , p<=3mw , Vicm=1.3v, Vocm=1.25v , Vp=0.5v , vocm=1.4v**
**Circuit 1** <br>
![Image](https://github.com/user-attachments/assets/4a8c18fd-31d4-42e2-84f7-ccaa40dd426d)


### Step 1:Dc analysis design Rd and Rss
![dc calc](https://github.com/user-attachments/assets/9effe2da-0b1a-43fd-aa7e-5bf8af3cdf2d)



Based on the computation, we have discovered  The Iss value is 1mA.
 Id1 as well as Id2 as 0.5mA
 Rd is equal to 1.833kohm.
 416.66 ohm for Rss
 1.3 - 0.5 - 0.8 v = vgs=vg - vp
 The formula for Vov is vgs - vth = 0.8v - 0.366v = 0.434v.

 Go to Configure Analysis and choose Dc operating Point to specify the operating point.

 to establish the proper operating point  Change the width and length settings. 
 length = 180n <br> width = 8.05u



![Screenshot 2025-03-04 183108](https://github.com/user-attachments/assets/29bcd7c2-01f8-4ccd-8868-6e676a54e5b3)

### **Analysis**

**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>
| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.38484V**             | **0.5V**                |
| **1.4V**                            | **1.23925V**                 | **0.572037V**               |




![Screenshot 2025-03-04 183146](https://github.com/user-attachments/assets/9ac2d4c0-65d6-4c50-9f07-6bba79589cb3)
### Effect of VICM on Vout and vp

As the common-mode input voltage \( VICM \) increases, the source voltage \( VP \) also increases, causing a shift in the operating point. This leads to a higher drain current, resulting in a greater voltage drop across \( RD \), which reduces \( Vout \).

### **Calculate maximum input ,output Swing  and gain**

change amplitude value from 50m to 600m




![Screenshot 2025-03-04 184021](https://github.com/user-attachments/assets/0164cb4d-2498-4a61-9d69-3bc4b7263f45)



![Screenshot 2025-03-04 104945](https://github.com/user-attachments/assets/e10f6351-9e54-4a54-9a92-3483ef9dcb76)
### **TRANSIENT ANALYSIS**
go to configure Analysis and select transient analysis then <br>
stop time as 5m <br>
time to start saving data as 0 <br>

• Waveform Type: Sine Wave
• Amplitude: 20 mV
• DC Offset: 1.3V
• Frequency: 1 kHz

And in V2 phi(deg) as 180


![Screenshot 2025-03-04 190934](https://github.com/user-attachments/assets/d61525d3-b43a-4dd1-8ada-21d0767d6c94)
### **AC Analysis**

go to configure analysis and select AC Analysis
• Type of sweep: Decade
• Number of points per decade: 5
• Start frequency: 0.1 Hz
• Stop frequency: 1 THz

Set <br>
AC Amplitude as 1 and AC Phase as 0 in V1 <br>
AC Amplitude as 1 and AC Phase as 180 in V2 <br>


![Screenshot 2025-03-04 191749](https://github.com/user-attachments/assets/84496068-358c-4a9d-9a47-9233deccde8e)


![Screenshot 2025-03-04 192520](https://github.com/user-attachments/assets/e98c280e-085f-4943-af51-a74986cc7228)

### CIRCUIT 2:
Replacing resistor with current source

![Screenshot 2025-03-04 193927](https://github.com/user-attachments/assets/58d25de9-2acd-45fb-bedf-93c3b865662a)
# DC ANALYSIS:

![Screenshot 2025-03-04 193540](https://github.com/user-attachments/assets/e5736bde-72ff-4d48-869f-b9d4794621c1)
### **Analysis**

**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>

| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.587**             | **0.537**                |
| **1.4V**                            | **1.587V**                 | **0.634**               |


![Screenshot 2025-03-04 193803](https://github.com/user-attachments/assets/a6a491b0-53ed-4f60-ac84-862a4e9531ee)
# transient analysis:


![Screenshot 2025-03-04 195407](https://github.com/user-attachments/assets/48474381-dae1-4dbd-af4a-828f2c4dbea9)

By changing amplitude from 20mv to 500 mv


![Screenshot 2025-03-04 195034](https://github.com/user-attachments/assets/32784df2-340d-4ff7-8c9e-b73e019e3efb)

### AC ANALYSIS :

![Screenshot 2025-03-04 195813](https://github.com/user-attachments/assets/9459856e-2c86-4cbd-b613-21fa5706749d)

### CIRCUIT 3:
Replacing current Source with MOSFET 


![Screenshot 2025-03-04 200424](https://github.com/user-attachments/assets/29db27ff-2882-4c49-bce8-ee48b11dc4e2)
How can I locate Vb?
 Vb = vth + Vp
 Vb is equal to 0.366v + 0.5v.
 Vb = 0.866v
 Change the third MOSFET's width to determine the operating point while maintaining the same length. 
 I obtained a width of 12.6u for the approximate operating point.


# dc analysis:


![Screenshot 2025-03-04 201336](https://github.com/user-attachments/assets/aa465d5c-54cc-4657-84ed-256c35610e47)
**Increase Vicm from 1.3v to 1.4v and observe Vocm and Vp** <br>

| **Common-Mode Input Voltage (V_ICM)** | **Output Voltage (V_out)** | **Voltage at Point P (V_P)** |
|--------------------------------------|--------------------------|--------------------------|
| **1.3V**                            | **1.394v**             | **0.497v**                |
| **1.4V**                            | **1.368V**                 | **0.587v**               |



![Screenshot 2025-03-04 201411](https://github.com/user-attachments/assets/a39e7127-5adb-429a-a985-9055d03b5696)
# transient analysis:




![trans 1](https://github.com/user-attachments/assets/1258abba-908d-48dd-bfaa-5a02670745d1)

BY changing amplitude from 20mv to 500mv
input and output swing




![amp 1](https://github.com/user-attachments/assets/2dc7b33f-2bec-4d5d-965d-d470cdeb7393)

# AC ANALYSIS:



![ac 1](https://github.com/user-attachments/assets/3f790afc-ef6f-4237-b407-fd6b32626083)


# Inference:  
This experiment investigated three different designs of differential amplifiers that have distinct effects on gain, bandwidth, and stability: resistor-based, current source-based, and NMOS-based.  

 Resistor: low gain, low CMRR, high bandwidth.  
 High gain, high CMRR, and somewhat reduced bandwidth are the current sources.  
 - NMOS (CMOSN): Maximum profit.  

  Ideal Setup Depending on Need:  
 1. Resistor → High bandwidth  
 2. NMOS (CMOSN) → maximum gain  
 3. Improved CMRR → NMOS or current source (CMOSN)




## result:

1. **Circuit-1:**  The circuit's proper behavior as a differential pair is confirmed by the transient response of **Circuit-1:**.  
    -  A respectable gain and strong common-mode noise rejection are shown by the AC analysis.  
    -  According to the DC analysis, when the input voltages are equivalent, the MOSFETs operate at saturation and have equal drain currents.  

 2. **Circuit-2:** - The signals have improved symmetry due to a more balanced transient response.  
    -  According to the AC study, this circuit has a larger frequency range and a greater gain than  Circuit 1.  
    The DC analysis shows that the biasing is more stable when a current source is used rather than a resistor.  


 3.  **Circuit-3:**-The transient response of circuit number three guarantees signal accuracy and enhances performance.  
    A wider frequency range and even more gain are revealed by the AC study.  
    -  The output changes as anticipated, according to the DC sweep analysis.  
    The DC analysis verifies that the tail current is efficiently controlled by the MOSFET-based current source.




### CIRCUIT 4:


![Screenshot 2025-03-04 223152](https://github.com/user-attachments/assets/6646efcb-08b5-4458-892c-9e4e8676b95d)

## DC ANALYSIS:



![Screenshot 2025-03-04 224318](https://github.com/user-attachments/assets/5bd7277d-3990-48a5-8ac8-94ac43c8be45)


