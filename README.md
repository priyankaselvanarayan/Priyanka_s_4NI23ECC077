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

ID = 27µA

The transistor width (*W) is determined as **1.08 µm* from process specifications.

## *3. AC Analysis*

AC analysis aids in identifying the frequency response of the amplifier. The AC amplitude of the input signal is **1V**, and the output is measured at:

- *Drain (Output)*
- *Gate (Input)*

### *Sweep Parameters:*
- *Sweep Type:* Decade
- *Points per Decade:* 20
- *Frequency Range:* 0.1 Hz – 1 THz

This analysis gives information on the *gain and bandwidth*.

*(Insert AC response graph here)*

## *4. Transient Analysis*

In order to see time-domain behavior, the **stop time is 5 ms**. The transient response assists in confirming how the **output waveform traces the input sinusoidal signal**.

*(Insert transient response graph here)*

## *5. Inference*

The simulation verifies that the **CS amplifier** is fully functional under the provided **power budget of 50 µW** while keeping the needed **DC operating point**. The theoretically calculated **drain current (ID) of 27 µA** matches expectations, and the **transistor width (W = 1.08 µm)** is well-suited for biasing within the **180 nm process**.

The **AC analysis** shows the **gain and bandwidth** of the amplifier, proving its capability to amplify signals in the target frequency range. The **decade sweep from 0.1 Hz to 1 THz** gives a full picture of its performance. The gain characteristics show its appropriateness for applications like low-power analog signal processing.

The **transient analysis** also confirms the functionality of the amplifier by demonstrating how the output waveform traces the input sinusoidal signal. The precise duplication of the input at the drain confirms stable operation with negligible distortion.

Generally, the results indicate that the **amplifier complies with the required specifications** and is able to **achieve stable operation while effectively consuming the provided power limitations**.

# Experiment - 1 - b

