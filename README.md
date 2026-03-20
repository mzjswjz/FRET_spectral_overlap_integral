# FRET_spectral_overlap_integral

Calculation tools for Förster Resonance Energy Transfer (FRET) spectral overlap integrals.

## Description

This repository contains Jupyter notebooks for calculating spectral overlap integrals used in Förster Resonance Energy Transfer (FRET) analysis. FRET is a mechanism describing energy transfer between two light-sensitive molecules (chromophores), and the spectral overlap integral is a key parameter in calculating Förster distances.

## Requirements

- Python 3.x
- Jupyter Notebook
- NumPy
- SciPy
- Matplotlib

## Usage

1. Clone the repository
2. Install dependencies: `pip install numpy scipy matplotlib jupyter`
3. Open the notebooks in Jupyter: `jupyter notebook`
4. Follow the notebook instructions to calculate spectral overlap integrals

## Theory

The spectral overlap integral (J) is defined as:

J = ∫ F_D(λ) ε_A(λ) λ⁴ dλ

where F_D is the normalized donor emission spectrum and ε_A is the acceptor molar extinction coefficient.

## Author

mzjswjz

## License

MIT
