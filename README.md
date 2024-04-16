### Acoustic Transmitter Design using the Goertzel Algorithm

This project aims to develop an acoustic transmitter that first identifies the frequency channels occupied by other transmitters and then emits an acoustic signal on one of the found free channels. The detection of a channel will be done using the Goertzel algorithm. The transmitter will scan the marine environment to determine occupied channels within a range of 500 meters. Subsequently, it will emit an acoustic pulse every second with a width of 10 ms and a frequency on a free channel.

#### Design Objectives:
- Identify occupied frequency channels using the Goertzel algorithm.
- Emit an acoustic pulse on a free channel every second.
- Utilize digital signal processing (DSP) techniques to modernize the transmitter.
- Improve cost, power consumption, and size compared to the original analog design.

#### Goertzel Algorithm Overview:
The Goertzel algorithm is chosen for its efficiency in detecting a few frequencies compared to other techniques like Fast Fourier Transform (FFT). It requires fewer resources and can be executed recursively. The algorithm involves calculating a few memories per frequency using the recursive formula:
```
Qn = Xn + Coeff(F) * Qn_1 – Qn_2
```
where:
- Xn is the sample of the input signal.
- Coeff(F) is a constant calculated based on the desired frequency.
- Qn, Qn_1, and Qn_2 are the memories for the current, previous, and two steps back iterations, respectively.

#### Implementation Details:
- Sampling frequency (Fe): 96 KHz
- Number of samples (N) for Goertzel algorithm: 192
- Calculation of Coeff(F) in fixed-point format (Q15):
  ```
  Coeff_Q15(F) = round(2^15 * Coeff(F))
  ```

#### Pseudocode for Goertzel Algorithm:
```plaintext
Initialize Qn_1(f) and Qn_2(f) to 0 for each frequency channel (f from 0 to 7)

For each sample (i from 0 to N-1):
    For each frequency channel (f from 0 to 7):
        Calculate Qn(f) using the Goertzel formula
        Update Qn_1(f) and Qn_2(f)
        
For each frequency channel (f from 0 to 7):
    Calculate Module(f) using Qn_1 and Qn_2
    Determine ModuleMax and ModuleMaxSuivant
    
If ModuleMax > ModuleMaxSuivant * CONTRASTE, then mark the channel as occupied

If not in the 5-second search period:
    If ModuleMax > ModuleMaxSuivant * CONTRASTE:
        Find the first free channel and exit the loop
```

#### Conclusion:
The implementation of the Goertzel algorithm allows for efficient detection of occupied frequency channels in the marine environment. By utilizing digital signal processing techniques, we aim to modernize the transmitter while improving its performance and reducing costs. The Goertzel algorithm provides a robust method for channel detection, paving the way for a more effective acoustic transmitter design.
