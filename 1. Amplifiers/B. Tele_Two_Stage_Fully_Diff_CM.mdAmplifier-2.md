
# Fully Differential Two-Stage Self-Zero-Canceling Compensated Op-Amp with Common Mode Feedback

With Regards, Abhitej Divi,

This project involves designing a fully differential two-stage operational amplifier (with a first-stage **differential telescopic amplifier** and a second-stage **common-source** amplifier) that incorporates common-mode feedback. The design targets approximately  dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1pF and 2pF cap loads. The design uses an Ahuja compensation technique, implemented with a cascoded transistor.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 95dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz 


## 2. Schematic diagram

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/tele_ahuza.png)


## 3. Helpful notes
- Design the [two-stage opamp](../1.%20Amplifiers/A.%20) and [5T ota](../1.%20Amplifiers/A.%20)  .
- We can use the same compensation methods as those applied in a two-stage op-amp, or the following techniques.
- Common-Mode Input Range and Output Swing (Based on Schematic)

$$
V_{icm(max)} = V_{b56} - V_{SG34} + V_{T29}
$$

$$
V_{icm(min)} = V_{Ov25(sat)} + V_{GS29}
$$

$$
V_{out(max)} = V_{DD} - V_{Ov30(sat)}
$$

$$
V_{out(min)} = V_{Ov31(sat)}
$$
#### Compensation
- In Miller compensation, a Right-Half-Plane (RHP) zero appears due to the **feed-forward path** from the input to the output, since the compensation capacitor is bidirectional.  
- The idea is to **cancel this feed-forward path** by using a Current-Controlled Current Source (CCCS).  
- The disadvantage of this method is that it requires an additional current source to activate the transistor used for zero cancellation.  
- However, in a telescopic amplifier, the **cascode transistor** itself can serve as the **zero-canceling device**, eliminating the need for any **extra current source or additional power consumption**.
- For additional compensation techniques, refer to the [two-stage opamp](../1.%20Amplifiers/A.%20).

  ![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/ahuza_block.png)

- Dominant Pole:
  $p_1 \approx \dfrac{G_{1}}{C_c \times G_{m2} / G_{L}}$

- New Non-Dominant Pole: 
  $p_{2,new} \approx \dfrac{G_{m2} \times C_c}{C_L \times C_1}$

- The new $p_{2,new}$ is higher than the original $p_2$ (without compensation), which results in an improved phase margin.




## 4. Results
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

