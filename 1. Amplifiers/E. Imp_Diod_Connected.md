


# MOS Characterization

With Regards, Abhitej Divi,

This design involves checking the MOS characteristics using a diode-connected transistor. By pushing or pulling current through the circuit and observing how V<sub>GS</sub>, V<sub>DS(sat)</sub>, g<sub>m</sub>, and g<sub>m</sub>/g<sub>ds</sub> vary with current, we can accurately determine transistor behavior. This approach is highly effective for fixing transistor sizes in amplifier designs, as it inherently accounts for all second- and third-order effects, making it more accurate than other methodologies.


## 1. Schematic diagram
<table>
  <tr>
    <td><img src="https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/nmoscha.png" width="400"/></td>
    <td><img src="https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/pmosch.png" width="400"/></td>
  </tr>
</table>

## 2. Helpful notes and test bench
- **I** is the bias current per unit width. Sweep **I** in logarithmic steps from a small value (e.g., 0.1 µA/µm) up to 1 mA/µm and simulate the operating point.

Plot the following parameters versus **I** for various transistor widths.  
*(The testbench used for this measurement is shown in the reference figure.)*

- **VGS** – Gate-to-source voltage. Used to identify a “reasonable” operating region.  
- **VDSAT** – Saturation voltage required across the device. Similar to the above, used to determine a valid operating region.  
- **gm** – Transconductance per unit transistor (1 µm / L). Helps in determining the required device sizing for a given gm.  
- **gm/gds** – Intrinsic gain. Used to determine the bias current density or device length required to achieve a desired DC gain.

In future designs, use the same transistor parameters (**W**, **L**, **Ad**, **As**, **Pd**, **Ps**) but adjust the **multiplier (m)** as needed to meet the required specifications.

![results](https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/nmoschtest.png)
## 4. Results
The NMOS parameters VGS, VDSAT, gm, and gm/gds are plotted versus ID on separate graphs for various transistor widths, as shown in the figure, to determine the appropriate width for the NMOS device.

![results](https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/nmoschoout.png)

The PMOS parameters VGS, VDSAT, gm, and gm/gds are plotted versus ID on separate graphs for various transistor widths, as shown in the figure, to determine the appropriate width for the NMOS device.

![results](https://raw.githubusercontent.com/abhitejdivi5/Analog-Blocks/main/pmoschout.png)

