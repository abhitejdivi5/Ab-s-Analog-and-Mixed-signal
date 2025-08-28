# 10-bit SAR ADC  

With Regards,  
**Abhitej Divi**  

This project involves designing a **10-bit Successive Approximation Register (SAR) ADC** capable of operating at **100 MHz**. The architecture integrates multiple custom-designed building blocks, including the **Bootstrapped Switch**, **Strong Arm Latch Comparator**, **D Flip-Flops**, **Binary Weighted Split C Capacitor DAC**, and **NOR Gate for comparator reset**. 

## 1. Design Requirements  

A) Technology: **TSMC 180 nm process**  
B) Supply Voltage: V₍dd₎ = 1.8 V  
C) Resolution: **10 bits**  
D) Sampling Frequency: **100 MS/s**  
E) Input Type: Differential analog input  
F) Output: 10-bit digital word  

---

## 2. Schematic Diagram  

![SAR ADC Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/d516c81f145fc15fae534168c0ce1013487cfc44/10_bit_sar.png)

The schematic shows the integration of:  
- **Bootstrapped Switch** for high-speed sampling without distortion  
- **Split Capacitor DAC Array** for binary-weighted charge redistribution  
- **Strong Arm Latch Comparator** for high-speed comparison  
- **D Flip-Flops and SAR Logic** for sequential control and bit storage  
- **NOR Gate control logic** for timing and reset functions  

---

## 3. Results  

### Transient Response  

![SAR ADC Output](https://github.com/abhitejdivi5/Analog-Blocks/blob/d516c81f145fc15fae534168c0ce1013487cfc44/SAR%20out.png)

- **/pi:** Input pulse trigger  
- **/valid:** Indicates comparator operation and valid decision phases  
- **/pi1 – /pi10:** Control pulses generated for successive approximation  

The simulation confirms that:  
- The comparator resolves each decision within ~365 ps and precharges in ~100 ps.  
- This timing allows **10 comparisons to be completed within 9 ns**, enabling reliable 10-bit conversion at 100 MS/s.  

---

## 4. Summary  

The designed **10-bit SAR ADC** demonstrates high-speed **TSMC 180 nm CMOS**, achieving:  
- **100 MS/s sampling rate**  
- **10-bit resolution**
- **SQNR = 61.83**

This design validates the integration of the Bootstrapped Switch, Strong Arm Latch, DFFs, and Split Capacitor DAC into a fully functional mixed-signal ADC architecture.  

---

