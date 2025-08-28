### Solar Panel Diagnostic System – Block Diagram

![Block Diagram](https://github.com/abhitejdivi5/Analog-Blocks/blob/df47d6f5411742e944274c6822c2df526b0bffc6/block.png)

**Explanation:**

1. **Solar Panel (SP)**  
   - Provides the input. Its voltage and current are continuously monitored.

2. **Voltage Sensing Circuit (VSC)**  
   - Scales down the solar panel’s voltage (using a resistor divider) for safe processing.

3. **Current Sensing Circuit (CSC)**  
   - Measures the solar panel’s current to determine its operating condition.

4. **Logic Driver Circuit (LDC)**  
   - Processes signals from VSC and CSC and drives the digital logic stage.

5. **Logic Gates (XOR)**  
   - Detects faults: outputs **high** when the panel is shorted or open.

6. **Memory + Reset Circuit**  
   - Stores fault information until reset.  
   - Ensures the fault indication (e.g., LED) stays active until the issue is cleared.
