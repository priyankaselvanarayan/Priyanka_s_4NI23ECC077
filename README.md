# Experiment - 1 - a

## *1. Introduction*

The report here shows the analysis of a Common-Source (CS) amplifier implemented based on a 180 nm TSMC process. The operation of the amplifier is at **VDD = 1.8V** with an available **power budget of 50 µW**. The **gate voltage (Vg)** is comprised of a **DC offset of 0.6V** and a **sinusoidal input of 50 mV amplitude at 1 kHz**.

## Aim

- Determining the **DC Operating Point** (Drain Current, ID)
- Calculating the **Transistor Width (W)**
- Evaluating **AC Response** (Gain and Bandwidth)
- Observing **Transient Behavior**

## *2. DC Analysis*

In order to keep the amplifier within the power limit, we apply the power equation:

P = V * ID

With **P = 50 µW** and **VDD = 1.8V**, we find **ID**:

ID = 50 µW / 1.8V

ID = 27.78µA

The transistor width (*W) is determined as **1.08 µm* from process specifications.

![image](https://github.com/user-attachments/assets/f58cd8f2-d031-42bf-b06d-582c2b84e1c6)

![image](https://github.com/user-attachments/assets/079cb26c-1b47-444b-9bb2-dd6f03f0fa38)


## *3. AC Analysis*

AC analysis aids in identifying the frequency response of the amplifier. The AC amplitude of the input signal is **1V**, and the output is measured at:

- *Drain (Output)*
- *Gate (Input)*

### *Sweep Parameters:*
- *Sweep Type:* Decade
- *Points per Decade:* 20
- *Frequency Range:* 0.1 Hz – 1 THz

This analysis gives information on the *gain and bandwidth*.

![image](https://github.com/user-attachments/assets/7de9cb9d-b6c8-4462-a7ff-1cd0bf1e7216)


## *4. Transient Analysis*

In order to see time-domain behavior, the **stop time is 5 ms**. The transient response assists in confirming how the **output waveform traces the input sinusoidal signal**.

![image](https://github.com/user-attachments/assets/3dd9b985-c701-4a41-98c0-28dd01e4b050)


## *5. Inference*

The simulation verifies that the **CS amplifier** is fully functional under the provided **power budget of 50 µW** while keeping the needed **DC operating point**. The theoretically calculated **drain current (ID) of 27 µA** matches expectations, and the **transistor width (W = 1.08 µm)** is well-suited for biasing within the **180 nm process**.

The **AC analysis** shows the **gain and bandwidth** of the amplifier, proving its capability to amplify signals in the target frequency range. The **decade sweep from 0.1 Hz to 1 THz** gives a full picture of its performance. The gain characteristics show its appropriateness for applications like low-power analog signal processing.

The **transient analysis** also confirms the functionality of the amplifier by demonstrating how the output waveform traces the input sinusoidal signal. The precise duplication of the input at the drain confirms stable operation with negligible distortion.

Generally, the results indicate that the **amplifier complies with the required specifications** and is able to **achieve stable operation while effectively consuming the provided power limitations**.

# Experiment - 1 - b

# Analysis of CS Amplifier

## Objective
The objective of this analysis is to analyze the behavior of a Common Source (CS) amplifier with a specified supply voltage of 1.8V and power consumption of 50μW. We will determine the DC operating point, including the drain current (ID) and investigate the response of the amplifier to sinusoidal signals. The gate voltage (VG) will have an offset of 0.9V, 50mV amplitude, and a frequency of 1kHz. The analysis will be done in three phases: DC analysis, AC analysis, and transient analysis. The idea is to determine how the amplifier works at various frequencies and over a period of time. The final output will be used to design the amplifier with best operating conditions and expected response.

## Specifications of NMOS and PMOS

### PMOS Transistor:
- Source: Connected to the supply voltage(VDD) = 1.8 V
- Gate: Connected to the gate voltage ????
???? = 0.7 ???? V G 
=0.7V
- Drain: Connected to the drain of the NMOS transistor

### NMOS Transistor:
- Source: Grounded (0V)
- Gate: Connected to the gate voltage ????
???? = 0.7 ???? V G 
=0.7V
- Drain: Connected to the drain of the PMOS transistor

## NMOS and PMOS Dimensions
In order to make sure that the amplifier is running with a drain current of 27.78μA and a total power of 50μW, we will have to determine suitable W (width) and L (length) values for both the NMOS and PMOS transistors. These are important dimensions to meet the design requirements and ensure proper functioning of the amplifier.

- **PMOS Transistor (W/L):** To be filled in later.
- **NMOS Transistor (W/L):** To be filled in later.

## DC Operating Point Calculation
Given the supply voltage ????
????
???? = 1.8 ???? V DD 
=1.8V and the total power ???? = 50 ???? ???? P=50μW, the drain current ????
???? I D 
 is calculated as:

```
P = VDD × ID
ID = P / VDD = (50 × 10^-6 W) / (1.8V) = 27.78μA
```

Thus, the drain current ????
???? I D 
 is approximately **27.78μA**. The gate voltage is set to 0.7V as a DC offset.

## AC Analysis Setup
For AC analysis, the gate voltage ????
???? V G 
 is modulated as a sinusoidal signal with the following parameters:

- **DC offset:** ????
???? 0 = 0.7 ???? V g0 
=0.7V
- **Amplitude:** ????
????
????
????
????
????
????
????
????
????
???? = 50 ???? ???? V g amplitude 
=50mV
- **Frequency:** ???? = 1 ???? ???? ???? f=1kHz

AC analysis will have the following frequency sweep settings:

- **Sweep Type:** Decade Sweep
- **Number of Sweeps per Decade:** 20
- **Start Frequency:** 0.1Hz
- **Stop Frequency:** 1THz

_Leave space for graph of AC sweep results._

## Transient Analysis Setup
In transient analysis, we will analyze the time-domain response of the amplifier with the sinusoidal input. The stop time for the simulation is 5 milliseconds.

- **Stop Time:** 5 milliseconds (5m)

_Leave space for graph of transient analysis results._

## Inference on DC, AC, and Transient Analyses
### DC Analysis
- The DC operating point assists in establishing the baseline conditions of the amplifier, with the drain current set to 27.78μA.
- This calculation keeps the amplifier in its proper operating region.

### AC Analysis
- The AC analysis, using a decade sweep from 0.1Hz to 1THz, enables us to analyze the frequency response of the amplifier.
- It helps in understanding amplification and attenuation at various frequencies.

### Transient Analysis
- Transient analysis gives information about the amplifier's response to the sinusoidal input in the time domain.
- It allows for evaluation of stability, transient response, and settling time over a 5ms time period.


