
# D Flip-Flop  

With Regards,  
**Abhitej Divi**

This project involves designing a **D Flip-Flop** to reliably store input data on the rising clock edge and maintain stability during the hold phase. The design also includes a reset feature to initialize the output.  

---

## 1. Design Requirements  

A) Technology: **TSMC 180 nm process**  
B) Supply Voltage: V<sub>dd</sub> = 1.8  
C) Functionality: Must latch the input (D) on the clock edge and hold it until the next triggering edge, with reset control  

---

## 2. Schematic Diagram  

![D Flip-Flop Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/1c598317e1f0790a2ae87186a33a0c7c1a1a180f/dflipflop.png)

---

## 3. Results  
![D Flip-Flop Transient Response](https://github.com/abhitejdivi5/Analog-Blocks/blob/1c598317e1f0790a2ae87186a33a0c7c1a1a180f/dflipflopout.png)

- **Yellow (/res):** Reset signal  
- **Blue (/data):** Input data (D)  
- **Red (/clk):** Clock signal  
- **Red (/out):** Flip-Flop output (Q)  
The transient simulation confirms correct **D Flip-Flop behavior**. The **2ns input data** is sampled on the 2ns period active clock edge and held stable at the output until the next event. The reset operation successfully initializes the output.  

---
