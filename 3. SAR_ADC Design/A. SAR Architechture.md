
# SAR Architecture and flowchart

With Regards,  
**Abhitej Divi**  

This project involves designing a **10-bit Successive Approximation Register (SAR) ADC** capable of operating at **100 MHz**. The architecture integrates multiple custom-designed building blocks, including the **Bootstrapped Switch**, **Strong Arm Latch Comparator**, **D Flip-Flops**, **Binary Weighted Split C Capacitor DAC working on monotonic switching**, and **NOR Gate for comparator reset**. 

## 1. Block Diagram
![SAR ADC Output](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/SARarch.png)

- For the fully differential SAR ADC, the analog inputs are sampled using a **bootstrapped switch** ([link]), which maintains an almost constant on-resistance across the entire input range.

- The sampled input is then compared using a **strong-arm latch comparator** ([link]), which offers dynamic power consumption only — meaning power is consumed only during comparison events.

- After the first comparison, the result is stored in the **MSB D flip-flop** ([link]). Simultaneously, a signal is sent to the **reset block** (for the next comparison) and to the **switching circuit** ([link]), which updates the capacitor connection based on the comparator output.

- If the comparator output is **‘1’**, the positive capacitor is switched to ground; otherwise, the negative capacitor is switched to ground. This method is known as **monotonic switching**.

- After storing, resetting, and switching, the comparator becomes ready for the next comparison. The process repeats for all remaining bits (typically 9 more for a 10-bit ADC). - Once all bits are resolved, the input sampling phase begins again for the next conversion cycle.

## 2. Flowchart
The flowchart is depicted below.

![SAR ADC Output](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/flowch.drawio.png)

