
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

![Opamp schematic](https://github.com/abhitejdivi5/Ab-s-Analog-and-Mixed-signal/blob/main/Analog-Blocks/opamp_5t_diff.png)



## 3. Results
Bode plot is adopted which effectively depicts the design parameters: 



Hence with 1pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 64° \
Gain Bandwidth Product (GBW) ≈ 227 MHz \

Hence with 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 61° \
Gain Bandwidth Product (GBW) ≈ 162 MHz \
