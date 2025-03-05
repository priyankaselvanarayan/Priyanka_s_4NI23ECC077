# Experiment 3 - Differential Amplifier
## Aim:
Design and analyse the MOS-Differential amplifier circuit for the following specifications. Design Differential amplifier and Perform DC analysis and extract the required parameters for the following specifications. VDD = 3.3V , P<=3mV , Vin(CM)=1.72V , Vo(CM)=1.8V , Vp=0.7V

## Theory - Differential Amplifier
It is an amplifier that amplifies the difference present between two signals which leads to the elimination of the signal that is in common that further leads to noise cancelling.The differential Amplifiers can be built using Transistors or Op-Amps.Differential Amplifiers using MOSFET has 2 Transistors (NPN) , 2 Drain Resistors RD , a Source Resistor RS or a current source which is common for both the braches as seen in the figure below , a Power Supply VDD , input signals V1 & V2 are applied at gates of the transistors that are equal and this voltage is called Common Mode Input Voltage and the output is taken from the drain terminal of the transistors. The advantage for opting a differential amplifier is that it has High Impedance, low power consumption and mainly for the noise cancellation as mentioned earlier.




## Design:






## Equipments Required
1. DC Power Supply , VDD=3.3V
2. AC Power Supply , Vi(CM)=1.72V (2nos)
3. Resistors , RD=3.3Kohm (2 nos) ,RSS=770ohm
4. Current Source , ISS=0.9A
5. CMOSN (2nos)
## Procedure:
1. Open LT-spice software and copy the librabry file(tsmc.lib) to the folder you are working in to get the proper values with respect to the NMOS.
2. Select the components with the you have designed theoritically and place the components you require to rig-up your circuit accordingly and link them using the 
 wire option.
3. Rigup the circuit as shown in fig , adjust the values of length and RD so that we obtain the required value of ID and Vo(CM).
4. Once you end up getting the required valued of ID and Vo(CM) , import library path .lib tsmc018.lib that contains all accurate values of MOSFET.
5. Now simulate the circuit you designed , place the .op cammand obtained and check for the values of ID and Vo(CM) , if there is no match with the theoritical 
 value derived , then adjust width values of MOSFETs to get accurate ID value and adjust RD values to get accurate value for Vo(CM).
6. Next simulate the circuit again , opt for transient analysis of 5m cycle , we obtain input and output waveforms separately and together as well.
7. In case of DC analysis , firstly change the DC source option to sinusoidal waveform option then we'll get a command SINE(1.72 50m 1k) place it near the circuit. now select AC analysis option values given as Decade , 20 , 0.1 , 1T . Get the output value while placing the probe at output region.
8. Repeat same steps for all the circuits .   

  


