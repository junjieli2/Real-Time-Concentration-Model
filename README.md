This repository contains the supporting data and programs associated with the following publication:

> **Junjie Li, Zhengbin Pan, Yiting Xiao, Xinyu Wang, and Bo Kong.**  
> *Real-Time Supersaturation Monitoring in Cooling Crystallization via Hybrid Electrical Conductivity–Ultrasonic Sensor Fusion.*  
> **The Canadian Journal of Chemical Engineering** (2026), Article cjce.70308.  
> DOI: [10.1002/cjce.70308](https://doi.org/10.1002/cjce.70308)

The repository is intended to support the reproducibility of the experimental data processing, sensor calibration, data fusion, supersaturation estimation, and visualization procedures reported in the paper.

## Overview

Cooling crystallization requires reliable real-time information on solution concentration and supersaturation. This work combines electrical conductivity and ultrasonic measurements to improve concentration estimation over different stages of the crystallization process.

The files provided in this repository may include:

- Raw and processed electrical conductivity measurements
- Raw and processed ultrasonic measurements

## Corrections (25 October 2026)

### Solubility correlation: Equation (2)

The quadratic term in the solubility correlation in Equation (2) should have a **negative** sign. The corrected expression is:

$$
c_{\mathrm{sat}}(T)=174.26\left(0.418+1.138\times10^{-2}T-1.688\times10^{-5}T^2\right).
$$

Here, $T$ is the temperature in degrees Celsius, and $c_{\mathrm{sat}}$ follows the concentration notation used in the paper. At $20\,^{\circ}\mathrm{C}$, this expression gives approximately $111.3257$ (reported as $111.3$ in the paper).

### Independent validation: corrected Table 1

The errors below are recalculated from the gravimetric and model-predicted concentration values printed in Table 1. The concentration entries are retained as published. Absolute errors are reported as non-negative values.

$$
E_{\mathrm{abs}}=\left|c_{\mathrm{model}}-c_{\mathrm{gravimetric}}\right|,
\qquad
E_{\mathrm{rel}}=\frac{E_{\mathrm{abs}}}{c_{\mathrm{gravimetric}}}\times100\%.
$$

| Gravimetric concentration (g/L) | US prediction (g/L) | EC prediction (g/L) | US absolute error (g/L) | EC absolute error (g/L) | US relative error (%) | EC relative error (%) |
| ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| 41.35 | 43.41 | 42.68 | 2.06 | 1.33 | 4.98 | 3.22 |
| 82.68 | 85.22 | 77.03 | 2.54 | 5.65 | 3.07 | 6.83 |
| 119.46 | 114.42 | 115.15 | 5.04 | 4.31 | 4.22 | 3.61 |

For the second sample, the corrected US absolute and relative errors are **2.54 g/L** and **3.07%**, and the corrected EC absolute and relative errors are **5.65 g/L** and **6.83%**.

Across these three independent validation samples, the maximum absolute errors are **5.04 g/L (US)** and **5.65 g/L (EC)**; the maximum relative errors are **4.98% (US)** and **6.83% (EC)**. These values correct the statement in Section 3.3.1 that all absolute errors were below 5 g/L and the maximum relative error was below 6%.
