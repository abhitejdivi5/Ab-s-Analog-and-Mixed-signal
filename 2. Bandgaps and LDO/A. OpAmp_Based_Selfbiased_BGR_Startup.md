
# Self_Biased Band gap reference

With Regards Abhitej Divi ;)

Band gap reference is a circuit which will give constant output voltage with respect to temperature and supply variations.  
We can make a constant voltage reference, cancelling the effect of temperature by combining CTAT and PTAT circuits.

BGR is a major building block of any IC as it is very essential for a circuit to be immune to effect of temperature change. BGR are commonly used in LDO, Buck-boost converter, Regulator, ADC, DAC etc. Although there are other parameters like process variation which might effect 




## 1. Schematic Diagram:
The figure below depicts the schematic diagram for band gap reference using current mirror circuit as current source.

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr.png)






## 3. Result:
#### A. Temperature variation of CTAT, PTAT and V<sub>REF</sub>
Hence, by adding scaled CTAT and PTAT we obtained a band gap reference of ≈ 1.16V

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr_out.png)


#### B. Supply variations on V<sub>REF</sub>
When evaluated with supply variation, we got 53mV deviation over 0.6V.

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr_out2.png)

Furthermore, if supply voltage and temperature variations is to be reduced, we need to use complex cascode mirror. Yet again using a cascode structure demands for higher supply voltage so trade-off is to be done as your requirement.

