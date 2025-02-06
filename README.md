# Solute Solubility Datasets in ScCO₂

This repository contains datasets of solubility data of solutes in supercritical CO₂ (ScCO₂). The datasets are compiled from multiple published studies and include anthraquinone derivatives (AQDs) and drug-like compounds (Drugs), aiming to facilitate research in data-driven solubility modeling.

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
```plaintext
📂 dataset/
 ├── 28AQD_dataset.csv        # Solubility data for anthraquinone derivatives
 ├── 96Drug_dataset.csv       # Solubility data for drug-like compounds
 ├── README.md              # Description of dataset folder
```
## Example Data Format

| SMILES                  | Readout                 | Temperature (K) | Pressure (MPa) | LOG(y) |
|-------------------------|-------------------------|---------------|--------------|---------|
| C1=CC=C2C(=O)C=CC(=O)C2=C1 | [0.23, -0.45, 0.89, ...] | 313.15        | 10.0         | -5.21   |
| C1=CC=C(C=C1)C=O        | [0.12, -0.34, 0.76, ...] | 323.15        | 12.5         | -4.85   |

- **Readout Vector**: The readout vector is a 200-dimensional molecular representation, learned from the MPNN model during sigma profile prediction. It captures the structural and physicochemical features of the molecule.

## Usage

To use the dataset, clone the repository:

```bash
git clone https://github.com/yuchiaochu/Solubility_data.git
```
Then, load the dataset in Python using pandas:
```python
import pandas as pd

aqd_df = pd.read_csv("dataset/28AQD_dataset.csv")
drug_df = pd.read_csv("dataset/96Drug_dataset.csv")

print(aqd_df.head())
print(drug_df.head())
```

## Citation
```BibTex
@article{YourCitation,
  author    = {Your Name and Others},
  title     = {Solubility Prediction of Anthraquinone Derivatives and Drug-like Compounds in ScCO₂ Using a Graph-Based Deep Learning Framework},
  journal   = {Your Journal},
  year      = {202X},
  doi       = {Your DOI}
}
```


