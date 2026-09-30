
Coordinate Displacement Algorithm (CDA) — Reproducibility Suite
This repository contains the numerical verification scripts for the Coordinate Displacement Algorithm (CDA) manuscript. It enables reviewers and readers to independently execute and validate the benchmark performance on the extreme degree test polynomial.
Benchmark Target
The stress test evaluates the root convergence for the 60,000^{\text{th}}-degree polynomial equation:
Prerequisites & Installation
To avoid floating-point overflow (x^{60000} \to \infty), the implementation uses standard arbitrary-precision arithmetic (gmpy2 / MPFR library).
Requirements
 * Python 3.8+
 * gmpy2
Setup Instructions
1. Clone the repository
git clone https://github.com/krllatonio-dot/CDA-Stress-Test.git
cd CDA-Stress-Test
2. Install dependencies
pip install gmpy2
Running the Verification Test
Run the benchmark script directly from your terminal:
python cda_stress_test.py
Expected Output
================================================================================
Coordinate Displacement Algorithm (CDA) - Benchmark Execution
Target Polynomial: f(x) = x^60000 - 4x^59999 + 9x^59998 + 9x^59997 + 3x - 14
[+] Macro-Scale Seed Initialized: x_0 = 0.999983333333333333
Iter (t)  Coordinate State (x_t)        Residual f(x_t)          Step Delta
0         0.9999833333333333            -1.26442180e-01          ---
1         0.9999948305525564            0.00000000e+00           -1.14972190e-05
2         0.9999948305525564            0.00000000e+00            0.00000000e+00
[✓] Convergence Reached at Iteration t = 2
[✓] Final Computed Root (x*): 0.9999948305525564
[✓] Final Function Residual:  0.0000000000000000e+00
Citation
If you find this code or algorithm useful for your research, please cite the primary manuscript:
@article{CDA2026,
title={Coordinate Displacement Algorithm for Extreme-Degree Polynomial Root Finding},
author={Latonio, Karl Arvin},
year={2026}
}
