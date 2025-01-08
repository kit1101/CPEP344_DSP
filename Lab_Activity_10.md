Laboratory Activity 10

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

IV. OBJECTIVES:

In this laboratory exercise, the students are expected to: • implement HP IIR filter for a given sequence. 

V. MATERIALS:

• Software: MATLAB

VI. PROCEDURES:

Algorithm: Step I : Enter the pass band ripple (rp) and stop band ripple (rs). Step II : the pass band frequency (wp) and stop band frequency (ws). Step III : Get the sampling frequency (fs). Step IV : Calculate normalized pass band frequency, and normalized stop band frequency w1 and w2 respectively. w1 = 2 * wp /fs w2 = 2 * ws /fs

Step V : Make use of the following function to calculate order of filter Butterworth filter order [n,wn]=buttord(w1,w2,rp,rs ) Chebyshev filter order [n,wn]=cheb1ord(w1,w2,rp,rs)

Step VI : Design an nth order digital high pass Butterworth or Chebyshev filter using the following statement. Butterworth filter [b,a]=butter (n, wn,’high’) Chebyshev filter [b,a]=cheby1 (n, 0.5, wn,'high')

Step VII : Find the digital frequency response of the filter by using ‘freqz( )’ function

Step VIII : Calculate the magnitude of the frequency response in decibels (dB) mag=20*log10 (abs (H))

Step IX : Plot the magnitude response [magnitude in dB Vs normalized frequency]

Step X : Calculate the phase response using angle (H)

Step XI : Plot the phase response [phase in radians Vs normalized frequency (Hz)].

Flowchart: ![image](https://github.com/user-attachments/assets/64b57f7d-07c5-4654-8250-1b79b02b2504)


INPUT: enter the IIR filter design specifications enter the passband ripple15 enter the stopband ripple60 enter the passband freq1500 enter the stopband freq3000 enter the sampling freq7000

Expected Waveforms: ![image](https://github.com/user-attachments/assets/11778fb0-d992-42c2-9225-e39c1d78d9cd)

VIVA QUESTIONS:

1. What are the filter specifications required to design the analog filters?
To design an analog filter, you need to specify the cutoff frequency (where it transitions between passing and blocking), the filter order (how sharply it separates frequencies), and the acceptable ripple (how much variation is allowed in the passband). These specs guide the design to meet your filtering needs.

2. What is meant by frequency response of filter?
Imagine a filter like a sound equalizer. The frequency response is basically a graph showing how much the filter boosts or cuts each frequency, from low to high. It's like a visual guide to how the filter shapes the sound, showing which frequencies get through and which are blocked or reduced.

3. What is meant by magnitude response?
Magnitude response basically tells you how much a system, like your headphones, boosts or cuts different frequencies in a sound. It's like a volume knob for each individual frequency, from the low bass to the high treble.

4. What is meant by phase response?
Phase response measures how much different frequencies in a sound are delayed or advanced in time relative to each other. Think of it as making sure all the different parts of a sound wave are "lined up" correctly.

5. Differentiate ideal filter and practical filter responses.
Think of ideal filters as perfect bouncers with strict rules, letting in only the right frequencies and completely blocking the rest. Practical filters are like real-world bouncers, with some flexibility and imperfections in who they allow through.

6. What are the different types of analog filter approximations?
Analog filter approximations are different ways to design filters, each with tradeoffs. Butterworth is smooth, Chebyshev is sharp but with ripples, and Bessel prioritizes accurate timing of frequencies.

7. Define order of the filter and explain important role it plays in designing of a filter.
The order of a filter determines how steep its cutoff is, like choosing between a gentle slope or a steep cliff. A higher order means a sharper transition between the frequencies it passes and those it blocks, but it also makes the filter more complex. Choosing the right order is about balancing how precisely you need to filter with the complexity of the design.

8. Explain advantages and disadvantages of Butterworth filter.
Butterworth filters are like the "easygoing" option: they have a maximally flat response in the passband, meaning they don't distort the desired frequencies. However, their transition between passband and stopband is more gradual, so they might not be the best choice when you need a really sharp cutoff.

9. Explain advantages and disadvantages of Chebyshev filter.
Chebyshev filters are like the "athletic" option: they have a steeper cutoff, meaning they block unwanted frequencies more quickly, but they have ripples in the passband, so they might slightly distort the desired frequencies. It's a trade-off between sharpness and smoothness.

10. Why Chebyshev is better than Butterworth filter?
Chebyshev filters are better than Butterworth when you need a sharper cutoff between desired and unwanted frequencies, like needing to block a specific noise quickly, but they can introduce small ripples in the desired frequencies.

Exercise:
1. Design High pass IIR filter using Chebyshev filter.

Design Process:

Specifications: Sampling frequency (𝑓𝑠): Example: 1000Hz. Passband frequency (𝑓𝑝 ): Example: 200Hz. Stopband frequency (𝑓𝑠): Example: 300Hz. Passband ripple (𝐴𝑝): Example: 1dB. Stopband attenuation (𝐴𝑠): Example: 40dB.

Calculate the filter order (𝑁): Use the formula for Chebyshev filter design: ![image](https://github.com/user-attachments/assets/1864b5a4-3fbc-49d9-846c-6ef53ba987d4)


Determine poles and coefficients: Use Chebyshev polynomial expressions to compute poles and gain.

Transform to Digital Filter: Apply bilinear transformation to convert the analog design to digital.

Implementation: Use software tools like MATLAB, Python, or Octave. Functions such as scipy.signal.cheby1 (Python) or butter (MATLAB) can simplify the process.

