# 🎧 Signal Sampling & Frequency Analysis – Lab 02 Report

> **Course**: BEGY6503 – Biomedical Instrumentation  
> **Lab Focus**: Sampling, Aliasing, FFT, Spectral Leakage, and Windowing in Biomedical Signal Analysis  
> **Team**: Ameya Srivastava, Mariam Zoair, Qing Xiang  
> **Tools**: MATLAB, Excel, Signal Processing Techniques

---

## Objective

This lab aims to explore the principles of **digital signal sampling and frequency analysis** using sinusoidal waveforms. Through MATLAB simulations and FFT processing, we investigate phenomena such as:

- Sampling accuracy and the **Nyquist criterion**
- **Aliasing** and how to detect/prevent it
- Effects of **window functions** on frequency leakage
- Signal characteristics in both **time** and **frequency** domains

---

## Experiments Overview

### **Exercise 1: Sampling & Frequency Resolution**

- Analyzed how sampling rate (fs), input frequency (fi), and sample size (N) affect:
  - Time resolution (Δt)
  - Frequency resolution (Δf)
  - FFT peak location and amplitude
- Confirmed **Nyquist Theorem**: No aliasing occurs when fs ≥ 2fi
- Observed **spectral leakage** when fi/Δf is non-integer

### **Exercise 2: Aliasing Behavior & Minimum Sampling Rate**

- Demonstrated aliasing when fs < 2fi  
- Calculated alias frequency using |fi - n·fs|
- Identified the **minimum sampling rate** to avoid aliasing
- Validated theoretical vs practical sampling (using 2fi + 1 to ensure safety margin)
- Confirmed accuracy improvements when fs = 5·fi

### **Exercise 3: Leakage & Windowing Effects**

- Compared FFT with:
  - No window
  - **Hanning window**
  - **Hamming window**
- Key Findings:
  - Hanning: Better leakage suppression, slightly lower peak amplitude
  - Hamming: Higher amplitude, but more side lobes (leakage)
  - No window: Max amplitude but highest leakage

### **Exercise 4: Time-Varying Signals & Spectrograms**

- Simulated sinusoidal tones with:
  - Decaying amplitude (changing time constant, tc)
  - Linear and non-linear frequency variation
- Studied how signal behavior reflects in:
  - Sound characteristics
  - Time domain signal
  - FFT spectra
  - **Spectrograms** for time-frequency representation
- Observed reversal behavior in time vs spectrogram axes

---

## Key Concepts Reinforced

| Concept               | Observed Using                     |
|-----------------------|------------------------------------|
| Nyquist Criterion     | FFT plots, alias frequency checks  |
| Frequency Resolution  | Δf = fs / N                        |
| Spectral Leakage      | FFT peaks spreading (fi/Δf ≠ int)  |
| Windowing Effects     | Amplitude drop vs leakage control  |
| Aliasing              | FFT mismatch when fs < 2fi         |
| Spectrogram Analysis  | Time-frequency behavior comparison |

---

## Sample Result: Aliasing Behavior (Exercise 2.1)

| fi (Hz) | fs (Hz) | FFT Output Freq | Aliased? | Alias Freq |
|--------:|--------:|----------------:|----------|------------|
| 55      | 100     | 45 Hz           | ✅ Yes    | 45 Hz      |
| 90      | 100     | 10 Hz           | ✅ Yes    | 10 Hz      |
| 30      | 100     | 30 Hz           | ❌ No     | –          |

---

## Key Takeaways

- **Theory vs Reality**: Real-world signals require fs > 2fi due to truncation, numerical errors, and non-integer cycles.
- **Windowing** is essential for reducing leakage but involves a trade-off with signal amplitude.
- **Spectrograms** are powerful for visualizing how signals evolve over time, especially for frequency sweeps or decay.
- **Signal decay** leads to amplitude spread in frequency domain, even when dominant frequency remains constant.

---

## Tools Used

- 🔢 **MATLAB** – Signal simulation, FFT, spectrograms, and figure generation
- 📊 **Excel** – Tabular data processing, calculations, and observations
- 🎧 **Auditory Tools** – Listening to decaying and sweeping tones to analyze temporal effects

---

## Conclusion

This lab provided practical experience in the **digital processing of biomedical signals**, deepening understanding of:

- Sampling principles and their practical limitations
- Frequency-domain transformations via FFT
- Real-world signal challenges such as aliasing and leakage
- Benefits of windowing and time-frequency analysis

The experiments reinforce theoretical concepts using visual and auditory feedback, preparing us for real-world biomedical signal acquisition and processing challenges.

---
