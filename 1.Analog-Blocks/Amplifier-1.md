
# Fully Differential Two-Stage Op-Amp with Common Mode Feedback

With Regards Abhitej Divi,

This project involves designing a fully differential two-stage operational amplifier (with a first-stage differential 5T OTA and a second-stage common-source amplifier) that incorporates common-mode feedback. The design targets approximately 70 dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1pF and 2pF cap loads.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 70dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz 


## 2. Schematic diagram

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/4e4b052f3b0c668dcb9d2615c14acd97f50d47b5/opamp_5t_diff.png)



## 3. Results
Bode plot is adopted which effectively depicts the design parameters: 

![Opamp results](https://github.com/abhitejdivi5/Analog-Blocks/blob/c85a984ae3d491121e4237f9f4b5aad8ecb71f53/opamp_5t_diff_output1.png)

Hence with 1pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 64° \
Gain Bandwidth Product (GBW) ≈ 227 MHz \

Hence with 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 61° \
Gain Bandwidth Product (GBW) ≈ 162 MHz \
