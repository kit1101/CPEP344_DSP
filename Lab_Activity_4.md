Laboratory Activity 4

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • find frequency response of a given system in differential equation form. II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY: Systems respond differently to inputs of different frequencies. Some systems may amplify components of certain frequencies, and attenuate components of other frequencies. The way that the system output is related to the system input for different frequencies is called the frequency response of the system.

Since the frequency response is a complex function, we can convert it to polar notation in the complex plane. This will give us a magnitude and an angle. We call the angle the phase. Amplitude Response: For each frequency, the magnitude represents the system's tendency to amplify or attenuate the input signal.

![image](https://github.com/user-attachments/assets/e6b1016e-7db7-4be1-a4a2-9bbc26a9bd40)


Phase Response: The phase represents the system's tendency to modify the phase of the input sinusoids

![image](https://github.com/user-attachments/assets/69c5f691-63ce-4f83-899b-d3143686c39e)

The phase response, or its derivative the group delay, tells us how the system delays the input signal as a function of frequency.

Given Difference equation is ![image](https://github.com/user-attachments/assets/830d1a9c-c5f9-47f4-8ffd-34688e0a2077)


Algorithm: Step I : Give numerator coefficients of the given transfer function or difference equation. Step II : Give denominator coefficients of the given transfer function or difference equation Step III : Pass these coefficients to matlab command freqz to find frequency response. Step IV : Find magnitude and phase response using matlab commands abs and angle. Step V : Plot magnitude and phase response.

Flow Chart: ![image](https://github.com/user-attachments/assets/14d5f385-9cb3-4698-aa09-88a99768ebcc)


Output: Enter the numerator coefficients: [1] Enter the denominator coefficients: [1 -1/6 -1/6]

Output Waveforms: ![image](https://github.com/user-attachments/assets/2a2ebb3e-8410-4d33-a470-9299d1f04bb2)


RESULT:

VIVA QUESTIONS: 
1. Define Frequency response? 
A frequency response is how a system reacts to different tones or frequencies which helps engineers fine-tune its performance.

2. Define magnitude response? 
Magnitude response shows how much a system amplifies or reduces different frequencies, like an equalizer adjusting the volume of each tone.

3. Define Phase response? 
Phase response describes the timing relationship between an input signal and the system's output signal at each frequency.

4. Define transfer function.
It is a mathematical representation that fully characterizes a system's behavior, detailing how it transforms inputs into outputs. 

5. State the significance of difference equations. 
Difference equations are like step-by-step instructions where each step depends on the one before it. They help us understand how things change over time and make predictions, like with growing plants or money in a savings account.

6. What are the classifications of system based on unit sample response? 
	Finite impulse response systems
	Infinite impulse response systems

7. What is zero input response? 
The system's output when no input is applied, often due to initial conditions or stored energy is called the zero-input response.

8. Define impulse response? 
Impulse response is the system's output when presented with a very short, sharp input, revealing its fundamental dynamic characteristic.

9. Define System. 
Any process or entity that takes an input and produces a corresponding output, often involving transformation or modification of the input signal is called System.

10. Write mathematical formula to find response of any given system. 
For a system, the output is like mixing the input signal with the system’s memory (impulse response) over time. It’s summarized by: y[n]=∑h[k]⋅x[n−k] This means the current output depends on the input and how the system has behaved before

Exercise:

Find the frequency response of the system described by the difference equation y(n)-3/4 y(n-1)+1/8y(n-3)=x(n)+2x(n-1).
The frequency response of the system is: ![image](https://github.com/user-attachments/assets/660357b4-cb96-4403-aa50-82aa35a50e4d)
