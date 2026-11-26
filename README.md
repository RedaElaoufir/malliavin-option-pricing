# Asian Option Delta Estimation using Malliavin Calculus

Monte Carlo pricing and sensitivity estimation for path-dependent options in the Black–Scholes model.

**Authors:** Mohamed Reda Elaoufir and Alexis Bruneau. MSc project, Université Paris 1 Panthéon-Sorbonne, March 2026. Original project supervisor: Christophe Chorro.

**Revision (November 2026):** This portfolio version includes AI-assisted mathematical corrections, refined explanations and numerical implementation improvements. It has not been reviewed or assessed by the course instructor.

## Methods

- Vectorized, batched simulation of geometric Brownian motion and trapezoidal quadrature.
- Central finite differences with common random numbers.
- Two Malliavin integration-by-parts weights.
- Sampling variance, 95% confidence intervals, paired estimator comparisons, and time-step and bump sensitivity.

## Main numerical result

With 20,000 paths, 250 time steps, a spot bump of 0.2 and the fixed seed in the notebook, the range digital payoff has approximately **149x** and **140x** lower pathwise variance under Malliavin methods 1 and 2, respectively, than under finite differences. For the continuous call payoff, finite differences have lower variance than either Malliavin estimator. These are experiment-specific results, not universal performance guarantees. Confidence intervals quantify Monte Carlo sampling error, not discretization or bump bias.

## Repository contents

- `asian_option_delta.ipynb`: executed numerical notebook with figures and tables.
- `theoretical_report.pdf`: revised theoretical report, including corrections and scope of the results.
- `requirements.txt`: Python dependencies.

## Reproduce

```bash
python -m pip install -r requirements.txt
jupyter notebook asian_option_delta.ipynb
```

Run all cells in order. No external data are needed. The model parameters are defined in the first code cell. The numerical notebook has been revised for clarity, correctness and reproducibility; the revised theoretical report explicitly identifies its changes and review status.
