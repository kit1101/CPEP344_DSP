Laboratory Activity 1

Name: KEITH O'MYRAH M. ALABAT

Course and Year: BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • find Discrete Fourier Transform and Inverse Discrete Fourier Transform of given digital signal..

II. MATERIALS:

• Software: MATLAB

III. PROCEDURE:

THEORY: Basic equation to find the DFT of a sequence is given below.

![image](https://github.com/user-attachments/assets/dea94523-8d4d-41f5-a89c-99637e602025)


Basic equation to find the IDFT of a sequence is given below.

![image](https://github.com/user-attachments/assets/476753db-6477-4118-a40a-25c423668971)


Algorithm: Step I: Get the input sequence. Step II: Find the DFT of the input sequence using direct equation of DFT. Step III: Find the IDFT using the direct equation. Step IV: Plot DFT and IDFT of the given sequence using matlab command stem. Step V: Display the above outputs.

Flow chart:

![image](https://github.com/user-attachments/assets/b850e401-c526-440c-aaef-2eb4cf80cd03)


Output Waveforms:

![image](https://github.com/user-attachments/assets/c06cc87a-ad8c-48e5-899c-1c23419011d8)


RESULT:
VIVA QUESTIONS: 
1.	Define signal, Give Examples for 1-D, 2-D, 3-D signals. 
A signal is a way of conveying information.
A 1-Dimensional signal is a signal that depends only on one variable. An example of it is sound wave.
A 2-Dimensioanl signal is a signal that depends on two variables. An example of it is 
A 3-Dimensional signal is a signal that contains information that varies across three spatial dimensions, like a video game character, an MRI scan, or any object in the real world.

2.	Define transform. What is the need for transform? 
Transform means the process of changing the representation of the signal from one form to another using mathematical transformations. The need for transform is most of the signals or images are time domain signal (ie) signals that can be measured with time.

3.	Differentiate Fourier transform and discrete Fourier transform. 
The Fourier Transform analyzes continuous signals, like sound waves, while the Discrete Fourier Transform analyzes discrete signals, like digital audio recordings. Essentially, one deals with smooth curves and the other with a series of individual points.

4.	Differentiate DFT and DTFT.
DFT (Discrete Fourier Transform) is the transform that deals with a finite discrete-time signal and a finite or discrete number of frequencies while DTFT (Discrete Time Fourier Transform) is for signals which are aperiodic and discrete in time domain.

5.	Explain mathematical formula for calculation of DFT.
The Discrete Fourier Transform (DFT) is a mathematical technique that decomposes a signal, such as a sound wave or an image, into its constituent frequencies. Essentially, it reveals the underlying "musical notes" that combine to create the overall signal. By multiplying the signal with a series of complex numbers at different frequencies and summing the results, the DFT identifies the strength of each frequency component within the original signal. This process is analogous to finding the individual colors that compose a painting, allowing for deeper analysis and manipulation of the signal. 

6.	Explain mathematical formula for calculation of IDFT. 
The Inverse Discrete Fourier Transform (IDFT) reconstructs the original signal from its frequency components obtained through the DFT. Essentially, it "reverses" the process of breaking down the signal. The IDFT formula involves multiplying each frequency component by a complex number that depends on its frequency and the specific point in time, then summing these products and dividing by the total number of samples. This allows us to recover the original signal, which is crucial for various applications such as signal reconstruction, filter design, and communication systems.

7.	How to calculate FT for 1-D signal? 
The Fourier Transform is a mathematical tool that dissects a signal, such as a sound wave or an image, into its individual frequency components. It essentially translates the signal from the time domain, where it's represented as a function of time, to the frequency domain, where it's represented as a function of frequency. This transformation provides valuable insights into the signal's underlying structure, enabling applications like signal processing, image analysis, and the design of communication systems.

8.	What is meant by magnitude plot, phase plot, power spectrum? 
The magnitude plot, phase plot, and power spectrum are essential visualizations that reveal a signal's frequency characteristics. The magnitude plot illustrates the strength of each frequency component, while the phase plot indicates the time shift associated with each. The power spectrum, derived from the squared magnitude, depicts the distribution of power across different frequencies. These plots are fundamental for analyzing signals, designing filters, and understanding the behavior of various systems.

9.	Explain the applications of DFT. 
The Discrete Fourier Transform (DFT) serves as a foundational tool within digital signal processing. Its primary function is to decompose a discrete-time signal into its constituent frequency components, effectively transforming the signal's representation from the time domain to the frequency domain. This transformation enables a wide range of applications, including spectral analysis, filter design, and the efficient implementation of convolution operations.

10.	What are separable transforms? 
Separable transforms in Digital Signal Processing are mathematical operations that decompose multidimensional signals (like images or videos) into a series of one-dimensional operations. This decomposition significantly reduces computational complexity by allowing for faster processing and requiring less memory compared to non-separable methods. Examples include the Discrete Fourier Transform (DFT), Discrete Cosine Transform (DCT), and certain wavelet transforms, which are crucial for applications such as image compression, filtering, and analysis in various fields like medical imaging and seismic data processing.

Exercise:

1. Find 8-point DFT of the sequence x (n) = [1 2 3 4 4 3 2 1]
To find the 8-point Discrete Fourier Transform (DFT) of the sequence x(n) = [1 2 3 4 4 3 2 1], you can use the DFT formula or MATLAB's built-in fft function. The DFT formula is: X(k) = ∑ n=0 N−1 x(n)e −j N 2πkn where N = 8, x(n) is the time-domain sequence, and X(k) is the frequency-domain sequence. You'll calculate the DFT for each k (from 0 to N-1) to obtain the 8-point DFT of the given sequence.
