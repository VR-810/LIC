# Telescopic Operational Amplifier Design

- **M. Niranjan**  
  Electronics and Communication Engineering  
  NIE Mysuru, India  
  2023ec_mniranjan_a@nie.ac.in

- **Mallikarjuna V R**  
  Electronics and Communication Engineering  
  NIE Mysuru, India  
  2023ec_mallikarjunavr_a@nie.ac.in

---

##  Objective

To design a telescopic operational amplifier (op-amp) that meets the following specifications:

- **Power Supply Voltage (VDD):** 3V  
- **Differential Output Swing (Vout1 - Vout2):** ±3V  
- **Input Offset Voltage (Vos):** ≤ 10mV  
- **Voltage Gain (Av):** ≥ 1000 V/V (60 dB)

---

##  Design Specifications

- **Power Supply:** Operates at VDD = 3V
- **Differential Input Stage:** NMOS transistors for sensing input voltage difference
- **Active Load:** PMOS transistors convert current to voltage
- **Cascoding:** Telescopic architecture improves gain and output resistance
- **Voltage Gain:** ≥ 1000 V/V
- **Output Swing:** ±3V
- **Offset Voltage:** ≤ 10 mV

---

##  Design Description

- **Differential Input Stage:**  
  NMOS transistors (M1, M2) sense the voltage difference between `Vin1` and `Vin2`.

- **Active PMOS Load:**  
  PMOS transistors (M5, M6) convert the differential current into output voltages (`Vout1`, `Vout2`).

- **Telescopic Cascode Structure:**  
  Cascode NMOS (M3, M4) and PMOS (M7, M8) transistors improve gain by increasing output resistance.

- **Biasing and Current Mirrors:**  
  Transistors like MB1, MB2 provide necessary bias voltages and distribute a reference bias current (~3 µA).

##circuit diagram
![image](https://github.com/user-attachments/assets/0a46fd5d-cb41-40b8-bf74-bc5c1ef41678)


##  Design Calculations

![image](https://github.com/user-attachments/assets/bda0f242-9846-48a5-a33c-9fe62bfde746)
![image](https://github.com/user-attachments/assets/9906faeb-6fdd-47db-a575-97297c301298)



##  LTSpice Simulation Results
![image](https://github.com/user-attachments/assets/760ea37d-694b-4a47-9ef8-5b37e636bce0)

![image](https://github.com/user-attachments/assets/fa09ef1f-e9d1-4611-8ac6-6abb57f41d33)

![image](https://github.com/user-attachments/assets/c1b8f686-15fd-49e6-86db-5faab097a2ef)




##  Waveform


![image](https://github.com/user-attachments/assets/e0de1dc1-84af-4a20-a49c-f2d6bf53af9d)


##  Conclusion

The telescopic operational amplifier design meets essential criteria of:
- High voltage gain
- Wide output swing
- Low input offset voltage

Its differential input stage, cascode architecture, and well-designed current mirror biasing make it suitable for precision analog applications with minimal distortion.

---

##  Summary

This project designed a telescopic cascode op-amp using:
- NMOS differential input stage
- PMOS active load
- Cascode transistors for enhanced gain and resistance
- Current mirrors for consistent biasing

Key specs:
- Gain ≥ 1000 V/V
- Output Swing ±3V
- Offset Voltage ≤ 10 mV

The design is robust and suitable for high-performance analog circuits.
