# Logic Driver Circuit (LDC)

With Regards, Abhitej Divi,

The Logic Driver Circuit (LDC) processes the outputs from both the Voltage Sensing Circuit (VSC) and the Current Sensing Circuit (CSC).  
It generates four different logic outputs (A, B, C, D), each representing the solar panel’s operating condition.  

The outputs are based on the combination of high/low values from the VSC and CSC:

| VSC Output | CSC Output | LDC Output | Condition             |
|------------|------------|------------|-----------------------|
| 0          | 0          | A          | Unstable / No fault   |
| 0          | 1          | B          | Short-circuit fault   |
| 1          | 0          | C          | Open-circuit fault    |
| 1          | 1          | D          | Ignore condition      |

---

## 1. Circuit Diagram

Below is the designed **Logic Driver Circuit (LDC):**

![Logic Driver Circuit](https://github.com/abhitejdivi5/Analog-Blocks/blob/664ce4df7c5828f0521eba92fa0c384afb48e2e8/logic%20driver.jpg)

---

## 2. Simulation Results

The transient simulation confirms the correct logic behavior of the LDC. Each combination of VSC and CSC outputs generates the expected fault indicator (A, B, C, or D).  

![Logic Driver Output](https://github.com/abhitejdivi5/Analog-Blocks/blob/664ce4df7c5828f0521eba92fa0c384afb48e2e8/lo_out.jpg)

---

## 3. Summary
The LDC ensures reliable classification of solar panel operating faults, providing digital outputs to the next state decision stage for further processing.
