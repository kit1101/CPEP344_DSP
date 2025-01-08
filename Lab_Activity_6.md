Laboratory Activity 6

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • determine the Power Spectrum of a given signal. 

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: The power spectrum describes the distribution of signal power over a frequency spectrum. The most common way of generating a power spectrum is by using a discrete Fourier transform, but other techniques such as the maximum entropy method can also be used. The power spectrum can also be defined as the Fourier transform of auto correlation function. Algorithm:
Step I : Give input sequence x Step II : Give sampling frequency, input frequency and length of the spectrum. Step III: Find power spectrum of input sequence using MATLAB command spectrum. Step IV: Plot power spectrum using spec plot.

Flow Chart: ![image](https://github.com/user-attachments/assets/bf08228d-5167-4dd4-a65c-0865ae4be508)


INPUT: Enter the frequency [1 to 5000]: 3000

Output Waveform:

![image](https://github.com/user-attachments/assets/cdd03667-efa6-47f2-8f0a-1c4e8446a2b1)


VIVA QUESTIONS:

1. Define power signal.  
A power signal is a signal with a power of finite or non-zero.

2. Define energy signal.  
It is a measure of total energy contained in a signal.

3. Define power spectral density of a signal.  
PSD or Power Spectral Density is a measure of how a power of a signal is distributed across a range of frequencies.

4. How the energy of a signal can be calculated?  
	Squaring the signal’s amplitude at each point in time
	Summing or integrating these squared values over the entire duration

5. Explain difference between energy spectral density and power spectral density. 
Energy spectral density (ESD) describes how the total energy of a signal is distributed across different frequencies, typically used for finite-energy signals like pulses. Power spectral density (PSD), on the other hand, describes the power distribution across frequencies for signals with finite power but infinite energy, like continuous signals. Essentially, ESD is used for signals that exist for a limited time, while PSD is used for ongoing signals.

6. Explain the PSD plot. 
A PSD plot is a visual representation of how the power of a signal is distributed across different frequencies. Imagine it as a graph where the horizontal axis (x-axis) shows the frequency, and the vertical axis (y-axis) shows the corresponding power density. Peaks in the plot indicate the dominant frequencies where the signal has the most power, like the loudest notes in a song or the strongest vibrations in a machine. The overall shape of the plot gives you a sense of the signal's character – a flat PSD indicates white noise with equal power across all frequencies, while concentrated peaks suggest strong periodic components like a pure tone. Essentially, a PSD plot provides a "frequency fingerprint" of a signal, revealing its hidden structure and allowing for analysis, filtering, and system design.

7. What is the importance of PSD?  
It is to analyze the frequency content of signals, which helps guide the design of relevant filters. It also allows scientists and engineers to characterize broadband, random signals.

8. What are the applications of PSD? 
	Analyzing vibrations
	Processing audio signals
	Characterizing noise
	Designing communication systems
	Studying brain waves

9. Explain MATLAB function randn(size(n)).  
The MATLAB function randn(size(n)) is a handy tool for generating arrays of random numbers. Imagine you're conducting a simulation where you need a set of random data points, or perhaps you're working on a statistical analysis that requires random inputs. This function allows you to create those random numbers easily.
Here's how it works: randn is the core of the function, responsible for generating random numbers from a standard normal distribution. This distribution, also known as a Gaussian distribution, is a bell-shaped curve where the numbers tend to cluster around zero. The size(n) part ensures that the generated random numbers are organized into an array that matches the dimensions of an existing array, n. This is useful because it allows you to easily integrate these random numbers into your existing code and workflows.
For instance, if n is a 3x2 matrix, meaning it has 3 rows and 2 columns, randn(size(n)) will produce another 3x2 matrix, but this new matrix will be filled with random numbers drawn from the standard normal distribution. This function is a common sight in various fields like signal processing, image analysis, and machine learning, where random data is often needed for tasks like testing algorithms, simulating real-world scenarios, and initializing models.


10. What is the need to represent the signal in frequency domain? 
Analyzing signals in the frequency domain reveals their underlying structure by decomposing them into their constituent frequencies. This perspective is essential for tasks like designing filters to remove unwanted noise, understanding how different systems modify signals, and extracting meaningful information from complex signals like speech or music.
 


Exercise: 
1. Find power spectrum of the signal x(n)=cos(2*pi*50*n)

The signal is: x(n)=cos(2π⋅50⋅n) This is a cosine wave that repeats over time. The key number here is 50, which tells us the frequency of the signal.
The power spectrum shows how the power of the signal is spread across different frequencies. For a simple cosine wave like this, all the power is concentrated at two specific frequencies; The positive and negative versions of the frequency.

For x(n)=cos(2π⋅50⋅n), the power is split between:

+50 Hz (positive frequency) -50 Hz (negative frequency) Imagine it like this: If you shine white light through a prism, the light splits into multiple colors (frequencies). But for a cosine wave, it's like a prism that only shows two colors at +50 and -50 Hz.

For a signal like a cosine wave, the power spectrum is always a pair of spikes at δ(f+50) part means there is a spike of power at -50 Hz. The 1/2 means the total power is split equally between the two frequencies (like two people sharing one pizza equally).

The power spectrum tells us which frequencies are in the signal. In this case, it’s telling us that the only important frequencies are -50 Hz and +50 Hz. This kind of analysis is essential in areas like communication systems, music production, and signal filtering, where we need to know which frequencies are present and how strong they are.
