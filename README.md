# qGAN on financial S&P500 Data
## Problem Statement : Quantum Generative Adversarial Network (qGAN) for Financial Time Series Synthesis 

### 1. Background & Problem Statement
Financial risk modeling, stress-testing, and portfolio optimization demand extensive historical market datasets to simulate black-swan scenarios and market shocks. However, real-world financial time series data is highly scarce, proprietary, and limited by non-stationary historical regimes. Standard generative models like classical GANs or VAEs struggle to adequately replicate the intrinsic statistical properties of financial data, such as heavy-tailed distributions (fat tails) and volatility clustering, without requiring massive amounts of training samples. A Quantum Generative Adversarial Network (qGAN) leverages a parameterized quantum circuit (PQC) as its generator node alongside a classical discriminator network. This hybrid model captures complex non-linear multi-variable probability distributions natively through quantum superposition and entanglement, enabling the synthesis of realistic macroeconomic and stock return distributions from small, compact empirical datasets.
### 2. Technical Architecture & Methodology
- Data Source: S&P 500 historical daily returns or customized index data extracted via the Yahoo Finance API.
- qGAN Architecture: ○ Generator: Parameterized Quantum Circuit (PQC) designed as a custom ansatz in Qiskit, using the Qiskit Machine Learning generative training paradigms to sample continuous asset return values.
- Discriminator: A classical PyTorch MLP or LSTM network trained to differentiate real asset streams from synthetic ones.
- Training Enhancements: Implement explicit gradient penalties (WGAN-GP style) or mode-collapse mitigation strategies tuned for Qiskit simulator backends or runtime environments.
- Fidelity Evaluation: Quantitative validation using the Kolmogorov-Smirnov (KS) statistical test, autocorrelation functions (ACF), and Value-at-Risk (VaR) / Conditional Value-at-Risk (CVaR) boundary matches between real and generated profiles.
