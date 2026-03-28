# SIR-Epidemic-Model
This Model is a fundamental mathematical framework in epidimiology. Where are gonna explore the the basic reproduction number R0 and herd immunity thresholds.
I am gonna get into:
SIR Model Theory,
R0 Analysis,
Herd Immunity,
Numerical Methods,
Simulations,
Vaccination Effects.
Stochastic SIR, testing randomness.
I am using numerical solution of the differential equations using scipy.integrate.odeint.
Derivation and computation of the basic reproduction number, threshold calculations for different disease.

## The SIR model is defined by three coupled differential equations:

- dS/dt = -βSI/N
- dI/dt = βSI/N - γI
- dR/dt = γI

## Key formulas:
- Basic reproduction number: R₀ = β/γ
- Herd immunity threshold: p = 1 - 1/R₀

## Requirements

- numpy
- matplotlib
- scipy

| Topic | Description |
|-------|-------------|
| **SIR Differential Equations** | Derivation and interpretation of dS/dt, dI/dt, dR/dt |
| **R₀ (Basic Reproduction Number)** | Formula derivation, threshold behavior, real-disease examples |
| **Herd Immunity** | Threshold formula p = 1 − 1/R₀, imperfect vaccine adjustments |
| **Numerical Methods** | Euler's method vs. scipy.integrate.odeint comparison |
| **Vaccination Scenarios** | Impact of different coverage levels on epidemic curves |
| **Stochastic SIR** | Gillespie algorithm — how randomness affects small populations |
| **Sensitivity Analysis** | Heatmaps, tornado diagrams, R₀ error amplification |
| **Parameter Misestimation** | Simulated scenario: what if β and γ are estimated wrong? |

## Visualizations

The notebook produces **12+ plots**, including:

- SIR time-series curves with annotated peak infection
- Phase portrait (I vs. S) showing epidemic trajectory and the R₀ = 1 threshold
- R₀ comparison panel — infection curves, cumulative cases, and phase portraits for multiple R₀ values
- Herd immunity threshold curve with real-disease markers (Flu, COVID, Smallpox, Measles)
- Vaccination effect plots — how increasing coverage flattens and eliminates the epidemic
- Stochastic vs. deterministic overlay — 50 Gillespie runs against the ODE solution
- Population size vs. noise — convergence of stochastic to deterministic as N grows
- Parameter sensitivity heatmaps — peak infections and attack rate across β–γ space
- Tornado diagram — which parameter the model is more sensitive to
- Misestimation comparison — true vs. estimated epidemic with hospital capacity overlay
- R₀ error amplification — non-linear relationship between estimation error and prediction error

## Key Results

| Metric | Value (β=0.25, γ=0.1, N=10,000) |
|--------|----------------------------------|
| R₀ | 2.50 |
| Herd immunity threshold | 60.0% |
| Peak infected | ~2,905 |
| Attack rate | ~89.8% |
| Vaccination needed (90% eff.) | ~66.7% |

**Sensitivity finding:** Underestimating β by 20% while overestimating γ by 20% causes R₀ to appear as 2.0 instead of 3.0 — leading to a peak infection underestimate of thousands of cases.

**Stochastic finding:** In small populations (N ≈ 200), epidemics frequently die out by chance even when R₀ > 1. As N grows beyond ~5,000, stochastic simulations converge tightly to the deterministic solution.

Atilla Ahmed



