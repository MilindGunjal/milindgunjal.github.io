---
title: "SABR Stochastic Volatility Model: Calibration, Greeks, and Copula-Based Multi-Asset Pricing"
layout: single
collection: projects
permalink: /projects/SABR_model

---
Abstract
-
This project implements and explores the SABR (Stochastic Alpha, Beta, Rho) model — an industry-standard stochastic volatility framework used to capture the volatility smile observed in real options markets, where implied volatility varies across strike prices rather than remaining constant as the Black-Scholes model assumes.
Using live options data sourced via yfinance, the project calibrates the four SABR parameters (α, β, ρ, ν) to market-implied volatilities through numerical optimization, fitting the volatility smile for equity instruments such as SPY. Forward prices are derived both analytically and from put-call parity, with the two methods benchmarked against each other. Calibrated SABR implied volatilities are then used to price call and put options and compared against Black-Scholes prices under a constant historical volatility assumption, illustrating the practical limitations of the constant-vol model in capturing skew and excess kurtosis.
The project further computes a full set of option Greeks — Delta, Gamma, Vega, Vanna, and Volga — for the SABR model using numerical finite differencing (bumping), alongside closed-form Black-Scholes Greeks, with spot-adjusted versions derived via the chain rule. These Greeks are applied in a delta hedging backtest using one year of historical price data, and extended to a framework for multi-Greek hedging (Gamma, Vega, Vanna, Volga neutrality) using a second option as the hedging instrument.
In the final section, the SABR model is integrated with copula dependency modeling to price multi-asset exotic derivatives — specifically, worst-of put and best-of call options on a two-asset basket (SPY and TSLA). Three copula structures are compared via Monte Carlo simulation: the Gaussian copula, the Student's t-copula (capturing symmetric tail dependence), and the Clayton copula (capturing asymmetric lower-tail dependence, modeling the tendency of assets to crash together). The project analyzes how the choice of copula meaningfully affects joint crash probabilities and option prices, underscoring the inadequacy of simple correlation coefficients for tail-risk-sensitive derivatives.

- [Github](https://github.com/MilindGunjal/SABR_model)
- [Jupyter Notebook](https://github.com/MilindGunjal/SABR_model/blob/main/SABR.ipynb)
