# Frequency Division Multiplexing (FDM) in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]

Figure 1 illustrates a typical communication system consisting of an emitter, a channel, and a receiver. The emitter includes components that aid in encoding, modulation, and shaping signals, transmitting the signal through the channel, and the receiver aids in demodulation, equalization, and decoding to generate data.
Figure 1: Simplified physical layer of the communication system
This project utilizes MATLAB for modeling and simulation of OFDM and GFDM systems. By analyzing the signal spectrum, constellation diagrams, eye diagrams, and comparing bit error rate (BER) and symbol error rate (SER) under different signal-to-noise ratios (SNR), the two systems are compared. The results indicate that GFDM offers better spectral efficiency, although OFDM performs better in terms of BER. However, it is observed that better equalization methods can improve BER for GFDM. A primary disadvantage of GFDM is its increased complexity in design.
Method 2.1 GFDM and OFDM Emitters
The block diagrams for the emitters of OFDM and GFDM systems are shown in Figures 2.1a and 2.1b respectively. The following table provides the functionality and implementation details for each module:
Before serialization for transmission, the signal format of the OFDM and GFDM blocks is shown in Figures 2.1c and 2.1d, with N representing the number of subcarriers, K the number of blocks, and M the number of subsymbols CP. The length of the cyclic prefix is indicated.
2.2 Channel Model
For this project, an adaptive white Gaussian noise (AWGN) was used to simulate the channel. The additive Gaussian white noise (AWGN) model describes the stochastic impact of the noise signal on the desired signal within the channel. The noise is generated using the MATLAB randn() function. The effect of the channel is to linearly add white noise to the signal.
The capacity of the AWGN channel is given by C = 1/2 log(1 + P/N), where N is the noise density and P is the signal power.
2.3 GFDM and OFDM Receivers
The designed OFDM and GFDM signal receivers are shown in Figures 2.3a and 2.3b respectively. The following table discusses the functionality and implementation details for each module:
Simulation results analysis comprehensively analyzes and compares OFDM systems and GFDM systems through the following methods:
3.1 Spectral comparison of the OFDM and GFDM signals generated
As shown in Figure 3.1a, the signal spectra of the OFDM and GFDM signals are compared. It can be observed that the sideband energy in GFDM is significantly reduced compared to that in OFDM, with a difference of about 15dB. This effect leads to reduced out-of-band (OOB) radiation, allowing multiple carriers to be orthogonally multiplexed, minimizing inter-carrier interference between adjacent carriers. Figure 3.1b shows the impact of block size on the spectrum of the GFDM signal without a cyclic prefix (CP), where we can observe that for two blocks, OOB radiation is less than for 32 blocks. This is a benefit for GFDM as its block size can vary. For OFDM, the block size is the largest.
3.2 Impact of cyclic prefix on the spectral efficiency of OFDM and GFDM signals
Considering the requirements for cyclic prefixes in both OFDM and GFDM, their spectral efficiency indicators are below 1, introducing additional overhead. Figure 3.2 displays the spectral efficiency metrics of the OFDM and GFDM signals. It can be observed that for both, the SEI decreases with increasing CP length, but this change is higher in OFDM than in GFDM, thus, GFDM has better spectral efficiency, consistent with point 3.1.
3.3 Bit Error Rate (BER) comparison of OFDM and GFDM signals
Figure 3.3 shows the BER performance of QAM 4 modulation format OFDM and GFDM signals. It can be observed that OFDM performs better in this case, as its BER curve closely approaches the ideal BER situation, while GFDM performs worst, showing a significant deviation from the ideal case. This is due to the complex process of generating the signals, making it more difficult to recover information through equalization.
3.4 Carrier Phase Comparison of OFDM and GFDM Signals at SNR = 10dB
Figure 3.4 confirms the challenges faced by the demodulator when performing hard decisions on GFDM symbols compared to OFDM symbols. It can be observed that more GFDM symbols appear closer to the decision boundary and may have already crossed it.
3.5 Complexity comparison between OFDM and GFDM generation and recovery
From the diagrams in Figures 2.1a, b and 2.3a, b, it is evident that the GFDM transmitter and receiver, respectively, include additional blocks with pulse-shaped filters and matched filters compared to the OFDM transmitter and receiver. Therefore, the GFDM system is more complex than the OFDM system. The main part of OFDM modulation is the IFFT block, which has a complexity of O(NlogN). GFDM demodulation involves complexities of O(N) for cyclic shifting, O(NlogN) for IFFT, and O(N2) for convolution with the filter.
3.6 User interface results
A GUI was constructed allowing users to input some parameters and simulate the results as shown below.
Conclusion This project designs and simulates the generation and recovery of OFDM and GFDM signals, comparing them from aspects such as signal spectrum, spectral efficiency, bit error rate, and constellation diagrams. The following table provides the comparative results; ticked off the best result for each comparison. Improving equalization methods can improve the bit error rate of GFDM. Otherwise, there is a trade-off between system complexity and performance. GFDM will be very useful in systems requiring higher spectral efficiency.
References 1) H.S. et al. "Machine-type Communication," IEEE Communications Magazine, pp.10-17, 2015
2) M.S. et al., "Comparative analysis of OFDM and GFDM," IJACTA, vol 4, no. 2, 2016.
3) G.F, M.K and S.B, "GFDM – Generalized Frequency Division Multiplexing," IEEE, 2009.
MATLAB Code
MATLAB Simulation Results

## Images

![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](01.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](02.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](03.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](04.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](05.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](06.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](07.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](08.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](09.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](10.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](11.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](12.jpg)
![Fractional Multiplexing in 5G: A comparison between OFDM and GFDM (spectral efficiency, bit error rate, constellation diagram, complexity) [with MATLAB code and report]](13.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
