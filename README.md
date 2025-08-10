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
