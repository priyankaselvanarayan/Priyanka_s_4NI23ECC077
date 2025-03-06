# Experiment 3 - Differential Amplifier
## Aim:
Design and analyse the MOS-Differential amplifier circuit for the following specifications. Design Differential amplifier and Perform DC analysis and extract the required parameters for the following specifications. VDD = 3.3V , P<=3mV , Vin(CM)=1.72V , Vo(CM)=1.8V , Vp=0.7V

## Theory - Differential Amplifier
It is an amplifier that amplifies the difference present between two signals which leads to the elimination of the signal that is in common that further leads to noise cancelling.The differential Amplifiers can be built using Transistors or Op-Amps.Differential Amplifiers using MOSFET has 2 Transistors (NPN) , 2 Drain Resistors RD , a Source Resistor RS or a current source which is common for both the braches as seen in the figure below , a Power Supply VDD , input signals V1 & V2 are applied at gates of the transistors that are equal and this voltage is called Common Mode Input Voltage and the output is taken from the drain terminal of the transistors. The advantage for opting a differential amplifier is that it has High Impedance, low power consumption and mainly for the noise cancellation as mentioned earlier.




## Design:


![image](https://github.com/user-attachments/assets/169809e9-8068-4c76-ab6c-366c85bddda7)







## Equipments Required
1. DC Power Supply , VDD=3.3V
2. DC Power Supply , Vi(CM)=1.72V (2nos)
3. Resistors , RD=3.3Kohm (2 nos) ,RSS=770ohm
4. Current Source , ISS=0.9A
5. CMOSN
## Procedure:
1. Open LT-spice software and copy the librabry file(tsmc.lib) to the folder you are working in to get the proper values with respect to the NMOS.
2. Select the components with the you have designed theoritically and place the components you require to rig-up your circuit accordingly and link them using the 
 wire option.
3. Rigup the circuit as shown in fig , adjust the values of length and RD so that we obtain the required value of ID and Vo(CM).
4. Once you end up getting the required valued of ID and Vo(CM) , import library path .lib tsmc018.lib that contains all accurate values of MOSFET.
5. Now simulate the circuit you designed , place the .op cammand obtained and check for the values of ID and Vo(CM) , if there is no match with the theoritical 
 value derived , then adjust width values of MOSFETs to get accurate ID value and adjust RD values to get accurate value for Vo(CM).
6. Next simulate the circuit again , opt for transient analysis of 5m cycle , we obtain input and output waveforms separately and together as well.
7. In case of AC analysis , firstly change the DC source option to sinusoidal waveform option then we'll get a command SINE(1.72 50m 1k) place it near the circuit. now select AC analysis option values given as Decade , 20 , 0.1 , 1T . Get the output value while placing the probe at output region.
8. Repeat same steps for all the circuits .   

## Circuit 1:


![image](https://github.com/user-attachments/assets/7468a247-fc59-4d87-a061-137e2db5c52f)



## Components Required :
1. CMOSN (2nos)
2. Resistors , RD=3.3Kohm (2nos), RSS=770ohm
3. DC Power supplies , VDD=3.3V , Vi(CM)=1.72V
  
## DC Analysis :
To perform DC Analysis select DC op pnt in the edit simulation. 


Set the appropriate values for W/L to obtain desired ID, and also set RD to obtain required value of Vo(CM).


![image](https://github.com/user-attachments/assets/eec77da0-3a05-46e0-bad6-590a5fcec2ab)


Here , to get ID (expected) = 0.45Awe have:


L = 180nm

W = 2.425um


To get Vo(CM) (expected) = 1.81V we have:


RD = 3.3094Kohm


After DC Analysis , we got:


ID_1 = 0.000450233A

ID_2 = 0.000450233A

Vo(CM)_1 = 1.81V

Vo(CM)_2 = 1.81V


![image](https://github.com/user-attachments/assets/aae1d420-a64f-4870-8dbb-e925ec150948)


## Transient Analysis:
 Transient Analysis showcases the behaviour of the circuits when it undergoes sudden transition from one steady-state to another.To perform Transient Analysis opt for transient analysis in edit simulation , give stop time as 5ms and run the simulation and observe the graph appeared below. And also calculate the gain.
 
 
 ![image](https://github.com/user-attachments/assets/7bac5821-b6d0-48eb-950f-d5d0c2d72806)

 Vi(CM) = 0.0602V

 Vo(CM) = 0.0475V
 
 Gain,A = Vo(CM)/Vi(CM) = 0.0475/0.0602 = 0.789036545 V/V 
 
 Gain in dB = 20log( )
 
 ## AC Analysis :
  Select the AC Analysis in edit simulation and select Decade for type of sweep , enter 20m for number of points per decade , 0.1 will be the start frequency and 1T will be stop frequency. 

![image](https://github.com/user-attachments/assets/c3df848a-a6d9-4172-8207-ffd72b7a08af)

## Circuit - 2:
 Replace RSS with a Current Source of 0.9mA supply.

![image](https://github.com/user-attachments/assets/a8e34490-77c8-41f4-9532-bcc17d017e5e)

## DC Analysis :
 To perform DC Analysis select DC op pnt in the edit simulation. 
Set the appropriate values for W/L to obtain desired ID, and also set RD to obtain required value of Vo(CM).

![image](https://github.com/user-attachments/assets/96f5d555-0674-4d09-b0f5-32f4c9ba6bb3)

for, 

L = 180nm

W = 6um 

![image](https://github.com/user-attachments/assets/9a900364-13e4-44f3-a412-5cb0d1329bd5)

we have got:

ID_1 = 0.45A

ID_2 = 0.45A

Vo(CM)_1 = 1.81V

Vo(CM)_2 = 1.81V

## Transient Analysis :
 To perform Transient Analysis opt for transient analysis in edit simulation , give stop time as 5ms and run the simulation and observe the graph appeared below. And also calculate the gain.
 
 
 Vo(CM) = 0.2998V 
 
 Vi(CM) = 0.0482V
 
 Gain,A = Vo(CM)/Vi(CM) = 0.2998/0.0482 = 6.21991701 V/V
 
 Gain in dB = 20lag( )
 
 ![image](https://github.com/user-attachments/assets/e4935764-c423-4f3a-8c18-45d167fc04f8)

## AC Analysis :

![image](https://github.com/user-attachments/assets/83b3f13e-d33f-43a5-967e-0ddc29b23abf)

## Circuit-3 :
 Replace Current Source with a CMOSN with Vp = 0.4V 

![image](https://github.com/user-attachments/assets/3159d669-b38e-4fbc-ac95-ec0e08414ed2)

Vary W/L of new MOSFET 

![image](https://github.com/user-attachments/assets/949a9688-4fe4-4f06-af0f-f4d3a697fbf5)

L = 180nm 

W = 6um 
 ## DC Analysis:
 Set the appropriate values for W/L to obtain desired ID, and also set RD to obtain required value of Vo(CM).

![image](https://github.com/user-attachments/assets/92f7d546-5a10-4498-86bb-0f389f13a8bc)

for,


L = 180nm

W = 0.851um


we got,

![image](https://github.com/user-attachments/assets/fe8a5340-52f7-432b-8296-1b1bdfa242f4)

ID_1 = 0.450818A

ID_2 = 0.450818A

Vo(CM)_1 = 1.81003V

Vo(CM)_2 = 1.81003V

## Transient Analysis :

![image](https://github.com/user-attachments/assets/47ebe88b-18d6-4290-84e7-0197443e48d1)

Vo(CM) = 0.0561V 

Vi(CM) = 0.0481V

Gain,A = Vo(CM)/Vi(CM) = 0.0561/0.0481 = 1.16632017 V/V

Gain in dB = 20lag( )

## AC Analysis:

![image](https://github.com/user-attachments/assets/c35aa9d3-bfc8-4b4c-9cd4-51fbe4a8e47d)

## Result :
## 1. Circuit-1:
   The DC Analysis shows that the MOSFETs operate in saturation with balanced drain currents when input voltages are equal.
   The Transient response confirms proper differential behaviour.
   The AC Analysis gives us the gain and common-mode rejection .
## 2. Circuit-2:
   Replacing the resistor with a current source improves bias stability, as seen in the DC Analysis.
   The Transient response is more stable , ensuring better symmetry.
   The AC Analysis indicates the gain and bandwidth increased.
## 3. Circuit-3:
   The DC Analysis confirms that the MOSFET-based current source regulates the tail current efficiently.
   The Transient response maintains signal accurancy with improved performance.
   The AC Analysis shows higher gain and bandwidth.
   The DC sweep analysis validates expected output variations. 

## Inference :
This experiment explored differential amplifier configurations: resistor-based , current source-based and CMOSN-based , each affecting gain, bandwidth , stability differently. 

Resistor: High bandwidth, low gain, low CMRR.

Current source: High gain, high CMRR, slightly lower bandwidth.

CMOSN: Highest gain.

Best Configuration Based on Need:

1.High bandwidth- Resistor 

2.Maximum gain- CMOSN 

3.Better CMRR- Current source or CMOSN 


     
   

 














