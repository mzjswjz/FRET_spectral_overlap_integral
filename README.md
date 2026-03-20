# FRET_spectral_overlap_integral

This repository provides tools for calculating the spectral overlap integral (J) used in Förster Resonance Energy Transfer (FRET) analysis, particularly for organic photovoltaic and light-emitting systems.

## What is FRET?

**Förster Resonance Energy Transfer (FRET)** is a non-radiative energy transfer process between two chromophores:
- **Donor (D)**: Excited molecule that transfers energy
- **Acceptor (A)**: Molecule that receives the energy

FRET occurs when:
1. The donor emission spectrum overlaps with the acceptor absorption spectrum
2. The donor and acceptor are in close proximity (typically 1-10 nm)
3. The transition dipoles are properly oriented

FRET efficiency depends on the sixth power of the distance between donor and acceptor, making it a sensitive molecular ruler.

## Theory Background

The Förster resonance energy transfer rate is given by:

$$k_{FRET} = \frac{1}{\tau_D} \left(\frac{R_0}{r}\right)^6$$

Where:
- $\tau_D$ = donor excited-state lifetime
- $R_0$ = Förster radius (distance at which 50% energy transfer occurs)
- $r$ = donor-acceptor distance

The Förster radius $R_0$ is calculated as:

$$R_0^6 = \frac{9 \ln(10) \kappa^2 Q_D}{128 \pi^5 n^4 N_A} J$$

Where:
- $\kappa^2$ = orientation factor (typically 2/3 for random orientation)
- $Q_D$ = donor photoluminescence quantum yield
- $n$ = refractive index of the medium
- $N_A$ = Avogadro's number
- $J$ = spectral overlap integral

## Spectral Overlap Calculation

The spectral overlap integral $J$ is defined as:

$$J = \int_0^\infty \varepsilon_A(\lambda) \cdot f_D(\lambda) \cdot \lambda^4 \, d\lambda$$

Where:
- $\varepsilon_A(\lambda)$ = acceptor molar extinction coefficient (L mol⁻¹ cm⁻¹)
- $f_D(\lambda)$ = normalized donor photoluminescence spectrum (area = 1)
- $\lambda$ = wavelength (nm)

The units of $J$ are: **L mol⁻¹ cm⁻¹ nm⁴**

## Usage

The Jupyter notebook `FRET_intergal.ipynb` provides a complete workflow:

1. **Load donor PL spectrum**: Photoluminescence data normalized to unit area
2. **Load acceptor absorption**: Molar extinction coefficient or absorption spectrum
3. **Calculate overlap integral**: Numerical integration using Simpson's rule
4. **Compute Förster radius**: Given donor quantum yield and refractive index
5. **Visualize overlap**: Plot donor emission and acceptor absorption spectra

### Supported Systems

The repository includes example calculations for various donor-acceptor pairs relevant to organic photovoltaics and FRET-based devices.

### Input Data Format

- Donor PL: Two-column file (wavelength in nm, intensity in arbitrary units)
- Acceptor absorption: Two-column file (wavelength in nm, extinction coefficient or absorbance)
- Additional parameters: Molecular weight, density (for extinction coefficient calculation)

## Dependencies

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- SciPy (for integration)

## Author

mzjswjz
