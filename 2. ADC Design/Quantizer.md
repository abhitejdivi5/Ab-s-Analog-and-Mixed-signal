# Quantizer  

With Regards,  
**Abhitej Divi**

This project involves designing a **Quantizer**, an essential block in an ADC, responsible for comparing the input analog voltage with a reference and generating the corresponding digital decision. The implemented design uses **Strong-Arm latch** structure to achieve high-speed quantization.  

---

## 1. Design Requirements  

A) Technology: **TSMC 180 nm process**  
B) Supply Voltage: V₍dd₎ = 1.8 V  
C) Input: Differential input pair (Vₚ, Vₙ)  
D) Speed: Designed to operate at **1Ghz** to support 100Mhz speed ADC applications  
E) Functionality: Generate a stable digital output that indicates whether Vₚ > Vₙ  

---

## 2. Schematic Diagram  

![Quantizer Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/7091a1334015cbe741c7df1afca57be6d6aa93ed/quant.png)

---

## 3. Results  

### Case 1: Transient Response

![Quantizer Output 1](https://github.com/abhitejdivi5/Analog-Blocks/blob/7091a1334015cbe741c7df1afca57be6d6aa93ed/quant_out1.png)  

- **Orange (Vₚ):** Positive input  
- **Green (Vₙ):** Negative input  
- **Yellow (/clk):** Clock input  
- **Purple (/on_internal) & Red (/op_internal):** Internal comparator nodes  
- **Brown (/op):** Comparator output  
- **Gray (/on):** Complementary output  

The zoomed transient waveform shows fast switching at the comparator’s decision point, with correct regeneration of outputs.  

---

### Case 2: Extended Transient Response  

![Quantizer Output 2](https://github.com/abhitejdivi5/Analog-Blocks/blob/7091a1334015cbe741c7df1afca57be6d6aa93ed/quant_out_2.png)  

From Figure 2, the comparator can decide approximately 365 ps and precharges in about 100 ps. This speed is sufficient to perform up to 10 comparisons within a 9 ns window, which occurs while the sampling circuit is turned off. As a result, the comparator can reliably resolve the 10-bit decisions required for the SAR ADC.
---

