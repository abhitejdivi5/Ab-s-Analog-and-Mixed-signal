
# Self_Biased Band gap reference

With Regards Abhitej Divi ;)

Band gap reference is a circuit which will give constant output voltage with respect to temperature and supply variations.  
We can make a constant voltage reference, cancelling the effect of temperature by combining CTAT and PTAT circuits.

BGR is a major building block of any IC as it is very essential for a circuit to be immune to effect of temperature change. BGR are commonly used in LDO, Buck-boost converter, Regulator, ADC, DAC etc. Although there are other parameters like process variation which might effect 




## 1. Schematic Diagram:
The figure below depicts the schematic diagram for band gap reference using current mirror circuit as current source.

<p align="center">
<img width="900" alt="Schematic Diagram" src="https://github.com/abhitejdivi5/Analog-Blocks/blob/3bbcaa0970d077aff918599a54a19d8e89595596/opamp_bgr.png">
</p>





## 3. Result:
#### A. Temperature variation of CTAT, PTAT and V<sub>REF</sub>
Hence, by adding scaled CTAT and PTAT we obtained a band gap reference of ≈ 1.16V

![3 Temperature variation of PTAT,CTAT and VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/3bbcaa0970d077aff918599a54a19d8e89595596/opamp_bgr_out.png)

#### B. Bell curve of V<sub>REF</sub>
When I zoomed in the graph of V<sub>REF</sub> , it looked like a bell-shaped curve with maximum variation 1.9mV. And we are getting such bell-curved because our CTAT and PTAT are not exact staright lines.

![2 Bell_curve_of_VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/3bbcaa0970d077aff918599a54a19d8e89595596/bamdgap_result_2.png)

#### C. Supply variations on V<sub>REF</sub>
When evaluated with supply variation, we got 53mV deviation over 0.6V.

![4 Supply variations on VREF](https://github.com/abhitejdivi5/Analog-Blocks/blob/a01c0e655bb6987425071c4c4af74f98c9ebc3de/bandgap_result_3.png)

Furthermore, if supply voltage and temperature variations is to be reduced, we need to use complex cascode mirror. Yet again using a cascode structure demands for higher supply voltage so trade-off is to be done as your requirement.

