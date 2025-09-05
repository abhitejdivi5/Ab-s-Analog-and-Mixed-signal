# Bootstrapped Switch  

With Regards,  
**Abhitej Divi**

This project involves designing a **Bootstrapped Switch** for sampling and holding the input signal. The circuit utilizes a charge pump, enabling the output to reliably hold the sampled signal during the comparison phase in later steps. The switch is designed to operate with a **4 pF load capacitor**, suitable for sampling into a **10-bit capacitor DAC**.   

---

## 1. Design Requirements  

A) Technology: **TSMC 180 nm process**  
B) Supply Voltage V_dd = 1.8   
C) Load Capacitor = 4 pF  
D) Speed Requirement: Must support **sampling within 2 ns** and **holding for 8 ns**, enabling **100 MS/s ADC operation**  

---

## 2. Schematic Diagram  

![Bootstrapped Switch Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/6bf6383a2450f60f96de05ba46ef886a41f6ee8e/boot.png)

---

## 3. Results  

![Bootstrapped Switch Results](https://github.com/abhitejdivi5/Analog-Blocks/blob/6bf6383a2450f60f96de05ba46ef886a41f6ee8e/boot_2.png)  

With a **4 pF load capacitor**, the bootstrapped switch achieves:  
- **Sampling time** ≈ 2 ns  
- **Hold time** ≈ 8 ns  
- Supports **100 MS/s ADC operation**  
