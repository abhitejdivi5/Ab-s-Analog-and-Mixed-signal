
# 1.6V LDO reference

With Regards Abhitej Divi ;)
A Low Dropout Regulator (LDO) is a linear voltage regulator that provides a stable output voltage even when the input voltage is only slightly higher than the desired output voltage. It is widely used in analog, mixed-signal, and digital ICs where clean and noise-free power is critical. This design uses a 1.2 V bandgap reference (BGR) and scales it up to 1.6 V using the LDO.

## 1. Schematic Diagram:
The figure below depicts the schematic diagram for band gap reference using current mirror circuit as current source.
![3 Temperature variation of PTAT,CTAT and VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/LDO.png)
## 2. Result:
#### A. Temperature variation of CTAT, PTAT and V<sub>REF</sub>
Hence, by adding scaled CTAT and PTAT we obtained a band gap reference of ≈ 1.16V

![3 Temperature variation of PTAT,CTAT and VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/LDO_out.png)

