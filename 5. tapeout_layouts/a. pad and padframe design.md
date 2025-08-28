## Pad Design with Static Diode Discharge

The **pad design** provides the interface between the integrated circuit (IC) 
and external environment. Each pad (70 µm × 70 µm) is constructed using 
a stack of six metal layers for robust via connections. To protect the chip from 
electrostatic discharge (ESD), diodes are connected to **VDD** and **GND**.  

This ensures that any external voltage surges are safely clamped and do not 
damage the internal circuitry.

![Pad Layout](https://github.com/abhitejdivi5/Analog-Blocks/blob/4f57557c35835dbc94b154398e7f25e7ff81bd60/6metalpad.png)  
*Figure: Pad layout with static diode discharge protection.*

---

## Padframe Design

The **padframe** houses all external connections and surrounds the IC core. 
In this design, **32 pads** are placed around the periphery, consisting of:  

- **I/O pads** for signal interfacing.  
- **VDD and GND pads** distributed Vdd, gnd rail uniformly for power and ground.  


![Padframe Layout](https://github.com/abhitejdivi5/Analog-Blocks/blob/4f57557c35835dbc94b154398e7f25e7ff81bd60/padframe.png)  
*Figure: Padframe design showing distributed power and I/O pads.*

