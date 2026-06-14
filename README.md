# Wireless Performance Evaluation of Digital Modulation Techniques over an AWGN Channel
## Project Description
This project focuses on the simulation and performance assessment of multiple digital modulation techniques under the influence of an Additive White Gaussian Noise (AWGN) channel. The simulation is implemented in Python and aims to investigate how different modulation schemes balance data transmission efficiency and communication reliability.
## Modulation Schemes Included
- BPSK (Binary Phase Shift Keying) – 1 bit per symbol
- QPSK (Quadrature Phase Shift Keying) – 2 bits per symbol
- 16-QAM (16-Quadrature Amplitude Modulation) – 4 bits per symbol
- 64-QAM (64-Quadrature Amplitude Modulation) – 6 bits per symbol
- 256-QAM (256-Quadrature Amplitude Modulation) – 8 bits per symbol
## Simulation Methodology
The simulation processes **200,000** bits for each experiment while evaluating system performance across an SNR range of **0 dB to 20 dB**.
## AWGN Channel Model
The communication channel is modeled using Additive White Gaussian Noise. Noise samples with a Gaussian distribution are introduced into the transmitted symbols according to the selected Signal-to-Noise Ratio (SNR).
## Gray Coding
Gray coding is employed for symbol mapping to reduce bit errors. Since neighboring constellation points differ by only one bit, symbol detection mistakes typically result in fewer bit errors.
## Receiver Detection
At the receiver side, a Maximum Likelihood (ML) detector is implemented using the nearest-neighbor approach. Received symbols are assigned to the closest constellation point to recover the transmitted data.
## Theoretical Verification
To validate the simulation results, the measured Bit Error Rate (BER) values are compared with theoretical BER expressions derived from the Q-function and complementary error function (erfc).
## Results and Analysis
## BER Performance at a Target BER of 10⁻³
The minimum SNR required by each modulation scheme to achieve a BER of approximately 10⁻³ was observed as follows:
| Modulation Scheme | Required SNR (Approx.) |
|-------------------|------------------------|
| BPSK              | 7 dB                   |
| QPSK              | 7 dB                   |
| 16-QAM            | 11 dB                  |
| 64-QAM            | 15 dB                  |
| 256-QAM           | 20 dB                  |
## Key Observation
The results clearly demonstrate the trade-off between **spectral efficiency** and **noise immunity**. Lower-order modulation schemes such as BPSK and QPSK provide excellent error performance in noisy environments but transmit fewer bits per symbol. In contrast, higher-order schemes such as 64-QAM and 256-QAM offer significantly higher data rates but require stronger signal quality to maintain reliable communication.

This principle forms the foundation of **Adaptive Modulation and Coding (AMC)** techniques used in modern wireless technologies such as LTE, 5G, and Wi-Fi systems, where modulation levels are dynamically adjusted according to channel conditions.
## Technologies Used
- Python
- NumPy
- Matplotlib
- SciPy
## Learning Outcomes
- Understanding digital modulation techniques
- BER analysis over AWGN channels
- Comparison of theoretical and simulated results
- Impact of SNR on communication reliability
- Spectral efficiency versus error performance trade-offs
