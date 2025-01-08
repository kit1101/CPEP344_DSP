Laboratory Activity 3

Name : KEITH O'MYRAH M. ALABAT

Course and Year : BSCpE4

I. OBJECTIVES:

In this laboratory exercise, the students are expected to: • compute auto correlation between two sequences II. MATERIALS:

• Software: MATLAB

III. PROCEDURES:

THEORY:

Auto Correlation Function Auto correlation function is a measure of similarity between a signal & its time delayed version. It is represented with R(k). The auto correlation function of x(n) is given by R11(k)=R(k)= ![image](https://github.com/user-attachments/assets/d38b4b7c-e785-4250-af09-7e3557d30c13)


Algorithm: Step I : Give input sequence x[n]. Step II : Give impulse response sequence h (n) Step III: Find auto correlation using the matlab command xcorr. Step IV: Plot x[n], h[n], z[n]. Step V: Display the results

Flow Chart: ![image](https://github.com/user-attachments/assets/830247c3-bc28-47b9-a557-d49bd1fa4338)


Output:

enter input sequence [1 2 3 4] z = [3.99, 11, 20, 30, 20, 11, 3.99]

![image](https://github.com/user-attachments/assets/5259e9b1-e69e-4847-b44c-eeabb5763e02)


RESULT:

VIVA QUESTIONS: 
1.	Write mathematical formula to find auto correlation? 
Autocorrelation measures the similarity between a signal and a time-shifted version of itself. It's calculated by multiplying the signal with its shifted copy and integrating (for continuous signals) or summing (for discrete signals) the result over time. This reveals how much the signal correlates with itself at different delays.

The autocorrelation function, denoted as R(τ), measures the similarity between a signal and a time-shifted version of itself. For a continuous-time signal x(t), the autocorrelation is calculated as:
	R(τ) = ∫ x(t) * x(t + τ) dt where τ represents the time shift or lag. This integral essentially computes the product of the signal with its shifted version and integrates it over all time, indicating the degree of similarity at that particular lag. For discrete-time signals x[n], the autocorrelation is given by:
	R[k] = Σ x[n] * x[n + k] where k is the lag in discrete samples. This summation performs a similar operation, multiplying the signal with its shifted version and summing the result over all discrete time indices. Both formulas quantify the self-similarity of a signal at different time shifts.

2.	Define auto correlation?
In digital signal processing, autocorrelation measures the similarity between a signal and a time-shifted version of itself. By comparing the signal with delayed copies, it reveals repeating patterns and internal structure, aiding in tasks such as identifying periodic components, estimating signal properties, and filtering out noise.

3.	Define correlation.
Correlation describes the degree to which two or more variables are related. It indicates whether and how strongly they tend to change together.

4.	Difference between Auto correlation and convolution? 
Autocorrelation examines a signal's self-similarity, identifying recurring patterns within the signal itself, whereas convolution blends two distinct signals to create a new output, essentially altering the characteristics of the input signal.

5.	Difference between Auto correlation and cross correlation? 
Autocorrelation measures the similarity of a signal to a time-shifted version of itself, revealing internal patterns, while cross-correlation measures the similarity between two different signals, identifying time shifts where they align or exhibit similar behavior.

6.	Write mathematical formula to find cross correlation?
Cross-correlation measures the similarity between two different signals at different time shifts. It does this by multiplying one signal with a shifted version of the other and integrating (for continuous signals) or summing (for discrete signals) the result. This reveals how much the signals resemble each other at different alignments.
	R<sub>xy</sub>(τ) = ∫ x(t) * y(t + τ) dt (This formula multiplies the first signal x(t) by a time-shifted version of the second signal y(t + τ) and integrates the product over all time. This process essentially slides one signal past the other, computing the similarity at each lag.)
	R<sub>xy</sub>[k] = Σ x[n] * y[n + k] (where k represents the lag in discrete samples. Similar to the continuous case, this formula multiplies the first signal by a shifted version of the second and sums the result over all discrete time indices. The result indicates how much the signals resemble each other at different relative positions.)

7.	What is the length of the resultant sequence of auto correlation?
The length of the resulting autocorrelation sequence is typically 2N - 1, where N is the length of the original signal. This occurs because autocorrelation involves correlating the signal with time-shifted versions of itself, extending the length of the resulting sequence beyond the original signal's length.

8.	List few applications of correlation. 
Correlation is a powerful tool used in different fields, including finance, marketing, healthcare, social sciences, and many more.

9.	Give the properties of auto correlation.
	Autocorrelation matrix
	Autocorrelation sequence
	Autocorrelation function
	Randomness or White Noise

10.	Define cross correlation.
Cross-correlation is measuring how two signals are similar and how they resemble well with each other.

Exercise: 
1. Find the auto correlation function of ramp sequence for 0≤n≤6.
To find the autocorrelation function of a ramp sequence for 0≤n≤6, we need to first define the ramp sequence and then apply the autocorrelation formula. to Define the Ramp Sequence: A ramp sequence is a sequence where each element increases linearly. For 0≤n≤6, the ramp sequence x[n] can be written as: x[n]=n This gives us x={0,1,2,3,4,5,6}.

For Autocorrelation Formula: The autocorrelation function 𝑅𝑥𝑥(k) for a discrete-time sequence x[n] is defined as: ![image](https://github.com/user-attachments/assets/8032905b-1f57-48dc-87e5-6cb48dfecdc0)


Here, k is the lag, and N is the length of the sequence, which in this case is 7.
Compute the Autocorrelation Values: We calculate 𝑅xx(k) for each lag k from 0 to 6. Let's calculate the autocorrelation values for each lag 𝑘. The autocorrelation function 𝑅xx​(k) of the ramp sequence x[n]= {0,1,2,3,4,5,6} for 0≤n≤6 is: Rxx(k)={91,70,50,32,17,6,0}

This sequence represents the autocorrelation values for each lag 𝑘 from 0 to 6.
