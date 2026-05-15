---
title: "Quantitative Finance Boot Camp (Erdős Institute) Notes"
layout: single
collection: projects
permalink: /projects/QuantBootCampNotes

---
Abstract
--
This notebook develops a quantitative framework for stochastic asset price modelling, derivatives pricing, and portfolio risk management, completed as part of the Erdős Institute Quantitative Finance Boot Camp. Beginning from first principles, it implements Geometric Brownian Motion for correlated multi-asset portfolios and uses Monte Carlo simulation to estimate Value-at-Risk, demonstrating how correlation structure governs tail risk. The Black–Scholes model is derived and implemented, with implied volatility extracted from live TSLA option data and visualised as a volatility smile across strikes and maturities. To address the empirical failure of constant volatility, the Heston stochastic volatility model is introduced: its mean-reverting variance process is simulated via Euler–Maruyama discretisation, and European option prices are computed semi-analytically through Fourier inversion of the characteristic function. The model is then calibrated to real market option prices by minimising mean squared pricing error using the L-BFGS-B algorithm. The project concludes with an empirical delta hedging backtest on a real historical stock path, reporting the discounted profit-and-loss of the strategy.

Summary
--
The notebook is structured as eight modules, each pairing mathematical theory with a working Python implementation.
The first module simulates correlated multi-asset portfolios under Geometric Brownian Motion, using a full correlation matrix validated for symmetry and positive semi-definiteness, with Cholesky decomposition to generate correlated noise. The second module uses those simulated paths to estimate Value-at-Risk at the 99% confidence level, comparing a correlated (hedged) portfolio against an independent (unhedged) one to quantify the risk-reduction effect of cross-asset correlation.
The third module implements the Black–Scholes formula for European calls and puts, covering the Greeks and put–call parity. The fourth applies it to live market data: TSLA option chains are downloaded from Yahoo Finance, spot prices are matched to trade timestamps at minute resolution, and implied volatility is recovered for every contract by inverting Black–Scholes numerically via Brent's method — revealing the characteristic equity volatility skew across expiries.
The fifth module introduces the Heston model, simulating coupled stock and variance paths with the Feller condition monitored throughout. The sixth prices European options under Heston semi-analytically, recovering the two risk-adjusted probabilities that enter the pricing formula by numerically integrating the characteristic function, and derives the Heston delta analytically as the first of those probabilities.
The seventh module calibrates the five Heston parameters to the TSLA option market by minimising mean squared pricing error over a curated set of expiry dates with well-behaved volatility smiles, using the L-BFGS-B optimiser with economically motivated parameter bounds. The eighth and final module backtests the resulting model on a real two-year TSLA price history, recomputing the Heston delta daily using rolling realised variance, and decomposing the total discounted P&L into call payout and hedge profit components.

- [Jupyter Notebook](https://github.com/MilindGunjal/QuantFinanceBootcamp2025/blob/main/QuantBootCamp_Summary.ipynb) 
