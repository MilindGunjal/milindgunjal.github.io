---
title: "Quantitative Momentum Trading & Value-at-Risk (VaR) Optimization"
layout: single
collection: projects
permalink: /projects/VaR_On_Momentum

---
Abstract
-
This project develops a high-performance quantitative framework for systematic asset management, emphasizing rigorous statistical validation and multi-model risk engineering. While the primary objective is to demonstrate a robust methodology for strategy lifecycle management—from signal generation to portfolio optimization—the framework is applied to a momentum-based investment universe within the Indian NSE (National Stock Exchange).

Core Methodologies & Technical Architecture 
-
- Statistical Risk Engine: The centerpiece of the project is an institutional-grade risk assessment module. It implements three distinct Value-at-Risk (VaR) methodologies—Historical Simulation, Variance-Covariance (Parametric), and Monte Carlo Simulation. These models provide a multi-faceted view of potential capital erosion under different market distributions.

- Model Validation & Backtesting: To ensure the reliability of the risk engine, I employed Kupiec Likelihood Ratio (POF) tests and Traffic Light Analysis. This rigorous backtesting of the VaR models ensures that the predicted risk parameters align with empirical market behavior, maintaining "Green Zone" regulatory standards even during periods of high volatility.

- Portfolio Optimization: Beyond simple allocation, the project utilizes Markowitz Mean-Variance Optimization (MVO) to determine the efficient frontier. By mathematically balancing expected returns against covariance-derived risk, the framework transitions from naive equal-weighting to a risk-optimized capital allocation model.

- Performance Analytics: Strategy efficacy is quantified using a comprehensive suite of risk-adjusted metrics, including Annualized Alpha, Portfolio Beta, Sharpe Ratio, and Maximum Drawdown analysis, allowing for precise benchmarking against the Nifty 50 and Nifty 100 indices.

Strategy Implementation (Contextual Application)
-
The framework is stress-tested using a trend-following momentum strategy. This implementation leverages 52-week high breakouts as primary entry signals, governed by a 50-day Simple Moving Average (SMA) market-regime gate. By utilizing the 50-day SMA as both a macro-trend filter and a trailing stop-loss mechanism, the strategy identifies periods of momentum persistence while systematically mitigating tail risk. Advanced iterations further refine this by ranking assets through risk-adjusted Relative Strength (RS), effectively isolating market leaders that demonstrate superior resilience during index-level pullbacks.

- [Github](https://github.com/MilindGunjal/VaR_On_Momentum)
- [Jupyter Notebook](https://github.com/MilindGunjal/VaR_On_Momentum/blob/main/VaR_On_Momentum.ipynb) on theory, and the original momentum strategy.
- [Jupyter Notebook](https://github.com/MilindGunjal/VaR_On_Momentum/blob/main/VaR_On_Momentum_Improved_Strategies.ipynb) on comparison with improved momentum strategies.
