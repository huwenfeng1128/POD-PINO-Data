# Figure Source Data

This folder contains the numerical data (source data) underlying **Figures 3–14** of the manuscript:

> **"A POD-PINO Approach for Identifying Governing Parameters of a Phenomenological Model for Liquid Rocket Engine Combustion Instability"**

Figures 1 and 2 are schematic diagrams and contain no numerical data.

## Parameter notation

The stochastic phenomenological model has three governing parameters:

| Symbol | Meaning |
|---|---|
| **ν (nu)** | linear growth rate |
| **κ (kappa)** | nonlinear saturation coefficient |
| **D** | diffusion parameter |

Filenames of the form `(ν, κ, D)` (e.g. `6.00,2.26,6.00.xlsx`) denote a specific parameter condition.

## Methods compared

- **FD** — finite-difference identification (numerical benchmark)
- **DeepONet** — deep operator network surrogate
- **POD-DeepONet** — proper-orthogonal-decomposition-based DeepONet
- **POD-PINO** — physics-informed POD-DeepONet (the proposed method)

## File-by-figure description

| Folder | Figure | Contents |
|---|---|---|
| `Fig3/` | Fig. 3 | Convergence histories: training total loss, validation total loss, validation data loss, and validation PDE residual (POD-DeepONet vs POD-PINO) |
| `Fig4/` | Fig. 4 | `WNRMSE.xlsx` — weighted normalized RMSE vs physics-loss weight |
| `Fig5/` | Fig. 5 | `PCI.xlsx` — Physical Consistency Index vs physics-loss weight |
| `Fig6/` | Fig. 6 | Predicted finite-time KM-coefficient fields and error distributions at three representative parameter conditions |
| `Fig7/` | Fig. 7 | First/second-order governing-equation residuals at three representative parameter conditions |
| `Fig8/` | Fig. 8 | Distributions of KM-coefficient prediction errors (`D1MSE`, `D2MSE`) and PDE residuals (`PDE Total MSE`, `Total MSE`) over the test set |
| `Fig9/` | Fig. 9 | Relative errors of identified parameters (interpolation) for FD, DeepONet, POD-DeepONet, POD-PINO |
| `Fig10/` | Fig. 10 | First-order (`R1MSE`), second-order (`R2MSE`) and total (`RTotalMSE`) governing-equation residuals (interpolation) |
| `Fig11/` | Fig. 11 | Steady-state amplitude probability density functions (`*PDF.xlsx`) and histograms (`*Histogram.xlsx`) at six parameter conditions |
| `Fig12/` | Fig. 12 | Relative errors of identified parameters (extrapolation) for DeepONet, POD-DeepONet, POD-PINO |
| `Fig13/` | Fig. 13 | Identified vs reference values of the three parameters (`nu.xlsx`, `kappa.xlsx`, `d.xlsx`) on the extrapolation test set |
| `Fig14/` | Fig. 14 | First/second-order and total governing-equation residuals associated with extrapolated parameter estimates |

## Data format

All files are Microsoft Excel (`.xlsx`). Each file contains the numerical values plotted in the corresponding figure panel(s).

## Related resources

- Code: <https://github.com/huwenfeng1128/POD-PINO>
- Trained model weights: see the parent `POD-PINO_data` directory.

## License

MIT License.
