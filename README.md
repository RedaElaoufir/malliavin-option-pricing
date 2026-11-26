# Asian Option Delta Estimation using Malliavin Calculus

Monte Carlo pricing and sensitivity estimation for path-dependent options in the Black–Scholes model.

**Authors:** Mohamed Reda Elaoufir and Alexis Bruneau. MSc project, Université Paris 1 Panthéon-Sorbonne, March 2026. Supervisor: Christophe Chorro.

## Methods

- Vectorized, batched simulation of geometric Brownian motion and trapezoidal quadrature.
- Central finite differences with common random numbers.
- Two Malliavin integration-by-parts weights.
- Sampling variance, 95% confidence intervals, paired estimator comparisons, and time-step and bump sensitivity.

## Main numerical result

With 20,000 paths, 250 time steps, a spot bump of 0.2 and the fixed seed in the notebook, the range digital payoff has approximately **149x** and **140x** lower pathwise variance under Malliavin methods 1 and 2, respectively, than under finite differences. For the continuous call payoff, finite differences have lower variance than either Malliavin estimator. These are experiment-specific results, not universal performance guarantees. Confidence intervals quantify Monte Carlo sampling error, not discretization or bump bias.

## Repository contents

- `asian_option_delta.ipynb`: executed numerical notebook with figures and tables.
- `original_theoretical_report.pdf`: original academic report, preserved unchanged.
- `THEORY_CORRECTIONS.md`: corrected formulas and theoretical qualifications; read alongside the report.
- `requirements.txt`: Python dependencies.

## Reproduce

```bash
python -m pip install -r requirements.txt
jupyter notebook asian_option_delta.ipynb
```

Run all cells in order. No external data are needed. The model parameters are defined in the first code cell. The numerical notebook has been revised for clarity, correctness and reproducibility; the original report has not been silently rewritten.
