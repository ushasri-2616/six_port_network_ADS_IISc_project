# Six-Port Microwave Network Simulation using Keysight ADS

## Overview
This project presents the design and simulation of a **Six-Port Microwave Network** using **Keysight Advanced Design System (ADS)**,carried out at IISc Microwave laboratory
The work was carried out by recreating the six-port circuit architecture from a published research paper and verifying its performance through S-parameter simulations.

## Project Objective

The primary objective of this project is to design and simulate a six-port microwave network and analyze its magnitude and phase responses.
The reference paper focuses on six-port interferometry for precise radar and sensing applications operating in the **1–2 GHz** frequency range. The initial circuit was first recreated in ADS before analyzing its performance at different frequencies.


## Reference Paper

**Title:**

*Six-Port Based Interferometry for Precise Radar and Sensing Applications*

**Authors:**

Alexander Koelpin, Fabian Lurz, Sarah Linz, Sebastian Mann, Christoph Will, Stefan Lindner

**Journal:**

Sensors, 2016

**DOI:** https://doi.org/10.3390/s16091556

## Circuit Components

- Wilkinson Power Divider
- Three 90° Hybrid Couplers
- 50 Ω Terminations
- S-Parameter Simulation Controller

# Figure 1 – Reference Circuit
The six-port network architecture was taken as a reference from the published research paper.( attached as figure1 in repository )

# Figure 2 – ADS Circuit Design
The reference architecture was recreated in Keysight ADS using ideal microwave components.
The designed circuit was verified using S-parameter simulation. ( attached as figure2 in repository )

# Figure 3 – Simulation Results (0.5 GHz – 5 GHz)
The circuit was simulated over the frequency range of **0.5 GHz to 5 GHz**. ( attached as figure3 in repository )

## Simulation Observations
The six-port microwave network was simulated in Keysight ADS over the frequency range of **0.5 GHz to 5 GHz** using S-parameter analysis.

### Magnitude Response

- The simulated output ports exhibit an insertion loss of approximately **−6 dB**.
- The observed **−6 dB** response is expected from the six-port architecture. The input signal is initially divided equally by the **Wilkinson Power Divider**, producing a **−3 dB** power split. The signals are then further distributed through the **90° Hybrid Couplers**, resulting in an additional **−3 dB** division. Consequently, each output port receives approximately one-quarter of the input power, corresponding to an insertion loss of **−6 dB**.
- The output responses remain nearly identical throughout the frequency sweep, demonstrating balanced power distribution and correct implementation of the six-port network.
- 
### Phase Response
- The phase responses vary continuously with frequency due to the propagation characteristics of the microwave network.
- The abrupt transitions between **+180°** and **−180°** are caused by **phase wrapping**. ADS represents phase only within the range of **−180° to +180°**; therefore, when the actual phase exceeds this range, it wraps around without affecting the physical behaviour of the circuit.

### Conclusion
The simulation results closely match the expected theoretical behaviour of a six-port microwave network. The approximately **−6 dB** output magnitude confirms proper power division, while the phase responses validate the expected signal relationships introduced by the hybrid couplers. These results demonstrate that the ADS implementation successfully reproduces the reference six-port architecture described in the research paper.


## Results
The simulated six-port network successfully demonstrates:

- Equal power division
- Approximately −6 dB output magnitude
- Expected phase characteristics
- Proper operation over the selected frequency range

## Software Used
- Keysight Advanced Design System (ADS)

## Future Work
- Replace ideal components with microstrip implementations.
- Design the circuit for practical PCB fabrication.

## Acknowledgement
The circuit topology presented in this repository is based on the architecture described in the above research paper.
This project focuses on implementing the reference design in ADS, performing simulations, and analyzing the obtained S-parameter results.
