# Deskmini-A300-SOC-and-CPU-Voltage-Hardware-Modification
Deskmini A300 SOC Voltage modded to 1100mV - VCORE Max 1388mV

  I was unable to get my Ryzen 4600G stable with PBO turned on. I tried to increase the SOC voltage using different BIOS versions but nothing worked.

  After modifying the SOC voltage to around 1.100V, there were still stability issues. I managed to solve this with a +112mV VCORE offset, by adding another resistor modification.

  My Deskmini A300 is using BIOS P3.60S with a Ryzen 4600G an PBO is set to enabled.


The Deskmini a300 uses a DS3667BB-02 Dual-Output PWM Controller.
  Data sheet: Dual-Output PWM Controller - DS3667BB-02.pdf


SOC Voltage
  Linking 5V via 150K resistor to RT3667BB pin 24 (OFSA) about 112mV Offset to CPU VSOC. For 4600G, SOC increased from 1000mv 1100mV
  NOTE: In pictures this resistor is linked with the white wires.

  82K resistor, offset ~206mV
  120K resistor, offset ~150mV
  150K resistor, offset ~112mV
  240K resistor, offset ~75mV
  360K resistor, offset ~50mV


CPU VCore Voltage Offset
  Linking 5V via 17.5K resistor to RT3667BB pin 23 (OFS) ~160mV Offset to CPU VCORE. For 4650G, VCORE max increased to 1388mV (PBO ON)
  NOTE: In pictures these resistors are linked with the pink (red) wires.

  17.5K resistor (22Kin parallel with a 150K and a 220K resistor), offset ~160mV

  22K resistor in parallel with a 150K resistor, offset ~90mV  - unstable


**Notes:**

  1. Although I have been as diligent as possible, I accept no responsibility for the information in the document, or the damage that it could lead to.

  2. This is very risky, you can destroy your Deskmini A300 CPU RAM drives etc.

  3. The components are very very small, only do this if you are very experienced soldering tiny components and have the correct equipment (soldering iorn with a very small diameter tip), and a lot of time.

  4. Do not heat the entire resistor, it will detach from the board and it will be game over. Only touch one end of the component with the soldering iron, and only for a fraction of a second. I used leaded solder and an iron tip temperature of 380 degrees celsius.
  
  5. Disconnect the power and all peripherals during the procedure.
  
  6. Use wire with a very small diameter.
  
