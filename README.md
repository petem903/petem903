# Pete Mathew

**Automation & Controls Engineer @ Yanfeng Automotive Interiors**

I build and program control systems for automotive interior manufacturing. My work spans PLC programming and industrial automation on the floor, signal processing and data analysis in Python, and firmware for embedded hardware. EE degree from Texas State University.

---

## Technical Skills

| Domain | Tools & Languages |
|---|---|
| Automation & Controls | PLC programming, industrial process control, machine vision (OpenCV) |
| Signal Processing & DSP | FFT, FIR/IIR filter design, Laplace/Fourier analysis, pole-zero methods |
| Scientific Computing | Python, NumPy, SciPy, SymPy, Pandas, Matplotlib, Jupyter |
| Embedded Systems | C/C++, Arduino, SPI, I²C, 74HC595, 7-segment displays, LCD |
| Hardware & EE Theory | Digital Logic, VLSI, Circuits, Signals & Systems, Semiconductor Devices |
| Design Tools | Multisim, Quartus, KiCad |

---

## Engineering Notebooks

**[`petem903/engineering-notebooks`](https://github.com/petem903/engineering-notebooks)** — Full repository of Python/Jupyter work organized by discipline.

### Thermal Systems Analysis
**[Heating Pad Thermal Analysis](https://github.com/petem903/engineering-notebooks/blob/main/thermal-analysis/heating_pad_thermal_analysis.ipynb)**
Real sensor data pipeline: 4-probe system at 1 Hz, multi-format ingestion (CSV + ODS), automatic steady-state detection via finite-difference dT/dt, multi-file aggregation, and 300 DPI publication figures.
`pandas` · `numpy` · `matplotlib` · `scipy`

### Signals & Systems
**[Laplace & Fourier Frequency Analysis](https://github.com/petem903/engineering-notebooks/blob/main/signals-systems/laplace_fourier_frequency_analysis.ipynb)**
Symbolic Laplace and inverse Laplace transforms for piecewise/exponential signals including repeated poles. Full Fourier series derivation (a₀, aₙ, bₙ) via symbolic integration, signal reconstruction from harmonics, and magnitude/phase frequency response plots.
`sympy` · `numpy` · `matplotlib`

**[FFT & Spectral Analysis](https://github.com/petem903/engineering-notebooks/blob/main/signals-systems/fft_spectral_analysis.ipynb)**
Spectral analysis of multi-tone signals. Zero-padding effects on frequency resolution, zero-stuffing, spectral modulation via sign-flipping, aliasing from undersampled signals. Nyquist criterion analysis.
`numpy` · `matplotlib`

**[Digital Filter Design — Convolution & Pole-Zero](https://github.com/petem903/engineering-notebooks/blob/main/signals-systems/filter_design_convolution.ipynb)**
FIR filter design from pole-zero specs: `zpk2tf` conversion, impulse response, pole-zero diagrams on the complex plane, DTFT frequency response in dB and radians, passband/stopband validation.
`scipy.signal` · `numpy` · `matplotlib`

### Numerical Methods
**[DFT from Scratch · Gaussian Elimination · Newton-Raphson](https://github.com/petem903/engineering-notebooks/blob/main/numerical-methods/dft_gaussian_elimination_newton_raphson.ipynb)**
Three hand-built implementations: O(N²) DFT/IDFT with round-trip verification, manual Gaussian elimination with back-substitution (no `numpy.linalg`), and Newton-Raphson root finding for transcendental/polynomial equations. Includes `timeit` benchmarking of manual vs. `numpy.dot` matrix multiply across sizes 4×4–20×20.
`numpy` · `matplotlib` · `timeit`

**[Taylor Series & Signal Reconstruction](https://github.com/petem903/engineering-notebooks/blob/main/numerical-methods/taylor_series_signal_reconstruction.ipynb)**
eˣ, e⁻ˣ, sin(x), cos(x) built from first principles with convergence to `error < 10⁻⁶`. Validated against `math` library over 20 random test values. Implements signal downsampling (x[2n], x[4n]) with linear interpolation recovery.
`numpy` · `math`

---

## Projects

**[VisionSystemAI — Industrial Process Flow](https://github.com/petem903/VisionSystemAIforIndustrialProcessFlow)**
OpenCV-based machine vision system for automated restock tracking in an industrial production environment.

**[Autonomous Line Following Robot](https://github.com/petem903/Line-Following-Robot)**
PID-controlled robot navigating a line course autonomously. Senior design capstone — full hardware/firmware build.

**[Industrial Automation Portfolio](https://github.com/petem903/Portfolio)**
Controls and automation work from co-op and employment at Yanfeng Automotive Interiors.

---

## Code Snippets

| Snippet | Language | Topic |
|---|---|---|
| [74HC595 Hex Display Counter](https://gist.github.com/petem903/77b51a8d4f5c0913dc7f30c472ef9d7e) | Arduino | Shift register, 7-seg display, SPI |
| [Dice Gambling Game](https://gist.github.com/petem903/00b9f3de1b9c3d2154bc350c20d64894) | C++ | Input validation, game loop |
| [Grade Drop Calculator](https://gist.github.com/petem903/bd7e1259151010bb1c4cf502729f5489) | C++ | Arrays, function decomposition |
| [Weekly Payroll Calculator](https://gist.github.com/petem903/5c9c573aba1984a8fc01ec73acc28901) | C++ | Modular functions, validation |

---

*Automation & Controls Engineer @ Yanfeng Automotive Interiors · EE @ TXST · DSP · Embedded Systems*
