
# Op-Amp Based Self-Biased Bandgap Reference with Startup Circuit

With Regards Abhitej Divi ;)

Band gap reference is a circuit which will give constant output voltage with respect to temperature and supply variations. This particular BGR design, shown below, includes a startup circuit, an op-amp to ensure both inputs maintain the same voltage, and the main BGR core. The op-amp is self-biased using the BGR itself.

## 1. Schematic Diagram:
The figure below depicts the schematic diagram for band gap reference using **Error Amplifier**, **Main BGR block**, and **Startup Circuit**
![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr.png)
Error Amplifier
An amplifier with a gain of 55 dB ensures there is no voltage error between the two input nodes.

Main BGR Block
The current mirror ensures equal current flow through both branches of the BGR. The generated current is also used to bias the amplifier.

Startup Circuit
Ensures that the circuit starts up correctly and settles into the desired steady-state operating point after power-up.


## 2. Result:
#### A. Temperature variation of CTAT, PTAT and V<sub>REF</sub>
Hence, by adding scaled CTAT and PTAT we obtained a band gap reference of ≈ 1.25V

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr_out.png)


#### B. Supply variations on V<sub>REF</sub>
When evaluated with supply variation, almost constant from supply of 1.3v to 6v

![Opamp schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/opamp_bgr_out2.png)



