# Behavioral Model Estimation – Contingent Valuation & Structural Simulation

This repository contains my code and analysis for a structural estimation exercise inspired by **Problem Set 2** of *ECON 35650 (Behavioral Development Economics)* with **Professor Anne Karing** at the University of Chicago. The assignment centers around a **contingent valuation (CV)** setup used to estimate behavioral parameters in public goods provision decisions.

---

## 📌 What This Project Does

This project simulates and structurally estimates individual decision-making using a CV design with varying parameters across treatment arms. It:

1. Simulates four empirical moments from a simple 2×2 design (tax × consequentiality).
2. Conducts comparative statics by varying one structural parameter at a time.
3. Implements GMM to recover parameters $(\mu_v, \sigma_v, p_l, p_h)$ under basic and full models.
4. Expands the model to include social signaling $(s \sim \mathcal{N}(\mu_s, \sigma_s))$ and incentives $(I)$.
5. Tests parameter identification using richer experimental designs with 12 treatment cells.
6. Compares estimation results when the model omits key behavioral components.
7. Calculates standard errors using the Jacobian and empirical moment variance.

---

## 📊 Key Findings

- **Valuation parameters** ($\mu_v, \sigma_v$) are identifiable and move empirical moments clearly.
- **Consequentiality parameters** ($p_l, p_h$) are weakly identified in simpler designs.
- Introducing **incentives** and **signaling** increases moment variation and improves identification.
- Estimating a misspecified model (e.g., ignoring $s$) leads to biased estimates of $p$ and $v$.
- Even with full designs, **parameter recovery remains noisy**, showing the limitations of partial identification with few moments.

---

## 📚 Context and Attribution

- This code builds on estimation exercises in Brandon et al. (2016) and DellaVigna et al. (2017).
- I used [ChatGPT-4o] to assist with function structure, simulation logic, and comparative plots.
- All simulations use `N = 100,000` per cell unless otherwise stated.
