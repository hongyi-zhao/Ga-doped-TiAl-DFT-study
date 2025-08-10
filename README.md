# Ga-doped TiAl DFT Study - Dataset

This repository contains the complete computational dataset for the "First-Principles Study of Ga-doped γ-TiAl Intermetallic Compound".

## Directory Structure

### `/pristine_TiAl/`
Reference calculations for pristine γ-TiAl matrix
- `1.opt/` - Structure optimization
- `2.scf/` - Self-consistent field calculation 
- `3.band/` - Band structure calculation
- `4.dos/` - Density of states calculation
- `phonopy/` - Phonon and thermodynamic properties

### `/Ti_substitution/`
Ti-site substitutional doping calculations
- Same subdirectory structure as pristine_TiAl reference
- Ga atoms replacing Ti atoms in the crystal structure

### `/Al_substitution/` 
Al-site substitutional doping calculations
- Same subdirectory structure as pristine_TiAl reference
- Ga atoms replacing Al atoms in the crystal structure

### `/interstitial_doping/`
Interstitial doping calculations
- Same subdirectory structure as pristine_TiAl reference
- Ga atoms inserted into interstitial sites

### `/elastic/`
Elastic property calculations using Virtual Crystal Approximation (VCA)
- `0/` - Pure TiAl reference
- `0.01/` to `0.06/` - Different Ga concentrations (0.01% to 0.06%)
- VCA parameters: `VCA = 1 [Al_fraction] [Ga_fraction]` in INCAR files
- Elastic constants calculated using finite difference method (IBRION = 6)

### `/slab/`
Surface calculations for work function analysis
- `pristine_TiAl/`, `Ti_substitution/`, `Al_substitution/`, `interstitial_doping/` - Four different systems
- Each contains crystal face directories: `022/`, `100/`, `110/`, `111/`, `202/`
- 4-layer slab models with 15 Å vacuum layers

## Key Files

### Input Files:
- `POSCAR` - Crystal structure coordinates
- `INCAR` - Calculation parameters and settings
- `KPOINTS` - k-point sampling mesh
- `POTCAR` - Pseudopotential files

### Output Files:
- `CONTCAR` - Optimized crystal structure
- `OUTCAR` - Main output with energies, forces, and properties
- `vasprun.xml` - Detailed calculation results
- `DOSCAR` - Density of states data
- `EIGENVAL` - Eigenvalues and band energies
- `ELASTIC_TENSOR` - Elastic constants (elastic directories only)
- `PLANAR_AVERAGE.dat` - Planar averaged potential (slab directories only)
- `thermo.dat` - Thermodynamic properties (phonopy directories only)

### Processed Data Files:
- `PDOS_*.dat` - Partial density of states for each element
- `BAND.dat` - Band structure data
- `PBAND_*.dat` - Projected band structure data
- `TDOS.dat` - Total density of states

## Usage

Each directory contains complete VASP input and output files for the corresponding calculation type. Use VASPKIT, PHONOPY, or other standard tools for post-processing and analysis.
