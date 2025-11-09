

# PMOS input 5t-ota

With Regards, Abhitej Divi,

This project involves the design of a five-transistor differential amplifier. The procedure is explained briefly, focusing on achieving the required gain and speed for a given load of 1 pF.

## 1. Design Requirement: 

A) Technology: TSMC 180nm process \
B) Supply Voltage (V<sub>dd</sub>) = 1.8 V \
C) Voltage gain (A<sub>v</sub>) = 95dB \
D) Load Capacitor (C<sub>L</sub>) = 1pF and 2pF \
E) Gain Bandwidth Product (GBW) > 150MHz


## 2. Schematic diagram

![PMOS 5T Amplifier](https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/pmos5t.png)

## 3. Helpful notes
- Calculate the required gm from the unity-gain bandwidth requirement:

  ωu = ωp × Av  
  where  
  ωp = 1 / (rout × CL) ,   Av = gm1 × rout  
  Therefore,  
  ωu = gm1 / CL  

- Use the **diode-connected circuit** and fix the current in the circuit.
- Mismatch Relation for the current mirror is given by:

ΔIout / Iout = ( ΔVT / ((VGS − VT)/2) ) + ( ΔK′ / K′ ) + ( Δ(W/L) / (W/L) )

- From the equation, a larger (VGS − VT) (overdrive) reduces mismatch. Use **large overdrive (> 200 mV)** for the tail transistors. Use smaller overdrive (> 100 mV) for the remaining transistors to achieve lower mismatch.
- Stability Analysis:
<img src="https://github.com/abhitejdivi5/Analog-Blocks/blob/main/gm.png" width="400">
Use the depicted circuit diagram and break the loop at the gate of M3. Apply a large capacitor of 1 MF and an inductor of 1 MH, then apply an AC magnitude of 1 V with a phase of 180° at the Vs node, and plot the magnitude and phase of the loop gain.

## 4. Results
Bode plot is adopted, which effectively depicts the design parameters: 

![Opamp results](https://github.com/abhitejdivi5/Analog-Blocks/blob/ee27edd41867a941b4efba2cec5413a38bd26f74/pmos5t.png)
Henc,e with 1pF load cap achieved \
Voltage gain (A<sub>v</sub>) = 99dB \
Phase margin = 63° \
Gain Bandwidth Product (GBW) ≈ 243 MHz \

![opamp](https://github.com/abhitejdivi5/Analog-Blocks/blob/ee27edd41867a941b4efba2cec5413a38bd26f74/tele_output_2.png)
Hence, with a 2pF load cap achived\
Voltage gain (A<sub>v</sub>) = 99dB \
Phase margin = 60° \
Gain Bandwidth Product (GBW) ≈ 173 MHz \
