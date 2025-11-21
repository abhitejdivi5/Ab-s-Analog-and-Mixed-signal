## Continuous Time Pipeline ADC (Ongoing work)
![Pad Layout](https://github.com/abhitejdivi5/Analog-Blocks/blob/main/pipe.drawio.png)  


**Problem 1 – Antialiasing Filter Complexity**  
Every ADC needs an antialiasing filter to remove high-frequency components that can alias into the signal band after sampling.  
For a small oversampling ratio (OSR), the filter must have a very steep roll-off, resulting in high order, large power, and high area.  
Such filters add noise and distortion, especially in wideband designs.

**Problem 2 – Power-Hungry Buffer**  
The switched-capacitor input of discrete-time ADCs draws large transient currents during sampling.  
A buffer is required to drive this load linearly, but it consumes high power and adds both noise and distortion.  
This makes the analog front end inefficient.

**Problem 3 – Inefficient Filter + ADC Cascade**  
When the antialias filter and ADC are separate blocks, both consume significant power and contribute noise.  
Increasing filter order further increases power roughly proportional to the square of the order, making the system inefficient.

**Solution 1 – Combine Filtering and Quantization**  
The Continuous-Time Pipeline (CTP) ADC merges the antialias filter and ADC into a single block.  
The filter inherently provides antialiasing and amplifies only the residue signal (difference between input and its coarse digital version).  
Since only a small residue is amplified, the system remains linear and avoids saturation.

**Solution 2 – Remove the Buffer**  
The CTP ADC eliminates the need for a power-hungry buffer by presenting a resistive input.  
No large current spikes occur at the input, reducing power, noise, and distortion while simplifying the overall design.

**Solution 3 – Break the Power–Noise Trade-Off**  
Multistage CTP architectures achieve higher-order antialiasing without increasing power or noise quadratically.  
Later stages handle smaller residue signals, keeping noise and distortion minimal and improving power efficiency.

**Summary**  
CTP ADC integrates antialias filtering and analog-to-digital conversion in one structure.  
It removes the buffer, lowers noise, saves power, and breaks the traditional power–noise trade-off — a fundamental improvement over the classic filter + ADC cascade.

