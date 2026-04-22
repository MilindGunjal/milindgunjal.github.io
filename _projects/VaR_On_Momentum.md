---
title: "Quantitative Momentum Trading & Value-at-Risk (VaR) Optimization"
layout: single
collection: projects
permalink: /projects/VaR_On_Momentum
date: 2026-04-23

---
Abstract: This project explores the development, backtesting, and risk-validation of a high-conviction momentum trading strategy focused on the Nifty 100 universe. The core strategy utilizes 52-week high breakouts as entry signals, coupled with a 10-week low trailing stop-loss mechanism to capture sustained trend extensions while mitigating downside volatility.

The research is divided into two primary phases:

Performance Engineering: I implemented and backtested three strategic variations—incorporating market regime filters (Nifty 50-SMA), relative strength ranking, and volatility-adjusted stops. These optimizations successfully reduced the portfolio’s Beta and significantly improved the Sharpe Ratio and alpha compared to a static momentum baseline.

Risk Validation: To ensure institutional-grade capital protection, the project employs a multi-model Value-at-Risk (VaR) framework, including Historical Simulation, Variance-Covariance, and Monte Carlo methods. The integrity of these risk models is rigorously evaluated through Traffic Light Analysis and Kupiec Backtesting (Likelihood Ratio tests), ensuring that observed breaches remain within statistically acceptable limits for "Good" regulatory ratings.

The final system demonstrates a disciplined quantitative approach to navigating equity momentum, balancing aggressive alpha generation with a mathematically sound defensive posture.

- [Github](https://github.com/MilindGunjal/VaR_On_Momentum)
- [Jupyter Notebook](https://github.com/MilindGunjal/VaR_On_Momentum/blob/main/VaR_On_Momentum.ipynb) on theory, and the original momentum strategy.
- [Jupyter Notebook](https://github.com/MilindGunjal/VaR_On_Momentum/blob/main/VaR_On_Momentum_Improved_Strategies.ipynb) on comparison with improved momentum strategies.
