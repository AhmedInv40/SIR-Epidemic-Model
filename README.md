# SIR-Epidemic-Model
This Model is a fundamental mathematical framework in epidimiology. Where are gonna explore the the basic reproduction number R0 and herd immunity thresholds.
I am gonna get into:
SIR Model Theory,
R0 Analysis,
Herd Immunity,
Numerical Methods,
Simulations,
Vaccination Effects.
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

## Key Results

- β (transmission rate): 0.25
- γ (recovery rate): 0.1
- R₀: 2.5
- Herd immunity threshold: 60%
- Infectious period: 10 days

Atilla Ahmed



