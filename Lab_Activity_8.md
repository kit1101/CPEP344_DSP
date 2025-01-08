Laboratory Activity 8

Name : KEITH O'MYRAH M. ALABAT 

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • implement HP FIR filter for a given sequence. 

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

Algorithm: Step I : Enter the pass band frequency (fp) and stop band frequency (fq). Step II : Get the sampling frequency (fs), length of window (n). Step III : Calculate cut off frequency Step IV : Use boxcar, hamming, Blackman Commands to design window. Step V : Design filter by using above parameters. Step VI : Find frequency response of the filter using matlab command freqz. Step VII : Plot the magnitude response and phase response of the filter.

Flow Chart: ![image](https://github.com/user-attachments/assets/b9c39df5-39a5-4925-b0d4-6399e7b13e9a)


Output Waveforms:

![image](https://github.com/user-attachments/assets/02d4143e-918b-4efa-b026-9688307921be)

VIVA QUESTIONS: 
1. What is a filter?
It is a system that selectively modifies the characteristics of a signal.


2. Differentiate analog filter and digital filter.
Analog filters process continuous-time signals using physical components like resistors, capacitors, and inductors, making them suitable for directly dealing with real-world signals. Digital filters, on the other hand, process discrete-time signals using mathematical algorithms implemented on computers or digital signal processors, making them flexible and adaptable for various applications.

3. Define FIR filter.
A Finite Impulse Response (FIR) filter is a type of digital filter that has a response to an input signal that lasts for a finite amount of time. This means that after a certain number of samples, the filter's output will become zero, unlike Infinite Impulse Response (IIR) filters which can have internal feedback and continue to respond indefinitely.

4. What are the differences between recursive and non-recursive systems?
Recursive systems use previous outputs in their calculations, creating feedback, while non-recursive systems only depend on current and past inputs. This means recursive systems have an infinite impulse response, while non-recursive systems have a finite impulse response.

5. List a few Applications of FIR filters.
	Audio processing
	Telecommunications
	Digital Signal Processing
	Image Processing
	Biomedical Signal Processing

6. Explain advantages of FIR filters over IIR filters.
FIR filters offer linear phase response, ensuring all frequencies are delayed equally, thus avoiding phase distortion. They are inherently stable due to their non-recursive nature, unlike IIR filters which can become unstable due to feedback.

7. Explain limitations of FIR filters.
FIR filters generally require a higher order (more coefficients) than IIR filters to achieve a similar filtering effect, leading to increased computational complexity and potential latency. This can be a significant drawback in resource-constrained environments or real-time applications.

8. What are the different methods to design FIR filters?
	Frequency sampling method
	Window method
	Optimal filter design methods

9. Explain different window functions.
Window functions are mathematical functions applied to the ideal impulse response of a filter to reduce unwanted ripples in the frequency response caused by truncation. Different window functions, like Hamming, Hanning, and Blackman, offer trade-offs between main lobe width (affecting transition sharpness) and side lobe attenuation (affecting stopband rejection). The choice of window function depends on the specific filter requirements.

10. Differentiate rectangular, triangular and Kaiser Windows.
The rectangular window simply truncates the ideal impulse response, leading to sharp transitions but significant ripples in the frequency response. The triangular window provides a smoother transition and lower side lobes compared to the rectangular window, but with a wider main lobe. The Kaiser window offers flexible control over the trade-off between main lobe width and side lobe attenuation through a parameter (β), allowing for customized filter design with improved performance compared to the fixed shapes of rectangular and triangular windows.

Exercise:
1. Design HP FIR filter using Rectangular and hamming Window.

Design HP FIR filter using Rectangular and hamming Window
Steps to Design: Specifications:
Determine the desired cutoff frequency (𝑓𝑐). Select sampling frequency (𝑓𝑠).

Calculate Filter Order (N): Use the formula 𝑁=𝑓𝑠/𝑓𝑐−1, adjusting as needed based on transition width.

Generate the Ideal Impulse Response (hd[n]): For a high-pass filter, derive the impulse response using the equation: ![image](https://github.com/user-attachments/assets/c779ae65-19e8-405f-8779-d1215e1abc0a)


Apply Window Function: Multiply ℎ𝑑[𝑛] by the chosen window function (𝑤[𝑛]to get the FIR coefficients: ![image](https://github.com/user-attachments/assets/9e733507-2823-4f4c-844e-109e5242f8ba)


Implementation: Convolve the input signal with ℎ[𝑛].
