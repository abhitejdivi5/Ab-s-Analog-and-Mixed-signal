# Bootstrapped Switch  

With Regards,  
**Abhitej Divi**

This project involves designing a **Bootstrapped Switch** for sampling and holding the input signal. The circuit utilizes a charge pump, enabling the output to reliably hold the sampled signal during the comparison phase in later steps. The switch is designed to operate with a **5 pF load capacitor**, suitable for sampling into a **10-bit capacitor DAC**.   

---

## 1. Design Requirements  

A) Technology: **TSMC 180 nm process**  
B) Supply Voltage V_dd = 1.8   
C) Load Capacitor = 5 pF  
D) Speed Requirement: Must support **sampling within 2 ns** and **holding for 8 ns**, enabling **100 MS/s ADC operation**  

---

## 2. Schematic Diagram  

![Bootstrapped Switch Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/boot.png)

### Clock Feedthrough Effect

After sampling the input onto the capacitor, a small parasitic capacitance exists between the gate and drain of the sampling transistor.  
This capacitance couples a portion of the clock signal to the output, slightly altering the stored voltage.  
This effect, known as **clock feedthrough**, introduces an error (typically in the millivolt range) that can significantly impact ADC accuracy.  

\[
\Delta V_{error} = \frac{C_{p2}}{C_{p2} + C} \times V_{clock}
\]
To minimize this error, a **dummy transistor** identical to the sampling switch is added.  
The dummy transistor cancels the feedthrough effect caused by the sampling transistor’s gate-to-drain capacitance (C<sub>gd</sub>), improving sampling accuracy.  



## 3. Results  

![Bootstrapped Switch Results](https://github.com/abhitejdivi5/Analog-Blocks/blob/6bf6383a2450f60f96de05ba46ef886a41f6ee8e/boot_2.png)  

With a **4 pF load capacitor**, the bootstrapped switch achieves:  
- **Sampling time** ≈ 2 ns  
- **Hold time** ≈ 8 ns  
- Supports **100 MS/s ADC operation**  
