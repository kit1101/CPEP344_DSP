Laboratory Activity 9

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • implement LP IIR filter for a given sequence. 

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: IIR filters are digital filters with infinite impulse response. Unlike FIR filters, they have the feedback (a recursive part of a filter) and are known as recursive digital filters therefore. For this reason, IIR filters have much better frequency response than FIR filters of the same order. Unlike FIR filters, their phase characteristic is not linear which can cause a problem to the systems which need phase linearity. For this reason, it is not preferable to use IIR filters in digital signal processing when the phase is of the essence. Otherwise, when the linear phase characteristic is not important, the use of IIR filters is an excellent solution. There is one problem known as a potential instability that is typical of IIR filters only. FIR filters do not have such a problem as they do not have the feedback. For this reason, it is always necessary to check after the design process whether the resulting IIR filter is stable or not.

IIR FILTER DESIGN For the given specifications to Design a digital IIR filter, first we need to design analog filter (Butterworth or chebyshev). The resultant analog filter is transformed to digital filter by using either “Bilinear transformation or Impulse Invariant transformation”. Algorithm: Step I : Enter the pass band ripple (rp) and stop band ripple (rs) . Step II : Enter the pass band frequency (wp) and stop band frequency (ws).

Step III : Get the sampling frequency (fs).

Step IV : Calculate normalized pass band frequency, and normalized stop band frequency w1 and w2 respectively. w1 = 2 * wp /fs w2 = 2 * ws /fs Step V : Make use of the following function to calculate order of filter Butterworth filter order [n,wn]=buttord(w1,w2,rp,rs ) Chebyshev filter order [n,wn]=cheb1ord(w1,w2,rp,rs)

Step VI: Design an nth order digital low pass Butterworth or Chebyshev filter using the following statements.

Butterworth filter [b, a]=butter (n, wn)

Chebyshev filter [b,a]=cheby1 (n, 0.5, wn)

Step VII : Find the digital frequency response of the filter by using ‘freqz( )’ function

Step VIII : Calculate the magnitude of the frequency response in decibels (dB) mag=20*log10 (abs (H))

Step IX : Plot the magnitude response [magnitude in dB Vs normalized frequency]

Step X : Calculate the phase response using angle (H)

Step XI : Plot the phase response [phase in radians Vs normalized frequency (Hz)].

Flow Chart:

![image](https://github.com/user-attachments/assets/0378323b-5e71-4d86-81dd-38c6c8602951)


Expected waveforms: enter the IIR filter design specifications enter the passband ripple:15 enter the stopband ripple:60 enter the passband freq:1500 enter the stopband freq:3000 enter the sampling freq:7000

Output Waveform: ![image](https://github.com/user-attachments/assets/5f440533-1dd5-440f-9b75-8a23cf3c2332)


VIVA QUESTIONS:

1. List some advantages of digital filters over analog filters.
	Flexibility
	Consistency
	Precision
	Reproducibility

2. Write some differences between FIR and IIR filters.
FIR filters are like short-term memory, using only current and past input values, while IIR filters have long-term memory, using both past inputs and outputs. This makes FIR filters inherently stable and easier to design, while IIR filters can be more efficient but require careful design to avoid instability.

3. What are the different methods to design IIR filters?
IIR filters can be designed by starting with an analog filter and converting it to a digital form using techniques like bilinear transformation or impulse invariance. Alternatively, they can be designed directly in the digital domain using methods like optimization algorithms or pole-zero placement. These methods offer different trade-offs in terms of accuracy, complexity, and control over the filter's characteristics.

4. Why IIR filters are not reliable?
IIR filters can be designed by starting with an analog filter and converting it to a digital form using techniques like bilinear transformation or impulse invariance. Alternatively, they can be designed directly in the digital domain using methods like optimization algorithms or pole-zero placement. These methods offer different trade-offs in terms of accuracy, complexity, and control over the filter's characteristics.

5. What are different applications of IIR filters?
IIR filters are used in a wide range of applications, including audio processing (like equalizers and sound effects), telecommunications (for signal filtering and noise reduction), and biomedical signal processing (for tasks like ECG and EEG analysis). Their efficiency and ability to mimic analog filter designs make them valuable tools in various fields.

6. What are advantages of IIR filters?
	Efficiency
	Low Memory
	Analog Similarity

7. What are disadvantages of IIR filters?
	Potential Instability
	Nonlinear Phase Response
	Sensitivity to Quantization

8. Differentiate Butterworth and Chebyshev approximations.
Butterworth filters prioritize a flat frequency response in the passband, like a smooth, level road, but have a gradual transition to the stopband. Chebyshev filters, on the other hand, have a steeper, sharper transition like a sudden cliff, but allow for ripples in the passband, like bumps in the road.

9. What is meant by impulse response?
The impulse response is like the "fingerprint" of a system, showing how it reacts to a sudden, brief input, revealing its unique characteristics.

10. Difference between IIR low pass and High pass filters.
IIR low-pass filters allow low-frequency signals to pass through while attenuating high-frequency signals, essentially acting as a treble cut. Conversely, IIR high-pass filters allow high-frequency signals to pass through while attenuating low-frequency signals, acting as a bass cut. This difference in frequency response is achieved through the use of feedback in their design, where past output values are used to influence the current output.

Exercise:
1. Design low pass IIR filter using Chebyshev filter.

Steps to Design:
Specifications: Determine the passband cutoff frequency (𝑓𝑝) and stopband frequency (𝑓𝑠). Specify passband ripple (𝐴𝑝) and stopband attenuation (𝐴𝑠).
Choose the Filter Type: Chebyshev Type I: Ripple in the passband. Chebyshev Type II: Ripple in the stopband.
Calculate Filter Order (𝑁): Use the formula: ![image](https://github.com/user-attachments/assets/ca166c70-43fc-4797-a093-10109f6e6843)

Determine Poles and Coefficients: Use Chebyshev polynomial equations to compute poles and filter coefficients.
Transform to Digital Domain: Use bilinear transformation to convert the analog design to a digital design.
Implementation: Use the derived filter coefficients to filter the input signal.
