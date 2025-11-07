
# Fully Differential Two-Stage Op-Amp with Common Mode Feedback

With Regards Abhitej Divi,

This project involves designing a fully differential two-stage operational amplifier (with a first-stage differential [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md) and a second-stage common-source amplifier) that incorporates common-mode feedback. The design uses a Miller compensation capacitor for pole splitting and a right-half-plane (RHP) zero-canceling resistor for enhanced stability. It targets approximately 70 dB gain, a 60° phase margin, and stable operation above 150 MHz for both 1 pF and 2 pF capacitive loads.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 70dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz 

## 2. Schematic diagram
![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/4e4b052f3b0c668dcb9d2615c14acd97f50d47b5/opamp_5t_diff.png)

## 3. Helpful Design Notes
- Design the first stage using [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md).
- Use [Helpful Diode Connected](../1.%20Amplifiers/E.%20Helpful_Diod_Connected.md) for transistor sizing. and change the connections as needed.
- After designing the [5T OTA](../1.%20Amplifiers/D.%20NMOS_5T_OTA.md), size the remaining transistors using the phase‑margin and compensation formulas given below. 
- Gain (A) = (Gm₁Gm₂)/(G₁G₂)
- Common-Mode Input Range and Output Swing (Based on Schematic)

#### Input Common-Mode Voltage Limits
$$
V_{icm(max)} = V_{DD} - V_{SG11} + V_{T6}
$$

$$
V_{icm(min)} = V_{SS} + V_{DS9(sat)} + V_{GS6}
$$

#### Output Swing Limits
$$
V_{out(max)} = V_{DD} - V_{SD1(sat)}
$$

$$
V_{out(min)} = V_{SS} + V_{DS15(sat)}
$$

- Phase Margin Condition

$$
\
\phi_m = 90^\circ - \tan^{-1}\!\left(\frac{\omega_{\text{loop}}}{p_2}\right)
          - \tan^{-1}\!\left(\frac{\beta \cdot G_{m1}}{G_{m2}}\right)
\
$$

- To achieve better phase margin, ensure:

$$
G_{m2} \ge  G_{m1}
$$

- this **makes the smaller angle to get high phase**
- Comparison Table: Effect of Compensation Resistor (R<sub>c</sub>)

<p align="center">

| **Configuration** | **Dominant Pole (p₁)** | **Non-Dominant Pole (p₂)** | **Extra Pole (p₃)** | **Zero (z₁)** |
|-------------------|-------------------------|-----------------------------|---------------------|----------------|
| Without R<sub>c</sub> | (G<sub>1</sub> × G<sub>L</sub>) / (C<sub>c</sub> × G<sub>m2</sub>) | G<sub>m2</sub> / C<sub>L</sub> | — | G<sub>m2</sub> / C<sub>c</sub> |
| With R<sub>c</sub>    | (G<sub>1</sub> × G<sub>L</sub>) / (C<sub>c</sub> × G<sub>m2</sub>) | G<sub>m2</sub> / C<sub>L</sub> | 1 / (R<sub>c</sub> × C<sub>1</sub>) | 1 / ((1 / G<sub>m2</sub> − R<sub>c</sub>) × C<sub>c</sub>) |

</p>

Observations
- p₁ and p₂ remain approximately the same.  
- The phase margin improves due to zero cancellation or its shift toward the LHP.
- make sure R<sub>c</sub> limited by `1/Gm2`


## 4. Results
Bode plot is adopted, which effectively depicts the design parameters: 

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
