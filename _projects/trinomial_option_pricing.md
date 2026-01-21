---
title: "Trinomial Tree Option Pricing: A Discussion"
layout: single
collection: projects
permalink: /projects/trinomial_option_pricing
date: 2026-01-21

---
Abstract: The study begins with the Binomial model, demonstrating how its step-by-step backward induction allows for the valuation of early exercise features in American options—a capability lacking in the standard Black-Scholes formula. It further investigates the Trinomial Tree model, which introduces a "stay" node to improve convergence stability and computational efficiency. Key comparative analyses include: 
 - Early Exercise Incentives: Evaluating how dividend yields ($q$) and interest rates ($r$) create price premiums for American options compared to their European counterparts.
 - Put-Call Parity: Demonstrating that while strict parity holds for European options, American options are governed by specific price inequalities.
 - The Greeks: Implementing methodologies to calculate price sensitivities, including Delta, Gamma, and Theta via internal tree nodes, and Vega and Rho using numerical finite difference (bumping) methods.
 
  Results confirm that the Trinomial model provides a smoother convergence to Black-Scholes-Merton values as the number of time steps ($N$) increases, establishing it as a robust industry standard for complex exotic and American options.

- [Github](https://github.com/MilindGunjal/Trinomial-trees)
- [Jupyter Notebook](https://github.com/MilindGunjal/Trinomial-trees/blob/main/Trinomial_tree_option_pricing.ipynb)
