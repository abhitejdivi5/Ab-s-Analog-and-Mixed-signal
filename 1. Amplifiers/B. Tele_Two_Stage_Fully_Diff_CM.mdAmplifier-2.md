
# Fully Differential Two-Stage Op-Amp with Common Mode Feedback

With Regards, Abhitej Divi,

This project involves designing a fully differential two-stage operational amplifier (with a first-stage **differential telescopic amplifier** and a second-stage **common-source** amplifier) that incorporates common-mode feedback. The design targets approximately  dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1pF and 2pF cap loads.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 95dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz 


## 2. Schematic diagram

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/ee27edd41867a941b4efba2cec5413a38bd26f74/tele_diff_crt.png)



## 3. Results
Bode plot is adopted, which effectively depicts the design parameters: 

![Opamp results](https://github.com/abhitejdivi5/Analog-Blocks/blob/ee27edd41867a941b4efba2cec5413a38bd26f74/tele_output_1.png)
Henc,e with 1pF load cap achieved \
Voltage gain (A<sub>v</sub>) = 99dB \
Phase margin = 63° \
Gain Bandwidth Product (GBW) ≈ 243 MHz \

![opamp](https://github.com/abhitejdivi5/Analog-Blocks/blob/ee27edd41867a941b4efba2cec5413a38bd26f74/tele_output_2.png)
Hence, with a 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 99dB \
Phase margin = 60° \
Gain Bandwidth Product (GBW) ≈ 173 MHz \

