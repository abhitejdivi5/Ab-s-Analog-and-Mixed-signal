# Capacitor DAC Switching And Reset Block for Latch

## • Capacitor DAC
- The **capacitor DAC array** performs charge redistribution after each comparison to generate the next reference voltage level for the comparator.  
- It uses **monotonic switching**, where each capacitor is selectively connected to ground or reference voltage (Vref) based on the comparator output, ensuring low power consumption and reduced switching energy.
- As shown in the figure, the Switch is designed using the AND gate and an inverter.

![SAR ADC Schematic](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/switch.png)

## • Reset Block
- The **reset block** discharges the comparator make-ready latch for next comparison and DAC nodes after each bit decision, ensuring the next comparison starts from a defined initial condition.  
- The valid signal (output of the comparator) and sampling signals are used as an input because, during these moments, the comparator is not in use and needs to be reset.
![SAR ADC Output](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/reset.png)


