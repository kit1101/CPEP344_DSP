Laboratory 2

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • obtain Linear Convolution of two finite length sequences

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: Convolution is a mathematical operation used to express the relation between input and output of an LTI system. It relates input, output and impulse response of an LTI system as

y(n)=x(n)∗h(n)

Where y (n) = output of LTI

x (n) = input of LTI

h (n) = impulse response of LTI

Discrete Convolution

y(n)=x(n)∗h(n)

![image](https://github.com/user-attachments/assets/56a471ab-eefd-49a3-8b15-642d63a303e3)


By using convolution we can find zero state response of the system.

Algorithm: Step I: Give input sequence x[n]. Step II: Give impulse response sequence h(n) Step III: Find the convolution y[n] using the matlab command conv. Step IV: Plot x[n],h[n],y[n]

![image](https://github.com/user-attachments/assets/ec62d008-44cb-4cd2-a087-86c86b544045)


Output: Enter the first sequence x1(n) = [1 2 3 4 5] Enter the second sequence x2(n) = [5 8 3 5 4 6] The values of yn are=

5 18 34 55 80 81 59 59 44 30

OUTPUT WAVEFORMS:

![image](https://github.com/user-attachments/assets/079c1c9d-4dc8-4a41-9736-2d1e6ae47cf0)


RESULT:

VIVA QUESTIONS: 
1.	Explain the significance of convolution.
Convolution in Digital Signal Processing is a fundamental operation that mathematically combines two signals to produce a third. It essentially describes how a system (represented by a filter) modifies an input signal to generate an output. This process is crucial for various signal processing tasks, including filtering (smoothing, sharpening, noise reduction), feature extraction, and system analysis, enabling precise manipulation and understanding of signals across diverse applications.
 
2.	Define linear convolution. 
Linear convolution is a fundamental mathematical operation in Digital Signal Processing that combines two signals to produce a third. It involves flipping one signal, shifting it across the other, multiplying corresponding points, and summing the products at each shift. This process accurately models how a linear time-invariant (LTI) system responds to an input signal, making it crucial for tasks like filtering, system analysis, and understanding the interaction between signals.

3.	Why linear convolution is called as a periodic convolution? 
Linear convolution is the standard operation for combining two signals, accurately modeling how a linear time-invariant system responds to an input. It involves flipping one signal, shifting it across the other, and summing the products at each shift. Circular convolution, on the other hand, treats signals as periodic, wrapping around their ends, which can lead to different results compared to linear convolution, especially for finite-length signals.

4.	Why zero padding is used in linear convolution? 
Zero-padding is essential when using the Fast Fourier Transform (FFT) to efficiently compute linear convolution. Since the FFT inherently performs circular convolution, zero-padding the input signals before the FFT effectively extends their perceived length, preventing undesired wraparound effects and ensuring that the circular convolution accurately approximates the desired linear convolution.

5.	What are the four steps to find linear convolution?
Linear convolution involves reversing one sequence, shifting it across the other, multiplying corresponding elements at each shift, and summing these products to obtain the output at that shift position. This process is repeated for all possible shifts to determine the complete output sequence.

6.	What is the length of the resultant sequence in linear convolution?
The length of the resultant sequence in linear convolution of two finite-length sequences is equal to the sum of the lengths of the individual sequences minus one.

7.	How linear convolution will be used in calculation of LTI system response? 
Linear convolution directly calculates the output of an LTI system given its impulse response (the system's response to a brief input) and any arbitrary input signal. This is achieved by convolving the input signal with the impulse response of the system. This fundamental relationship allows for precise prediction and analysis of how an LTI system will behave for any given input, making it a cornerstone of LTI system analysis and design.

8.	List few applications of linear convolution in LTI system design.
Linear convolution is fundamental in LTI system design, enabling tasks like designing filters for signal processing (e.g., noise reduction, audio equalization), analyzing system behavior to predict output for given inputs, and implementing image processing techniques such as blurring and sharpening. It provides a powerful framework for understanding and manipulating signals within the context of LTI systems across various engineering and scientific domains.

9.	Give the properties of linear convolution. 
Linear convolution exhibits key properties: it's commutative (order of signals doesn't matter), associative (order of multiple convolutions is irrelevant), and distributive over addition. These properties simplify system analysis and design in signal processing.

10.	How the linear convolution will be used to calculate the DFT of a signal? 
The DFT allows efficient computation of linear convolution by leveraging the convolution theorem: multiplication in the frequency domain corresponds to linear convolution in the time domain. To avoid circular convolution, signals are zero-padded before computing their DFTs. The product of the DFTs is then obtained and its inverse DFT yields the linear convolution of the original signals.
