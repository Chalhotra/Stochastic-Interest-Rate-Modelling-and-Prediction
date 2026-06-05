# Stochastic Interest Rate Modelling — CIR Model & Extensions

Implementation of the Cox-Ingersoll-Ross (1985) short-rate model, calibrated on real yield curve data and extended with a Two-Factor CIR model. Built as part of Finance Club IIT Roorkee's Open Projects 2026.

## What's in here

- **Data preprocessing** — outlier detection, interpolation, missing value handling
- **Base CIR** — MLE calibration on the 3M yield, closed-form yield curve reconstruction
- **Two-Factor CIR** — Longstaff-Schwartz (1992), hidden state recovery via 2×2 inversion, drift-only test propagation
- **CIR++** — deterministic shift correction with rolling window stabilisation

## Results

| Model | Pooled $R^2$ |
|-------|-------------|
| Base CIR (MLE) | 0.799 |
| Two-Factor CIR | 0.947 |

All predictions use **only the 3M yield** as input on test days.

## Structure

```
notebook.ipynb   — single Colab notebook, runs top to bottom
train_data.csv   — training yields (9 tenors, 3M–30Y)
test_data.csv    — test yields (5 tenors, 3M–2Y)
```

## Requirements

```
numpy, pandas, scipy, scikit-learn, matplotlib
```
