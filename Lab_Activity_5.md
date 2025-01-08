Laboratory Activity 5

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • find the FFT of a given sequence

II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: DFT of a sequence ![image](https://github.com/user-attachments/assets/27d2ba06-87c6-4b6b-81e9-83984ff4819a)


Where N= Length of sequence. K= Frequency Coefficient. n = Samples in time domain.

FFT: -Fast Fourier transform. There are two methods.

Decimation in time (DIT ) FFT.
Decimation in Frequency (DIF) FFT. Why we need FFT? The no of multiplications in DFT = N2. The no of Additions in DFT = N (N-1). For FFT. The no of multiplication = N/2 log 2N. The no of additions = N log2 N.
Algorithm: Step I : Give input sequence x[n]. Step II : Find the length of the input sequence using length command. Step III : Find FFT and IFFT using matlab commands fft and ifft. Step IV : Plot magnitude and phase response Step V : Display the results

Flow Chart: ![image](https://github.com/user-attachments/assets/339d5886-68ae-424c-ab3d-69624ef53f6e)


Output:

Enter the sequence: [1 2 3 4 5]

Output Waveform:

![image](https://github.com/user-attachments/assets/6b10ee5f-fc18-4411-96fe-4c1f7c4a958e)


VIVA QUESTIONS:

1. Define transform. What is the need for transform? 
A transform is like hitting the "rearrange" button on a complex set of data. It shifts your perspective, making it easier to analyze information and solve problems. This is crucial in many fields, as it can simplify complex calculations, reveal hidden patterns, and allow for more efficient data processing. Think of it as translating a book into a different language – the story remains the same, but it becomes accessible to a new audience.

2. Differentiate Fourier transform and discrete Fourier transform. 
The Fourier Transform and Discrete Fourier Transform both reveal the hidden frequencies in a signal, but the key difference lies in the type of signal they analyze: the Fourier Transform works with continuous signals like sound waves, providing a complete spectrum of frequencies, while the Discrete Fourier Transform deals with discrete signals like digital audio, giving a simplified frequency spectrum based on sampled points. It's like comparing a continuous rainbow to one made of distinct LEGO bricks – both show the colors, but in different ways.

3. Differentiate DFT and DTFT. 
Both the Discrete Fourier Transform (DFT) and Discrete-Time Fourier Transform (DTFT) deal with discrete signals, but the DFT analyzes a finite chunk of that signal, like a single verse in a song, while the DTFT analyzes the entire signal, as if considering the whole song at once. This means the DFT gives you a discrete set of frequencies, like individual notes, while the DTFT provides a continuous spectrum, like all the subtle tones and overtones blended together. Essentially, the DFT gives a snapshot of frequencies in a window of time, while the DTFT provides a complete frequency picture of the entire signal.

4. What are the advantages of FFT over DFT? 
	Speed
	Efficiency
	Reduced Complexity
	Lower Memory Usage
	Wide Applicability

5. Differentiate DITFFT and DIFFFT algorithms. 
Both DITFFT (Decimation-In-Time Fast Fourier Transform) and DIFFFT (Decimation-In-Frequency Fast Fourier Transform) are efficient algorithms for computing the Discrete Fourier Transform (DFT) of a sequence, significantly reducing the number of computations compared to a direct DFT calculation. The key difference lies in how they break down the problem. DITFFT recursively divides the input sequence in the time domain into smaller subsequences, computes their DFTs, and then combines the results to obtain the DFT of the original sequence. In contrast, DIFFFT recursively divides the output sequence in the frequency domain, calculating smaller DFTs and combining them to produce the final DFT. Both algorithms utilize the periodicity and symmetry properties of the twiddle factors to achieve computational efficiency, ultimately leading to the same result but with different intermediate steps.

6. What is meant by radix? 
Radix is like choosing the size of your "counting buckets." We humans usually count in buckets of ten (our decimal system), but computers use buckets of two (binary system, with 0s and 1s). It's like choosing between organizing apples in bags of ten or pairs. So, whether you're a human counting on your fingers or a computer crunching data, the radix is the fundamental building block of how you group and represent numbers

7. What is meant by twiddle factor and give its properties? 
In the Fast Fourier Transform (FFT), a twiddle factor is like a precise instruction for a dancer, telling them how much to turn and in which direction. These special numbers, which involve imaginary components, act as rotations, guiding the "dance" of data within the FFT algorithm. Their properties, like periodicity and symmetry, allow for efficient rearrangement and analysis of frequencies within a signal. Think of them as the choreographic cues that enable a complex dance routine, ensuring each dancer moves gracefully and precisely to create a harmonious pattern.

8. How FFT is useful to represent a signal? 
The Fast Fourier Transform (FFT) is like a prism for digital signals, breaking them down into their individual frequency components. Just as a prism reveals the hidden colors in white light, the FFT reveals the hidden frequencies in a signal, allowing us to see its "ingredients." This frequency representation is incredibly useful because it helps us understand the signal's underlying structure, identify important patterns, and even manipulate it for specific purposes like filtering out noise or compressing audio. Think of it as transforming a complex musical chord into its individual notes, making it easier to understand and appreciate the composition.

9. Compare FFT and DFT with respect to number of calculations required? 
The DFT (Discrete Fourier Transform) requires a significantly larger number of calculations compared to the FFT (Fast Fourier Transform). For a sequence of length N, the DFT involves roughly N² complex multiplications and additions, making it computationally expensive for large datasets. In contrast, the FFT, by cleverly exploiting symmetry and periodicity in the DFT calculation, reduces this number to approximately N*log₂(N) operations. This drastic reduction in computational complexity makes the FFT much faster and more efficient, especially for long data sequences commonly encountered in signal processing and other applications.

10. How the original signal is reconstructed from the FFT of a signal? 
The IFFT reconstructs the original signal from its FFT by combining the frequency components, like reversing a recipe.

Exercise: 
1. Find 8-point DFT of sequence x(n)=[1 2 1 2 3 4 4 3] using FFT algorithm.

We used the Fast Fourier Transform (FFT) to compute the 8-point Discrete Fourier Transform (DFT) for the sequence x(n)=[1,2,1,2,3,4,4,3]. Here's what we got:

Results: X[0]=20: This is the DC (zero-frequency) component, showing the average value of the sequence. X[1]=−2.71+5.12j: A complex number representing the contribution of the first frequency. Its magnitude and angle tell us the strength and phase. X[2]=−1−1j: Another frequency contribution, with both real and imaginary parts. X[3]=−1.29−0.88j: A weaker frequency contribution. X[4]=−2: A real value, meaning no phase shift. X[5]=−1.29+0.88j: Symmetric to X[3], as expected in FFT results. X[6]=−1+1j: Symmetric to X[2]. X[7]=−2.71−5.12j: Symmetric to X[1]. These values describe how much of each frequency is present in the original sequence and include both magnitude (strength) and phase (timing shift). For instance:

The large value X[0]=20 shows a strong constant (average) component. The symmetry across indices (e.g., X[7]) is a typical property of FFTs for real sequences. In simpler terms, this process tells us what "notes" (frequencies) make up our "music" (the sequence) and how loud or shifted they are.
