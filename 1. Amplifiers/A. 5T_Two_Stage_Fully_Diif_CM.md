
# Fully Differential Two-Stage Op-Amp with Common Mode Feedback

With Regards Abhitej Divi,

This project involves designing a fully differential two-stage operational amplifier (with a first-stage differential [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md) and a second-stage common-source amplifier) that incorporates common-mode feedback. The design uses a Miller compensation capacitor for pole splitting and a right-half-plane (RHP) zero-canceling resistor for enhanced stability. It targets approximately 70 dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1 pF and 2 pF capacitive loads.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 70dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz 

#### 2. Helpful Design Notes

- Design the first stage using [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md).
- Use [Helpful Diode Connected](../1.%20Amplifiers/E.%20Helpful_Diod_Connected.md) for transistor sizing.
- After designing the [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md), size the remaining transistors using the phase margin and compensation formulas given below.

---

To achieve better **phase margin**, ensure:

\[
G_{m2} \geq 5 \times G_{m1}
\]

Phase margin expression:

\[
\phi_m = 90^\circ - \tan^{-1}\left(\frac{\omega_{\text{loop}}}{p_2}\right) - \tan^{-1}\left(\frac{\beta \cdot G_{m1}}{G_{m2}}\right)
\]

Loop bandwidth approximation:

\[
\omega_{\text{loop}} = \frac{G_{m1}}{C_c}
\]

Other key relations:

- \( p_2 \approx \frac{G_{m2}}{C_L} \)
- \( G_{m1} = \frac{G_{m2}}{5} \)
- \( A_{\text{loop}} = \frac{\beta \cdot G_{m1}}{\omega C_c} \)

---

### 🧮 Comparison Table: With and Without Compensation Resistor \( R_c \)

| Configuration        | Dominant Pole \(p_1\)      | Non-Dom Pole \(p_2\)         | RHP Zero \(z_1\)          |
|----------------------|----------------------------|-------------------------------|---------------------------|
| **Without \( R_c \)**| \( \frac{1}{R_o C_c} \)     | \( \frac{G_{m2}}{C_L} \)      | \( \frac{G_{m2}}{C_c} \)   |
| **With \( R_c \)**   | \( \frac{1}{R_o C_c} \) `   | \( \frac{G_{m2}}{C_L} \)      | \( \frac{1}{R_c C_c} \)    |


## 3. Schematic diagram

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/4e4b052f3b0c668dcb9d2615c14acd97f50d47b5/opamp_5t_diff.png)



## 4. Results
Bode plot is adopted which effectively depicts the design parameters: 

![Opamp results](https://github.com/abhitejdivi5/Analog-Blocks/blob/c85a984ae3d491121e4237f9f4b5aad8ecb71f53/opamp_5t_diff_output1.png)
Hence with 1pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 63° \
Gain Bandwidth Product (GBW) ≈ 236 MHz \

![opamp](https://github.com/abhitejdivi5/Analog-Blocks/blob/1eb3b59a8cbb0fa0ccb049555863249b4b938e3c/Untitledopamp_5t_diff_output2.png)
Hence with 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 71dB \
Phase margin = 65° \
Gain Bandwidth Product (GBW) ≈ 165 MHz \
