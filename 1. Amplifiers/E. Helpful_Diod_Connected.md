


# MOS Characterization

With Regards, Abhitej Divi,

This design involves checking the MOS characteristics using a diode-connected transistor. By pushing or pulling current through the circuit and observing how V<sub>GS</sub>, V<sub>DS(sat)</sub>, g<sub>m</sub>, and g<sub>m</sub>/g<sub>ds</sub> vary with current, we can accurately determine transistor behavior. This approach is highly effective for fixing transistor sizes in amplifier designs, as it inherently accounts for all second- and third-order effects, making it more accurate than other methodologies.


## 1. Schematic diagram


## 2. Helpful notes and test bench
- Calculate the required gm from the unity-gain bandwidth requirement:

  ωu = ωp × Av  
  where  
  ωp = 1 / (rout × CL) ,   Av = gm1 × rout  
  Therefore,  
  ωu = gm1 / CL  

- Use the **diode-connected circuit** and fix the current and widths in the circuit.
- Mismatch Relation for the current mirror is given by:

ΔIout / Iout = ( ΔVT / ((VGS − VT)/2) ) + ( ΔK′ / K′ ) + ( Δ(W/L) / (W/L) )

- From the equation, a larger (VGS − VT) (overdrive) reduces mismatch. Use **large overdrive (> 200 mV)** for the tail transistors. Use smaller overdrive (> 100 mV) for the remaining transistors to achieve lower mismatch.
- Stability Analysis:
<img src="https://github.com/abhitejdivi5/Analog-Blocks/blob/main/gm.png" width="400">
Use the depicted circuit diagram and break the loop at the gate of M3. Apply a large capacitor of 1 MF and an inductor of 1 MH, then apply an AC magnitude of 1 V with a phase of 180° at the Vs node, and plot the magnitude and phase of the loop gain.

## 4. Results
Bode plot is adopted, which effectively depicts the design parameters: 

![results](https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/bg.png)
Henc,e with 1pF load cap achieved \
Voltage gain (A<sub>v</sub>) = 27 dB \
Gain Bandwidth Product (GBW) ≈ 417 MHz \

