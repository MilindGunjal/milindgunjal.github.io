---
title: "Trinomial Tree Option Pricing using Hidden Markov Model"
layout: single
collection: projects
permalink: /projects/trinomial_option_pricing

---
Abstract
-

This project extends a discrete-time framework for option pricing — beginning with the classical Binomial model and progressing to the Trinomial Tree — to incorporate real-time, regime-aware volatility estimation via Markov and Hidden Markov Models. The study begins with the Binomial model, demonstrating how its step-by-step backward induction allows for the valuation of early exercise features in American options — a capability lacking in the standard Black-Scholes formula. It further investigates the Trinomial Tree model, which introduces a "stay" node to improve convergence stability and computational efficiency. Key comparative analyses include:

- **Early Exercise Incentives:** Evaluating how dividend yields ($q$) and interest rates ($r$) create price premiums for American options compared to their European counterparts.
- **Put-Call Parity:** Demonstrating that while strict parity holds for European options, American options are governed by specific price inequalities.
- **The Greeks:** Implementing methodologies to calculate price sensitivities, including Delta, Gamma, and Theta via internal tree nodes, and Vega and Rho using numerical finite difference (bumping) methods.

The project then addresses a fundamental limitation of constant-volatility models: real markets cycle between calm and turbulent regimes. Two stochastic regime models are introduced and calibrated on real market data. The **2-State Markov Regime-Switching Model** classifies market conditions into low- and high-volatility regimes using rolling realised volatility, and estimates a transition matrix to derive a stationary-distribution-weighted volatility. The **Gaussian Hidden Markov Model (HMM)** treats regimes as latent states, inferring emission distributions and transition dynamics from observed log-returns alone via the Baum–Welch EM algorithm, with optimal state decoding via the Viterbi algorithm. The resulting regime-adjusted volatility estimates — Historical, Markov, and HMM — are each fed into the Trinomial pricing engine to produce European and American call and put prices, with full Greek surfaces plotted across strikes.

Results confirm that the Trinomial model provides a smoother convergence to Black-Scholes-Merton values as $N$ increases, and that regime-based volatility inputs produce meaningfully distinct option prices: historical volatility yields the most conservative estimates, while HMM-inferred volatility, by isolating the low-volatility regime more precisely, produces the most aggressive pricing — underscoring the practical importance of volatility regime modelling in derivatives valuation.

- [Github](https://github.com/MilindGunjal/Trinomial-trees)
- [Jupyter Notebook](https://github.com/MilindGunjal/Trinomial-trees/blob/main/Trinomial_tree_with_HMM.ipynb)
