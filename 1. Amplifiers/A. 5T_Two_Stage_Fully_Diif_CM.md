
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

#### Phase Margin Condition

To achieve better **phase margin**, ensure:

$$
G_{m2} \ge 5 \times G_{m1}
$$

#### Phase Margin Expression
#### Phase Margin Expression

![eq2](https://latex.codecogs.com/svg.image?\phi_m%20=%2090^{\circ}%20-%20\tan^{-1}\!\left(\frac{\omega_{\text{loop}}}{p_2}\right)%20-%20\tan^{-1}\!\left(\frac{\beta%20\cdot%20G_{m1}}{G_{m2}}\right))

From the equation, larger \(G_{m2}\) pushes \(p_2\) higher and the RHP zero farther, improving phase margin.

\[
\phi_m = 90^\circ - \tan^{-1}\!\left(\frac{\omega_{\text{loop}}}{p_2}\right)
          - \tan^{-1}\!\left(\frac{\beta \cdot G_{m1}}{G_{m2}}\right)
\]

From the equation, larger \( G_{m2} \) pushes \( p_2 \) higher and the RHP zero farther, improving phase margin.


#### Loop Bandwidth Approximation

$$
\omega_{\text{loop}} = \frac{G_{m1}}{C_c}
$$


#### Other Key Relations

- p₂ ≈ Gm₂ / CL  
- Gm₁ = Gm₂ / 5  
- Aloop = β × Gm₁ / (ω × Cc)


#### Comparison Table: With and Without Compensation Resistor (Rc)

| Configuration | Dominant Pole (p₁) | Non‑Dom Pole (p₂) | RHP Zero (z₁) |
|---------------|---------------------|-------------------|----------------|
| Without (Rc)  | 1 / (Ro × Cc) | Gm₂ / CL | Gm₂ / Cc |
| With (Rc)     | 1 / (Ro × Cc) | Gm₂ / CL | 1 / (Rc × Cc) |


Using Rc helps cancel or move the RHP zero to the LHP side, stabilizing the op‑amp.




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
