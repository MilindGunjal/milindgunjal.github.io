---
title: "Advanced Derivative Pricing and Risk Management using the SABR Model"
layout: single
collection: projects
permalink: /projects/SABR_model
date: 2026-02-25

---
Abstract: 

Overview

This project provides a robust implementation and comparative analysis of the SABR (Stochastic Alpha, Beta, Rho) model—a sophisticated stochastic volatility framework designed to capture the "volatility smile" and "skew" prevalent in modern financial markets. While the traditional Black-Scholes model assumes constant volatility, this work demonstrates how the SABR model mathematically accounts for the dynamic relationship between an asset’s price and its volatility, offering a more accurate representation of market reality.

Key Methodologies
-
- Model Calibration: Leveraging real-time market data via yfinance, the project calibrates the four core SABR parameters ($\alpha, \beta, \rho, \nu$) to minimize the Sum of Squared Errors (SSE) against market-implied volatilities.
- Arbitrage-Free Forward Pricing: Implements the calculation of the Implied Forward Price ($F$) through Put-Call Parity, ensuring the model is grounded in actual market-clearing rates rather than theoretical spot-price approximations.
- Calculating Greeks: Provides a deep dive into the "Smile Greeks"—Delta, Gamma, Vega, Vanna, and Volga. By incorporating the "volatility backbone" (the sensitivity of implied vol to price moves), the project highlights the necessary adjustments for precise delta-hedging.

Comparative Findings
- 
- The analysis visually and numerically compares SABR outputs against the Constant Volatility Black-Scholes baseline and Market Last Traded Prices (LTP).
- Pricing Accuracy: Demonstrates that the SABR model significantly reduces pricing errors for Out-of-the-Money (OTM) options by accounting for "fat-tailed" return distributions.
- Risk Mitigation: The comparison of Greeks reveals the "Hedge Leakage" inherent in Black-Scholes, specifically showing how SABR Vanna and Volga capture risks that traditional models ignore—namely, the risk of a changing skew and the volatility-of-volatility.

- [Github](https://github.com/MilindGunjal/SABR_model)
- [Jupyter Notebook](https://github.com/MilindGunjal/SABR_model/blob/main/SABR.ipynb)
