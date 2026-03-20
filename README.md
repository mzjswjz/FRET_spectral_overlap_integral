# FRET_spectral_overlap_integral

Jupyter notebook for calculating Förster Resonance Energy Transfer (FRET) spectral overlap integrals.

## Files

| File | Description |
|------|-------------|
| `FRET_intergal.ipynb` | Notebook for computing spectral overlap between donor emission and acceptor absorption |

## What It Does

The notebook calculates the spectral overlap integral (J) needed for FRET rate calculations:

```
J = ∫ F_D(λ) · ε_A(λ) · λ⁴ dλ
```

Where:
- `F_D(λ)` = Normalized donor emission spectrum
- `ε_A(λ)` = Acceptor molar extinction coefficient
- `λ` = Wavelength

## Key Calculations

- Loads donor photoluminescence (PL) data
- Loads acceptor absorption data
- Normalizes spectra
- Computes overlap integral
- Calculates Förster radius (R₀)

## Dependencies

- numpy
- pandas
- matplotlib
- scipy

## Author

mzjswjz
