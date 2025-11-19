# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

# __Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

# __Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
# __Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

# __Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

# __Program:__
```
import numpy as np 
import matplotlib.pyplot as plt 
Ac = 8 
fc = 2500 
Am = 2.5 
fm = 250 
fs = 25000 
beta = 3.6 
t = np.arange(0, 2/fm, 1/fs) 
Em = Am * np.cos(2 * np.pi * fm * t) 
Ec = Ac * np.cos(2 * np.pi * fc * t) 
Efm = Ac * np.cos(2 * np.pi * fc * t + beta * np.sin(2 * np.pi * fm *t)) 
plt.figure(figsize=(10, 6)) 
plt.subplot(3, 1, 1) 
plt.plot(t, Em) 
plt.grid() 
plt.subplot(3, 1, 2) 
plt.plot(t, Ec) 
plt.grid() 
plt.subplot(3, 1, 3) 
plt.plot(t, Efm) 
plt.grid() 
plt.tight_layout() 
plt.show()
```

# __Output:__
![WhatsApp Image 2025-11-19 at 13 51 30_d856a5f2](https://github.com/user-attachments/assets/7398c3f8-16d2-4fc6-991a-986be0da1839)

# TABULATION:
![WhatsApp Image 2025-11-19 at 14 05 44_a5cd9a6c](https://github.com/user-attachments/assets/7d7e1917-18a0-4e3b-b00b-dea5142c939d)


# CALCULATION:
![WhatsApp Image 2025-11-19 at 14 05 44_7874c988](https://github.com/user-attachments/assets/5b916cf8-e86b-4a31-9a02-18a9d014b824)



# __Result:__
Thus the Frequency Modulation and Demodulation using NumPy and Matplotlib is verified successfully.
