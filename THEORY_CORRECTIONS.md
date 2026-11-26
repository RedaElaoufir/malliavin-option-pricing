# Corrections to the original theoretical report

The original jointly authored report is preserved unchanged for academic attribution. The following errata supersede the affected formulas in the numerical companion.

## Part B(b), (e): first Malliavin weight

Define $A=\int_0^T X_t\,dt$, $J_1=\int_0^T t X_t\,dt$, $J_2=\int_0^T t^2 X_t\,dt$ and $B=\sigma J_1$. Then $D_t A=\sigma\int_t^T X_s\,ds$ and $\int_0^T D_t B\,dt=\sigma^2 J_2$ (not $\sigma J_2$). The divergence product rule gives

$$\delta(A/B)=\frac{AB_T}{B}-1+\frac{A\sigma^2J_2}{B^2}=\frac{AB_T}{\sigma J_1}+\frac{AJ_2}{J_1^2}-1.$$

This replaces the inconsistent expressions on printed pages 4 and 6 (PDF pages 5 and 7). The original notebook's factor $1/x$ inside the second term was also incorrect. The line involving $\delta(A)$ in step 6 is not needed: the divergence of the process $t\mapsto X_t$, rather than of the scalar $A$, is the Itô integral shown there.

## Part B(c): second weight

The second formula is retained: $\Pi_2=2\sigma^{-2}((X_T-x)/A-r)+1$.

For both choices, $\Delta(x)=e^{-rT}\mathbb E[\Phi(A)\Pi_i]/x$. The factor $1/x$ is applied once, outside the unnormalized weight. Part B(d) uses a normalized weight; distinguish it from these $\Pi_i$.

## Scope of the variance result and discontinuous payoff

The conditioning argument applies when the payoff-weighted variable is square-integrable. For a fixed payoff, equality of variances need not imply that the weight is measurable everywhere (the payoff may vanish). The digital payoff is outside the continuous linear-growth class in Part B(f); its use additionally requires an extension by smoothing/density or an equivalent weak-derivative argument. The notebook illustrates this extension numerically rather than claiming that Part B(f) alone proves it.
