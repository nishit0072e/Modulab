# ModuLab: Ultimate Modulation Workspace

**ModuLab** is a powerful, interactive, browser-based simulation tool designed for students, engineers, and enthusiasts to visualize and understand complex telecommunications modulation schemes.

Unlike static diagrams, ModuLab generates signals in real-time using Digital Signal Processing (DSP) algorithms directly in your browser, allowing you to tweak parameters and instantly see the results in the time and frequency domains.

## 🚀 Quick Start

**No installation required!** ModuLab is built as a Single File Application.

1.  Download the `index.html` file.
2.  Double-click it to open it in any modern web browser (Chrome, Firefox, Edge, Safari).
3.  Start exploring!

## ✨ Key Features

* **Real-Time Signal Generation:** Waveforms are calculated mathematically on the fly, not pre-rendered videos.
* **Triple-Scope Visualization:**
    * **Input:** See the raw message signal (analog sine or digital bitstream).
    * **Intermediate:** Visualize carrier waves, spreading codes, sampling pulses, or control voltages.
    * **Output:** The final modulated signal with adjustable channel noise.
* **Analysis Tools:**
    * **Constellation Diagram:** Real-time I/Q plotting to visualize phase and amplitude states.
    * **Power Spectral Density (PSD):** FFT-based frequency spectrum analyzer with logarithmic scaling.
    * **BER Calculator:** Live Bit Error Rate estimation for digital schemes.
* **Interactive Controls:**
    * Adjust **SNR (Signal-to-Noise Ratio)** to simulate channel interference.
    * Tweak Carrier Frequency, Modulation Index, Symbol Rates, and "M" (constellation size).
    * Zoom and Pan time-domain controls.
* **Export:** Download signal data as `.csv` or capture scope views as `.png` images.

## 📡 Supported Modulation Schemes

ModuLab supports over 30 distinct modulation architectures across 9 categories:

### 1. Basic Analog
* **AM:** Amplitude Modulation
* **DSB-SC:** Double Sideband Suppressed Carrier
* **SSB-SC:** Single Sideband (USB)
* **VSB:** Vestigial Sideband

### 2. Angle Modulation
* **FM:** Frequency Modulation
* **PM:** Phase Modulation
* **NBFM:** Narrowband FM
* **WBFM:** Wideband FM

### 3. Complex Analog
* **Armstrong FM:** Indirect FM generation via integration and phase modulation.
* **MPX Stereo:** FM Stereo Multiplexing (L+R, L-R, Pilot, Subcarrier).

### 4. Pulse / PCM
* **PCM:** Pulse Code Modulation (Analog-to-Digital quantization visualizer).
* **PWM:** Pulse Width Modulation.
* **PAM:** Pulse Amplitude Modulation.
* **PDM:** Pulse Density Modulation (Sigma-Delta simulation).

### 5. FSK Family
* **BFSK:** Binary FSK.
* **MFSK:** M-ary FSK (multi-tone).
* **MSK:** Minimum Shift Keying.
* **GMSK:** Gaussian MSK (used in GSM).

### 6. PSK Family
* **BPSK:** Binary PSK.
* **QPSK:** Quadrature PSK.
* **OQPSK:** Offset QPSK.
* **DPSK:** Differential PSK.
* **M-PSK:** M-ary PSK (e.g., 8-PSK).

### 7. QAM & Amplitude Digital
* **ASK:** Binary Amplitude Shift Keying.
* **M-ASK:** M-ary ASK (e.g., 4-ASK).
* **16-QAM:** 16-state Quadrature Amplitude Modulation.
* **64-QAM:** 64-state High-order QAM.

### 8. Spread Spectrum & Multicarrier
* **DSSS:** Direct Sequence Spread Spectrum.
* **FHSS:** Frequency Hopping Spread Spectrum.
* **OFDM:** Orthogonal Frequency Division Multiplexing (4-subcarrier visualization).

### 9. Specialized / Modern
* **Polar:** Polar Modulation architecture.
* **OTFS:** Orthogonal Time Frequency Space (Delay-Doppler conceptual visualizer).

## 🛠️ Tech Stack

* **HTML5 Canvas API:** For high-performance 60fps rendering of oscilloscopes and constellation diagrams.
* **React:** For UI state management and component structure.
* **Tailwind CSS:** For responsive, modern styling.
* **Babel (Standalone):** Allows JSX compilation in the browser without a build step.

## 🤝 Contribution & Pull Request are welcome

ModuLab is open for experimentation! Since the logic is contained in simple JavaScript functions within the `SCHEMES` array, you can easily add your own modulation types.

1.  Look for the `SCHEMES` constant in the script.
2.  Add a new object with a unique `id`, `name`, and `gen` function.
3.  The `gen` function receives time `t` and parameters `p` and returns the signal value.

## 📄 License

