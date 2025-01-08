Laboratory Activity 7

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • implement LP FIR filter for a given sequence. 

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: FIR filters are digital filters with finite impulse response. They are also known as non-recursive digital filters as they do not have the feedback. An FIR filter has two important advantages over an IIR design: Firstly, there is no feedback loop in the structure of an FIR filter. Due to not having a feedback loop, an FIR filter is inherently stable. Meanwhile, for an IIR filter, we need to check the stability. ∙ Secondly, an FIR filter can provide a linear-phase response. As a matter of fact, a linear-phase response is the main advantage of an FIR filter over an IIR design otherwise, for the same filtering specifications; an IIR filter will lead to a lower order. FIR FILTER DESIGN An FIR filter is designed by finding the coefficients and filter order that meet certain specifications, which can be in the time-domain (e.g., a matched filter) and/or the frequency domain (most common). Matched filters perform a cross-correlation between the input signal and a known pulse-shape. The FIR convolution is a cross-correlation between theinput signal and a time-reversed copy of the impulse-response. Therefore, the matched-filter's impulse response is "designed" by sampling the known pulse-shape and using those samples in reverse order as the coefficients of the filter. When a particular frequency response is desired, several different design methods are common:

1. Window design method
2. Frequency Sampling method
3. Weighted least squares design WINDOW DESIGN METHOD In the window design method, one first designs an ideal IIR filter and then truncates the infinite impulse response by multiplying it with a finite length window function. The result is a finite impulse response filter whose frequency response is modified from that of the IIR filter. ![image](https://github.com/user-attachments/assets/8ba67fd6-0e6b-40c7-b9cb-92f01eff2a3e)

Algorithm: Step I : Enter the pass band frequency (fp) and stop band frequency (fq). Step II : Get the sampling frequency (fs), length of window (n). Step III : Calculate the cut off frequency, fn Step IV : Use boxcar, hamming, blackman Commands to design window. Step V : Design filter by using above parameters. Step VI : Find frequency response of the filter using matlab command freqz. Step VII : Plot the magnitude response and phase response of the filter.

Flow Chart: ![image](https://github.com/user-attachments/assets/9621912e-a9c5-4f06-92d6-2c356cc1f6ae)


Expected Wave forms: ![image](https://github.com/user-attachments/assets/0576b406-9b29-4e96-b9cb-683167c6e803)


VIVA QUESTIONS:

1. Define filter.
It is a system that selectively modifies the characteristics of a signal.

2. What are the different types of filters?
	Low-pass filter
	High-pass filter
	Band-pass filter
	Band-stop filter
	All-pass filter
	Analog filter
	Digital filter
	Finite and infinite impulse response filters
	Butterworth, Chebyshev, Bessel, Elliptic filters
	And many more.

3. Why are FIR filters generally preferred over IIR filters in multirate (decimating 
and interpolating) systems
FIR filters are favored in multirate systems due to their linear phase response, which prevents distortion when changing sampling rates. Additionally, their inherent stability ensures reliable performance even with fluctuating input signals.

4. Difference between IIR and FIR filters?
IIR filters use feedback, incorporating past output values in their calculations, while FIR filters rely only on current and past input values. This makes IIR filters potentially unstable but computationally efficient, while FIR filters are inherently stable but may require more processing power. The key distinction lies in their impulse response: IIR filters have an infinite impulse response, while FIR filters have a finite one.

5. Differentiate ideal filter and practical filter responses.
Ideal filters have perfectly sharp cutoffs between passbands and stopbands, instantly transitioning from allowing signals to completely blocking them. In contrast, practical filters have a gradual transition zone, called the roll-off, where the signal attenuation increases gradually with frequency. This is due to real-world limitations in components and circuit design, preventing the instantaneous changes of ideal filters.

6. What is the filter specifications required to design the analog filters?
To design an analog filter, you must define the desired frequency response, including cutoff frequencies, allowed ripple, and roll-off. These specifications guide the selection of filter type, order, and component values to achieve the desired filtering characteristics.

7. What is meant by frequency response of filter?
The frequency response of a filter describes how it affects the different frequencies within a signal. It essentially shows how much of each frequency is allowed to pass through the filter and how much is attenuated, giving you a visual representation of the filter's behavior across the frequency spectrum.

8. What is meant by magnitude response?
Magnitude response refers to how the amplitude or strength of a signal is altered across different frequencies after passing through a system, such as a filter. It essentially shows how much each frequency component is amplified or attenuated by the system.

9. What is meant by phase response?
Phase response describes how the phase of different frequency components in a signal is shifted as it passes through a system, like a filter. It indicates how much each frequency is delayed or advanced in time relative to other frequencies.

10. Difference between FIR low pass filter and high pass filter.
Both FIR low-pass and high-pass filters are designed using a finite number of past input values, ensuring stability. However, they differ in which frequencies they allow to pass through. A low-pass FIR filter acts like a "treble cut," attenuating high frequencies while allowing low frequencies to pass, making it useful for smoothing signals and removing noise. Conversely, a high-pass FIR filter acts like a "bass cut," attenuating low frequencies while allowing high frequencies to pass, making it useful for edge detection or isolating high-pitched sounds. Essentially, they are mirror images of each other in terms of frequency response.

Exercise:
1. Design LP FIR filter using Bartlett and hamming window.

Design LP FIR filter using Bartlett and hamming window.
FIR filters are preferred over IIR filters in multirate systems because they have linear phase, are always stable, and have better control of delay. Filter design requires key parameters like cutoff frequency, passband ripple, and stopband attenuation. Bartlett windows give wider transition bands but simpler design, while Hamming windows provide better attenuation of side-lobes. Filters can be designed and visualized using software like MATLAB or Python (via libraries like scipy.signal).
Sampling frequency (𝑓𝑠​) = 1000 Hz Cutoff frequency (𝑓𝑐) = 200 Hz Filter order (N) = 50

Output: ![image](https://github.com/user-attachments/assets/8d889526-585a-4c10-9329-4e145b8e6dba)
