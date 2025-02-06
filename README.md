# Solubility Prediction Dataset in ScCO₂

This repository contains a curated dataset for solubility prediction of solutes in supercritical CO₂ (ScCO₂). The dataset is compiled from multiple published studies and includes anthraquinone derivatives (AQDs) and drug-like compounds (Drugs), aiming to facilitate research in data-driven solubility modeling.

## Dataset Overview

- **AQD Dataset**: Includes solubility data of 28 anthraquinone derivatives in ScCO₂.
- **Drug Dataset**: Includes solubility data of 96 drug-like compounds in ScCO₂.
- **Features**:
  - **SMILES**: Canonical SMILES representation of each solute.
  - **Readout**: The readout vector obtained from the MPNN model during sigma profile prediction.
  - **Temperature (K)**: Experimental temperature condition in Kelvin.
  - **Pressure (MPa)**: Experimental pressure condition in Megapascal.
  - **LOG(y)**: Logarithmic solubility value of the solute in ScCO₂.

## Data Sources

The solubility data in this repository are collected and curated from multiple published studies. The full list of original sources, data processing methods, and experimental conditions can be found in our paper:

> **[Your Paper Title]**  
> *Your Name et al.*  
> Journal Name, Year. DOI: [Your DOI]
(For a complete reference list, please check `metadata.json`.)

## File Structure
### Example Data Format

| SMILES                  | Readout                 | Temperature (K) | Pressure (MPa) | LOG(y) |
|-------------------------|-------------------------|---------------|--------------|---------|
| C1=CC=C2C(=O)C=CC(=O)C2=C1 | [0.23, -0.45, 0.89, ...] | 313.15        | 10.0         | -5.21   |
| C1=CC=C(C=C1)C=O        | [0.12, -0.34, 0.76, ...] | 323.15        | 12.5         | -4.85   |

- **Readout Vector**: The readout vector is a learned representation from the MPNN model, which is used in sigma profile prediction. It captures structural and physicochemical features of the molecule.

## Usage

To use the dataset, simply clone the repository:

```bash
git clone https://github.com/yuchiaochu/Solubility_data.git

