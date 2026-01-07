# Option-Pricing-Stochastic-Analysis
# Stochastic Option Pricing: Monte Carlo vs. Black-Scholes
**Quantitative Finance Project | Stony Brook University**

## Overview
This repository contains a Python-based framework for pricing European options using two distinct methodologies: the analytical **Black-Scholes-Merton** model and a numerical **Monte Carlo Simulation**. The project focuses on the valuation of **Omnicom Group Inc. (OMC)**.

## Mathematical Foundation
The model assumes that the underlying asset price follows **Geometric Brownian Motion (GBM)**, defined by the Stochastic Differential Equation:

$$dS_t = \mu S_t dt + \sigma S_t dW_t$$

Where:
- $S_t$: Asset price at time $t$
- $\mu$: Risk-free rate (drift)
- $\sigma$: Volatility (diffusion)
- $W_t$: Wiener process (randomness)

## Features
- **Data Acquisition:** Automated retrieval of 252-day historical data via `yfinance`.
- **Calibration:** Calculation of annualized volatility ($\sigma = 31.77\%$) and current risk-free rate ($r = 3.97\%$).
- **Monte Carlo Engine:** 10,000 simulated price paths using NumPy vectorization for computational efficiency.
- **Validation:** Direct comparison of simulated results against Black-Scholes closed-form solutions to ensure convergence (accuracy within 1.3%).

## Usage
Open `Stock_Price_Predictor.ipynb` in a Jupyter environment. The script prompts for a Ticker, Strike Price, and Option Type (Call/Put) to generate fair value estimates.

## Contact
**Lia Li** - [LinkedIn](https://linkedin.com/in/lialil)
