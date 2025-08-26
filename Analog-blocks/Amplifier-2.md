# Fully Differential two-stage Op-amp with common mode feedback

With Regards Abhitej Divi ;)

This project involves designing a fully differential two-stage operational amplifier (with a first-stage differential 5T OTA and a second-stage common-source amplifier) that incorporates common-mode feedback. The design targets approximately 70 dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1pF and 2pF cap loads.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 70dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
H) Gain Bandwidth Product (GBW) > 150MHz 

## 2. Schematic diagram

![image alt](https://github.com/abhitejdivi5/Analog-Blocks/blob/ede17b1840882ddd305fb75539875c9c78d120df/2stg_opamp_5t.png)

## 3. Results
Bode plot is adopted which effectively depicts the design parameters: 

![image alt](https://github.com/abhitejdivi5/Analog-Blocks/blob/241ce5666b25131bdd4326dcc6162fb48f12b146/1p_load.png)

Hence with 1pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 64° \
Gain Bandwidth Product (GBW) ≈ 227 MHz \


![image alt](https://github.com/abhitejdivi5/Analog-Blocks/blob/241ce5666b25131bdd4326dcc6162fb48f12b146/2p_load.png)

Hence with 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 61° \
Gain Bandwidth Product (GBW) ≈ 162 MHz \
