
# 0.6V Fractional Band gap reference

With Regards Abhitej Divi ;)

Band gap reference is a circuit which will give constant output voltage with respect to temperature and supply variations.  
We can make a constant voltage reference, cancelling the effect of temperature by combining CTAT and PTAT circuits. BGR is a major building block of any IC as it is very essential for a circuit to be immune to effect of temperature change. From the op-amp-based bandgap, we can obtain a fixed voltage of 1.25 V. If a lower on-chip reference voltage is required, a fractional bandgap reference circuit can be used




## 1. Schematic Diagram:
The figure below depicts the schematic diagram for band gap reference using current mirror circuit as current source.
![2 Bell_curve_of_VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/Fractional%20BandGap.png)

## 2. Result:
#### A. Temperature variation of CTAT, PTAT and V<sub>REF</sub>
Hence, by adding scaled CTAT and PTAT we obtained a fractional band gap reference of ≈ 630mV

![2 Bell_curve_of_VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/fractional_bandgap_out.png)
